---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
api/webservers ^A2GpqDKz

client(s) ^XplmRVct

success ^94M3sZyO

failure (too many requests) ^wumSZeej

cache
(high throughput) ^98FaI0f8

logging mechanism ^nrzyywoM

database (nosql) ^rqIzafJN

http 200 ^5D0JroNY

- server-side rate-limiter
- use ip/user-id for unique identifier
- send HTTP 429 on rejection
- use load balancer to scale with multiple load balancers
- each rate limiter can send to specific set of servers
  so that we don't need another layer of load balancers ^ADLDwJqv

rate limiter ^WRp1OQyu

load balancer ^dWmDqizl

multiple rate limiters ^5k9cQOoe

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://excalidraw.com",
	"elements": [
		{
			"type": "rectangle",
			"version": 693,
			"versionNonce": 1963137042,
			"isDeleted": false,
			"id": "acEfDy7Supqen6bv7bCDJ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -550.8684738825707,
			"y": -241.46484375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 100,
			"height": 47,
			"seed": 1716336402,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"id": "XplmRVct",
					"type": "text"
				},
				{
					"id": "T8pDVSR8Ly-6-vIE5-vBM",
					"type": "arrow"
				},
				{
					"id": "Cy1Mwb00l_LNYB43fQsgP",
					"type": "arrow"
				},
				{
					"id": "DxMWk99s3EgBpYweJP400",
					"type": "arrow"
				},
				{
					"id": "JnVKt9TK669Ope64ORuot",
					"type": "arrow"
				}
			],
			"updated": 1669671121465,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 588,
			"versionNonce": 18407054,
			"isDeleted": false,
			"id": "XplmRVct",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -532.8684738825707,
			"y": -227.96484375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 64,
			"height": 20,
			"seed": 2037941458,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019457,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client(s)",
			"rawText": "client(s)",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "acEfDy7Supqen6bv7bCDJ",
			"originalText": "client(s)"
		},
		{
			"type": "diamond",
			"version": 654,
			"versionNonce": 939254098,
			"isDeleted": false,
			"id": "zUS4zd5VPSarPWxVoj5Qk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -62.5546875,
			"y": -263.21484375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 104,
			"height": 87,
			"seed": 1719221842,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"id": "WRp1OQyu",
					"type": "text"
				},
				{
					"id": "T8pDVSR8Ly-6-vIE5-vBM",
					"type": "arrow"
				},
				{
					"id": "_0JcYoeCghwKbv3fjAawx",
					"type": "arrow"
				},
				{
					"id": "Cy1Mwb00l_LNYB43fQsgP",
					"type": "arrow"
				},
				{
					"id": "knzn4Z3oVVIGTlonU0tly",
					"type": "arrow"
				},
				{
					"id": "DxMWk99s3EgBpYweJP400",
					"type": "arrow"
				},
				{
					"id": "TZyZjEsdF9a5w3Vzhy3NP",
					"type": "arrow"
				},
				{
					"id": "5_OqRwOvjXUaehsTPZLxX",
					"type": "arrow"
				}
			],
			"updated": 1669671045681,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 669,
			"versionNonce": 1876548814,
			"isDeleted": false,
			"id": "WRp1OQyu",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -56.5546875,
			"y": -229.71484375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 92,
			"height": 20,
			"seed": 2099356690,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019457,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "rate limiter",
			"rawText": "rate limiter",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "zUS4zd5VPSarPWxVoj5Qk",
			"originalText": "rate limiter"
		},
		{
			"type": "rectangle",
			"version": 786,
			"versionNonce": 2027527954,
			"isDeleted": false,
			"id": "_a7y8DS8xEAPuDZ-ErrIw",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 151.072265625,
			"y": -249.92578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 181,
			"height": 60,
			"seed": 1127611790,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "A2GpqDKz"
				},
				{
					"id": "_0JcYoeCghwKbv3fjAawx",
					"type": "arrow"
				},
				{
					"id": "knzn4Z3oVVIGTlonU0tly",
					"type": "arrow"
				}
			],
			"updated": 1669671019457,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 698,
			"versionNonce": 1382093582,
			"isDeleted": false,
			"id": "A2GpqDKz",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 183.572265625,
			"y": -229.92578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 116,
			"height": 20,
			"seed": 1332827470,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019457,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "api/webservers",
			"rawText": "api/webservers",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "_a7y8DS8xEAPuDZ-ErrIw",
			"originalText": "api/webservers"
		},
		{
			"type": "arrow",
			"version": 858,
			"versionNonce": 1373077134,
			"isDeleted": false,
			"id": "T8pDVSR8Ly-6-vIE5-vBM",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -444.3079270075707,
			"y": -218.56938886718603,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 110.74780134163143,
			"height": 0,
			"seed": 113922194,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479686,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "acEfDy7Supqen6bv7bCDJ",
				"gap": 6.560546875,
				"focus": -0.025725324135575958
			},
			"endBinding": {
				"elementId": "I0x6jboIQt5Z4Q65P81D1",
				"gap": 11.73024294878769,
				"focus": 0.25763848747706525
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					110.74780134163143,
					0
				]
			]
		},
		{
			"type": "arrow",
			"version": 229,
			"versionNonce": 207056014,
			"isDeleted": false,
			"id": "_0JcYoeCghwKbv3fjAawx",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 47.4976772063126,
			"y": -219.18281693333816,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 96.0687290436874,
			"height": 2.552114573934375,
			"seed": 1351537298,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479679,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "zUS4zd5VPSarPWxVoj5Qk",
				"gap": 6.075703339685511,
				"focus": -0.023262585787978195
			},
			"endBinding": {
				"elementId": "_a7y8DS8xEAPuDZ-ErrIw",
				"gap": 7.505859375,
				"focus": -0.18195332669904737
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					49.3206821686874,
					1.3117231833381595
				],
				[
					96.0687290436874,
					2.552114573934375
				]
			]
		},
		{
			"type": "text",
			"version": 214,
			"versionNonce": 629548942,
			"isDeleted": false,
			"id": "94M3sZyO",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 55.25390625,
			"y": -239,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 62,
			"height": 20,
			"seed": 1839974738,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019457,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "success",
			"rawText": "success",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "success"
		},
		{
			"type": "arrow",
			"version": 1860,
			"versionNonce": 979959570,
			"isDeleted": false,
			"id": "Cy1Mwb00l_LNYB43fQsgP",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -16.520636891927964,
			"y": -169.11747389036282,
			"strokeColor": "#c92a2a",
			"backgroundColor": "transparent",
			"width": 235.68711340634104,
			"height": 42.543923750944,
			"seed": 1779617614,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479686,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "CkPm8MXN4apAylNybBtV9",
				"focus": -0.8133581147686592,
				"gap": 1
			},
			"endBinding": {
				"elementId": "I0x6jboIQt5Z4Q65P81D1",
				"gap": 13.571266085622739,
				"focus": 0.8215340321898914
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-102.92662873307204,
					41.24833326536282
				],
				[
					-235.68711340634104,
					-1.2955904855811866
				]
			]
		},
		{
			"type": "text",
			"version": 198,
			"versionNonce": 162923982,
			"isDeleted": false,
			"id": "wumSZeej",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -219.671875,
			"y": -118.1875,
			"strokeColor": "#c92a2a",
			"backgroundColor": "transparent",
			"width": 220,
			"height": 20,
			"seed": 771627022,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019457,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "failure (too many requests)",
			"rawText": "failure (too many requests)",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "failure (too many requests)"
		},
		{
			"type": "arrow",
			"version": 122,
			"versionNonce": 1880533710,
			"isDeleted": false,
			"id": "knzn4Z3oVVIGTlonU0tly",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 142.3359375,
			"y": -203.01755153349768,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 105.09774248171537,
			"height": 0.6732351480095815,
			"seed": 873294226,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479679,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "_a7y8DS8xEAPuDZ-ErrIw",
				"gap": 8.736328125,
				"focus": -0.5316083938404832
			},
			"endBinding": {
				"elementId": "zUS4zd5VPSarPWxVoj5Qk",
				"gap": 10.623953379782002,
				"focus": 0.4063604373479382
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-105.09774248171537,
					0.6732351480095815
				]
			]
		},
		{
			"type": "arrow",
			"version": 1625,
			"versionNonce": 2090317902,
			"isDeleted": false,
			"id": "HogJ64fYm3annAjyEmcnQ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -130.63425075358572,
			"y": -200.05318895614434,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 45.492778917833334,
			"height": 0.9878242817481748,
			"seed": 801531278,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479686,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "5D0JroNY",
				"gap": 7.1500639137649955,
				"focus": 1.5188767584858958
			},
			"endBinding": {
				"elementId": "I0x6jboIQt5Z4Q65P81D1",
				"gap": 11.702853045732525,
				"focus": 0.4879292901249346
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-45.492778917833334,
					0.9878242817481748
				]
			]
		},
		{
			"type": "ellipse",
			"version": 410,
			"versionNonce": 953807826,
			"isDeleted": false,
			"id": "xzkaf9Ch1FaE9p6wbNpIu",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 104.49609375,
			"y": -102.203125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 181,
			"height": 92,
			"seed": 1622729426,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "98FaI0f8"
				},
				{
					"id": "TZyZjEsdF9a5w3Vzhy3NP",
					"type": "arrow"
				},
				{
					"id": "QpFAuUICI4q7K9Gfvs2Xa",
					"type": "arrow"
				}
			],
			"updated": 1669671019458,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 302,
			"versionNonce": 2093984146,
			"isDeleted": false,
			"id": "98FaI0f8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 128.49609375,
			"y": -76.203125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 133,
			"height": 40,
			"seed": 1852073038,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019458,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "cache\n(high throughput)",
			"rawText": "cache\n(high throughput)",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "xzkaf9Ch1FaE9p6wbNpIu",
			"originalText": "cache\n(high throughput)"
		},
		{
			"type": "arrow",
			"version": 183,
			"versionNonce": 232005902,
			"isDeleted": false,
			"id": "TZyZjEsdF9a5w3Vzhy3NP",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 18.585332181088006,
			"y": -191.57371237744863,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 112.65016931305038,
			"height": 92.44912636945446,
			"seed": 65473298,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479680,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "zUS4zd5VPSarPWxVoj5Qk",
				"gap": 6.91681096953841,
				"focus": 0.09715308132318816
			},
			"endBinding": {
				"elementId": "xzkaf9Ch1FaE9p6wbNpIu",
				"gap": 9.656439179813674,
				"focus": -0.10765769221393608
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					112.65016931305038,
					92.44912636945446
				]
			]
		},
		{
			"type": "rectangle",
			"version": 183,
			"versionNonce": 738764626,
			"isDeleted": false,
			"id": "aHtLBkmmUdQQFf-Opjfet",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 131.50390625,
			"y": 52.767578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 137,
			"height": 57,
			"seed": 586753038,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "nrzyywoM"
				},
				{
					"id": "QpFAuUICI4q7K9Gfvs2Xa",
					"type": "arrow"
				},
				{
					"id": "mlyRqfb8R2FVSVihkzFhk",
					"type": "arrow"
				}
			],
			"updated": 1669671019458,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 86,
			"versionNonce": 1941286606,
			"isDeleted": false,
			"id": "nrzyywoM",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 161.00390625,
			"y": 61.267578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 78,
			"height": 40,
			"seed": 1890787854,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019458,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "logging \nmechanism",
			"rawText": "logging mechanism",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aHtLBkmmUdQQFf-Opjfet",
			"originalText": "logging mechanism"
		},
		{
			"type": "arrow",
			"version": 78,
			"versionNonce": 1846392206,
			"isDeleted": false,
			"id": "QpFAuUICI4q7K9Gfvs2Xa",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 195.12109378960292,
			"y": -1.8359390443769925,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 1.1328125396029236,
			"height": 44.17578279437699,
			"seed": 305287054,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479680,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "xzkaf9Ch1FaE9p6wbNpIu",
				"gap": 8.367229408941917,
				"focus": -0.016784803187919244
			},
			"endBinding": {
				"elementId": "aHtLBkmmUdQQFf-Opjfet",
				"gap": 10.427734375,
				"focus": -0.10131122083317634
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-1.1328125396029236,
					44.17578279437699
				]
			]
		},
		{
			"type": "ellipse",
			"version": 299,
			"versionNonce": 1324524814,
			"isDeleted": false,
			"id": "qJvxOBE8YTHlwhey3PTIo",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 117.67578125,
			"y": 176.560546875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 168,
			"height": 93,
			"seed": 973299854,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "rqIzafJN"
				},
				{
					"id": "mlyRqfb8R2FVSVihkzFhk",
					"type": "arrow"
				}
			],
			"updated": 1669671019458,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 228,
			"versionNonce": 1254128338,
			"isDeleted": false,
			"id": "rqIzafJN",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 133.67578125,
			"y": 213.060546875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 136,
			"height": 20,
			"seed": 2084169362,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019458,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "database (nosql)",
			"rawText": "database (nosql)",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "qJvxOBE8YTHlwhey3PTIo",
			"originalText": "database (nosql)"
		},
		{
			"type": "arrow",
			"version": 79,
			"versionNonce": 189540878,
			"isDeleted": false,
			"id": "mlyRqfb8R2FVSVihkzFhk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 196.28571419387754,
			"y": 118.92578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 0.04077322216713242,
			"height": 45.021434356951346,
			"seed": 337658770,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479685,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "aHtLBkmmUdQQFf-Opjfet",
				"gap": 9.158203125,
				"focus": 0.053775091240875914
			},
			"endBinding": {
				"elementId": "qJvxOBE8YTHlwhey3PTIo",
				"gap": 12.706765172980397,
				"focus": -0.06529017857142858
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-0.04077322216713242,
					45.021434356951346
				]
			]
		},
		{
			"type": "text",
			"version": 529,
			"versionNonce": 1052174354,
			"isDeleted": false,
			"id": "5D0JroNY",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -126.1015625,
			"y": -194.5234375,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 78,
			"height": 20,
			"seed": 1882535886,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"id": "HogJ64fYm3annAjyEmcnQ",
					"type": "arrow"
				}
			],
			"updated": 1669671100057,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "http 200",
			"rawText": "http 200",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "http 200"
		},
		{
			"type": "text",
			"version": 992,
			"versionNonce": 2135581646,
			"isDeleted": false,
			"id": "ADLDwJqv",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -445.4832721105155,
			"y": -57.33486938775542,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 456,
			"height": 120,
			"seed": 351288782,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671500638,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "- server-side rate-limiter\n- use ip/user-id for unique identifier\n- send HTTP 429 on rejection\n- use load balancer to scale with multiple load balancers\n- each rate limiter can send to specific set of servers\n  so that we don't need another layer of load balancers",
			"rawText": "- server-side rate-limiter\n- use ip/user-id for unique identifier\n- send HTTP 429 on rejection\n- use load balancer to scale with multiple load balancers\n- each rate limiter can send to specific set of servers\n  so that we don't need another layer of load balancers",
			"baseline": 114,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- server-side rate-limiter\n- use ip/user-id for unique identifier\n- send HTTP 429 on rejection\n- use load balancer to scale with multiple load balancers\n- each rate limiter can send to specific set of servers\n  so that we don't need another layer of load balancers"
		},
		{
			"type": "diamond",
			"version": 1227,
			"versionNonce": 1403559118,
			"isDeleted": false,
			"id": "CkPm8MXN4apAylNybBtV9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -61.60821946660201,
			"y": -250.7687358588878,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 104,
			"height": 87,
			"seed": 350366674,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"id": "T8pDVSR8Ly-6-vIE5-vBM",
					"type": "arrow"
				},
				{
					"id": "_0JcYoeCghwKbv3fjAawx",
					"type": "arrow"
				},
				{
					"id": "Cy1Mwb00l_LNYB43fQsgP",
					"type": "arrow"
				},
				{
					"id": "knzn4Z3oVVIGTlonU0tly",
					"type": "arrow"
				},
				{
					"id": "DxMWk99s3EgBpYweJP400",
					"type": "arrow"
				},
				{
					"id": "TZyZjEsdF9a5w3Vzhy3NP",
					"type": "arrow"
				},
				{
					"id": "5_OqRwOvjXUaehsTPZLxX",
					"type": "arrow"
				}
			],
			"updated": 1669671090507,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 413,
			"versionNonce": 2054763090,
			"isDeleted": false,
			"id": "I0x6jboIQt5Z4Q65P81D1",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -321.8298827171516,
			"y": -238.98433046156674,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 134,
			"height": 55,
			"seed": 1939083470,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "dWmDqizl"
				},
				{
					"id": "HogJ64fYm3annAjyEmcnQ",
					"type": "arrow"
				},
				{
					"id": "T8pDVSR8Ly-6-vIE5-vBM",
					"type": "arrow"
				},
				{
					"id": "DxMWk99s3EgBpYweJP400",
					"type": "arrow"
				},
				{
					"id": "Cy1Mwb00l_LNYB43fQsgP",
					"type": "arrow"
				},
				{
					"id": "JnVKt9TK669Ope64ORuot",
					"type": "arrow"
				}
			],
			"updated": 1669671121465,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 288,
			"versionNonce": 639876174,
			"isDeleted": false,
			"id": "dWmDqizl",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -308.8298827171516,
			"y": -221.48433046156674,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 108,
			"height": 20,
			"seed": 1186405138,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671019458,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "load balancer",
			"rawText": "load balancer",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "I0x6jboIQt5Z4Q65P81D1",
			"originalText": "load balancer"
		},
		{
			"type": "arrow",
			"version": 759,
			"versionNonce": 643891474,
			"isDeleted": false,
			"id": "5_OqRwOvjXUaehsTPZLxX",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -170.83872429202927,
			"y": -220.15387108297722,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 100.61454412939315,
			"height": 0,
			"seed": 900550674,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671094266,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "CkPm8MXN4apAylNybBtV9",
				"focus": 0.29621000515148105,
				"gap": 15.411333027905123
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					100.61454412939315,
					0
				]
			]
		},
		{
			"type": "text",
			"version": 203,
			"versionNonce": 1257535506,
			"isDeleted": false,
			"id": "5k9cQOoe",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -90.73399272153279,
			"y": -294.0627712870448,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 165,
			"height": 20,
			"seed": 1256301970,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1669671086935,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "multiple rate limiters",
			"rawText": "multiple rate limiters",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "multiple rate limiters"
		},
		{
			"type": "arrow",
			"version": 2017,
			"versionNonce": 1875147982,
			"isDeleted": false,
			"id": "DxMWk99s3EgBpYweJP400",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -335.9872452052774,
			"y": -201.673501413765,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 100.84616440801284,
			"height": 0,
			"seed": 1040420562,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479686,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "I0x6jboIQt5Z4Q65P81D1",
				"gap": 14.157362488125841,
				"focus": -0.3567574199200635
			},
			"endBinding": {
				"elementId": "acEfDy7Supqen6bv7bCDJ",
				"gap": 14.03506426928044,
				"focus": 0.6932486100525533
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-100.84616440801284,
					0
				]
			]
		},
		{
			"type": "arrow",
			"version": 304,
			"versionNonce": 1006088974,
			"isDeleted": false,
			"id": "JnVKt9TK669Ope64ORuot",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -259.14803333757345,
			"y": -172.52817463835584,
			"strokeColor": "#c92a2a",
			"backgroundColor": "transparent",
			"width": 240.60779788157038,
			"height": 50.242026915789694,
			"seed": 291618638,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1669671479686,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "I0x6jboIQt5Z4Q65P81D1",
				"gap": 11.456155823210906,
				"focus": -0.8210147071321026
			},
			"endBinding": {
				"elementId": "acEfDy7Supqen6bv7bCDJ",
				"gap": 8.33305556454701,
				"focus": 0.6693659805019483
			},
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-132.71352626288524,
					36.63841336869254
				],
				[
					-240.60779788157038,
					-13.603613547097154
				]
			]
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#000000",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "hachure",
		"currentItemStrokeWidth": 1,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 16,
		"currentItemTextAlign": "left",
		"currentItemStrokeSharpness": "sharp",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"currentItemLinearStrokeSharpness": "round",
		"gridSize": null,
		"colorPalette": {}
	},
	"files": {}
}
```
%%