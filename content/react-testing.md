---
created_at: 2023-01-05
type: video
aliases: []
---

# React Testing Crash Course

<iframe width="560" height="315" src="https://www.youtube.com/embed/OVNjsIto9xM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

- [03:37](https://www.youtube.com/watch?v=OVNjsIto9xM#t=217.74264096185303) what should you test?
	- test for high value features first, edge cases.
	- test for both happy paths and common sad paths.
	- react component testing.
		- conditional rendering, utils/hooks.
- [08:32](https://www.youtube.com/watch?v=OVNjsIto9xM#t=512.1363119713898) examples of the above testing priorities in a test app.
- [10:06](https://www.youtube.com/watch?v=OVNjsIto9xM#t=600) tiers of testing.
	- unit tests, integration tests, end-to-end tests.
- [12:49](https://www.youtube.com/watch?v=OVNjsIto9xM#t=769.8240419008179) code for unit tests using react testing library.
- [15:20](https://www.youtube.com/watch?v=OVNjsIto9xM#t=920.4393120400543) using `debug` in react testing.
- [18:46](https://www.youtube.com/watch?v=OVNjsIto9xM#t=1126.847246164032) when you’re making an assertion, first assert the wrong thing and make sure the test fails before trying to make the test pass.
- [26:19](https://www.youtube.com/watch?v=OVNjsIto9xM#t=1579.0182699103545) integration test code example.
	- main idea is to resemble a realistic user flow.
	- sometimes can combine many unit tests into one integration test.
- [28:11](https://www.youtube.com/watch?v=OVNjsIto9xM#t=1691.068735011444) e2e tests.
	- video example uses cypress.
- [30:31](https://youtu.be/OVNjsIto9xM#t=1831.097661929428) example integration test in cypress.
- [35:57](https://youtu.be/OVNjsIto9xM#t=2157.91026206485) use testing playground to help you get the selectors for targeting certain elements in your app for testing.
	- probably should just use testing ids for everything though…
- [55:54](https://youtu.be/OVNjsIto9xM#t=3354.7434570228884) wrap up, conlusion.
	- need to check if the app behaves as expected.

```js
// cypress test
describe("payment", () => {
	it("my first test goes here", () => {
		// write test logic here
		cy.visit("/") // actually opens a browser to simulate being a user
	})
})
```

- 

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[testing]], [[react]]
