---
type: system-design-example
parents:
  - "[[system-design]]"
---

# web crawler

- typical usecases.
	- search engine indexing.
	- web archiving.
	- data mining the internet for training data for machine learning models.
- clarifications.
	- needs to recursively go to webpages, download them, and continue exploring the links on those pages.
	- in this case, assume it is for search engine indexing.
	- web crawler indexes one billion pages in a month.
	- only scrapes for html files.
	- needs to consider newly created pages.
	- needs to store these indexed pages for five years.
	- pages with duplicate content should be ignored.
- back of the envelope estimations.
	- needs to download about 400 pages per second.
		- peak would be about 800 pages per second.
	- assuming the average html webpage is 500 kilobytes, we need to store 500 terabytes per month and storage of up to 30 petabytes for 5 years.
- design.
	- we first assemble some seed urls for our web crawler to start at.
	- starting at these urls, the web crawler calls a dns server to convert the urls into ip addresses.
	- we need a component that actually parses the content in the webpages and extract new urls to visit.
		- should be run separately because it will slow down the crawler.
		- we can use a [[message-queue]] and [[asynchronism]] to process new webpages without slowing down the actual web crawler.
		- because the number of pages in the queue can grow very large, we should keep a buffer for fast lookup of urls while keeping the majority of the urls on disk.
	- we can keep track of webpages that we’ve already seen with a sort of set structure, where we compare the hashes of two html files to see if we’ve seen it before.
	- should have another microservice that extracts urls from an html file, which can also run asynchronously.
	- ![[web-crawler-diagram.png]]
	- politeness is a concept important in the field of web crawlers because we don’t want to be ddos’ing any hosts.
		- we should spread out different hostnames to different workers in our distributed system so that we don’t have all of our workers hit the same hostname in parallel.
	- we can cache `robots.txt` files for websites.
		- this is a file websites put up to tell web crawlers what they should and should not index.
- further points.
	- many websites do server-side rendering or dynamic content.
		- how do we deal with this?
