---
created_at: 2023-01-08
type: video
aliases: []
link: https://youtu.be/jPKTo1iGQiE
---

# Design Youtube – Neetcode

<iframe width="560" height="315" src="https://www.youtube.com/embed/jPKTo1iGQiE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Notes and highlights.

- [01:30](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=90.26987214877319) make sure to only pick a few functional requirements to focus on.
	- we will pick uploading and watching videos.
- [02:06](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=126.46583904005432) non-functional requirements.
	- uploaded videos should ensure that they don’t disappear or get corrupted.
- [02:52](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=172.9987630076294) back-of-envelope estimations *(note that this isn’t super important).*
	- assume one billion DAU.
	- 1% of users upload videos, and the average user watches 5 videos per day.
	- assume that most videos do not get views.
	- 500 videos uploaded per second.
- [04:19](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=259.7046371468658) favor availability over consistency.
	- we want the page to always load, but users can sometimes wait a bit for a new video to show up.
	- different considerations for livestreams, but out of scope.
- [05:26](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=326.1878109256134) minimize latency.
	- start playing the video before the entire video is loaded.
- [05:47](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=347.5793671087189) high level design for user uploading a video.
	- load balancer with a bunch of app servers.
		- can include a [[rate-limiter]] in this.
	- we will store the raw video files in some object store like AWS S3, they will handle [[database-replication]] for us.
	- videos should also have metadata that contains the title, description, author, etc.
		- this data will be stored in a [[nosql-database]] database like MongoDB, which contains a reference to the video file in the data store.
		- can be keyed by the video id.
	- [11:23](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=683.26889) we need to encode the videos to compress/normalize them.
		- this is a non-trivial operation that will take time.
		- use a [[message-queue]] to have a separate service encode the videos using [[asynchronism]].
			- how many workers should we have?
				- we need more than 500 workers because assuming we have 500 videos uploaded in a second, the videos uploaded in the next second will not have any workers to encode those.
				- so, we need way more than 500 workers.
		- send these encoded videos to object storage.
- [13:06](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=786.3662799904632) caching to improve read speeds.
	- we can use a [[content-delivery-network]] to distribute the video geographically across the world.
	- we can use [[caching]] for our metadata database to improve read speeds for users who are trying to watch videos.
- [18:08](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=1080) explanation of the way that youtube loads chunks of video at a time instead of using streaming.
	- this is how we lower [[latency]] by chunking our data.
	- this is known as video streaming, but we’re not exactly livestreaming, which is different.
- [23:34](https://www.youtube.com/watch?v=jPKTo1iGQiE#t=1414.694799011444) comparisons with real youtube.
	- YouTube doesn’t actually use a nosql database, but uses [[mysql]].
		- mongodb didn’t exist when youtube was starting.
		- they tried [[database-replication]] and [[database-sharding|sharding]] to try to scale.
		- they then created vitess to decouple the application layer from the database layer.
