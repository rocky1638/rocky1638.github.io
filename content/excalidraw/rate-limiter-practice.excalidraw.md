---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==

# Text Elements
Requirements:
- Limit the amount of times that a user can access
  a service within a set time period.
    - A way to distinguish between different users.
    - A way to keep track of how many times a user
      has tried to access the service. ^EfQJE3hl

How do we keep track of unique users? ^a16s4GAs

How do we keep track of when a user has logged in? ^R8gq2oW9

Client
- IP address
- MAC Address ^Mtt9XJxH

API ^fzsEiLfa

rate limiter ^AwFSTtKX

request ^hOXpAlab

too many requests
HTTP status ^ewEDBEjj

use a key value-store to track each
time a user logs in. ^vbWw8XdJ

bucket cache ^AdYqfc0i

{ user1: 5, user2: 3, etc. } ^jOStqw6F

check cache for tokens,
decrement if tokens are available ^Ug6XgJ4b

LB ^CyHtlmQV

blacklist DB ^ie8NT5Is

if user is in the blacklist db,
don't allow. ^JnGHevAT

{ user1: time_to_unblacklist, ... } ^jvhGdHmk

tunable
parameters ^zCXxXfnU

rules DB ^WUbhw3UQ

globally distributed
through database
replication (master/slave) ^teW5CVCy

rules cache ^MZiGoFLU

on a timer, increment
all the values in the cache ^W5qUhAbI

request ^6v2GwkPk

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
			"version": 141,
			"versionNonce": 1794475430,
			"isDeleted": false,
			"id": "pFyLon9i622ubActVL5r_",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 610.703125,
			"y": 166.734375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 502.30859375,
			"height": 166.9375,
			"seed": 235746918,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1674593161069,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 308,
			"versionNonce": 223055802,
			"isDeleted": false,
			"id": "EfQJE3hl",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 644.93359375,
			"y": 188.38671875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 422,
			"height": 120,
			"seed": 1210731962,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674593161069,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Requirements:\n- Limit the amount of times that a user can access\n  a service within a set time period.\n    - A way to distinguish between different users.\n    - A way to keep track of how many times a user\n      has tried to access the service.",
			"rawText": "Requirements:\n- Limit the amount of times that a user can access\n  a service within a set time period.\n    - A way to distinguish between different users.\n    - A way to keep track of how many times a user\n      has tried to access the service.",
			"baseline": 114,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Requirements:\n- Limit the amount of times that a user can access\n  a service within a set time period.\n    - A way to distinguish between different users.\n    - A way to keep track of how many times a user\n      has tried to access the service."
		},
		{
			"type": "rectangle",
			"version": 176,
			"versionNonce": 1791090918,
			"isDeleted": false,
			"id": "EeYwO8ymp5WQWfoYwDkDH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 612.08984375,
			"y": 359.109375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 497.8984375,
			"height": 103.61718750000003,
			"seed": 1720666746,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1674593161069,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 85,
			"versionNonce": 58034298,
			"isDeleted": false,
			"id": "a16s4GAs",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 641.98828125,
			"y": 383.46484375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 309,
			"height": 20,
			"seed": 1706944442,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674593161069,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "How do we keep track of unique users?",
			"rawText": "How do we keep track of unique users?",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "How do we keep track of unique users?"
		},
		{
			"type": "text",
			"version": 177,
			"versionNonce": 1054921766,
			"isDeleted": false,
			"id": "R8gq2oW9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 640.6796875,
			"y": 413.9765625,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 416,
			"height": 20,
			"seed": 1051674746,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674593161069,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "How do we keep track of when a user has logged in?",
			"rawText": "How do we keep track of when a user has logged in?",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "How do we keep track of when a user has logged in?"
		},
		{
			"type": "rectangle",
			"version": 461,
			"versionNonce": 1136588346,
			"isDeleted": false,
			"id": "XeOANPyyynA6q9vmQvgxK",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 655.88671875,
			"y": 786.2578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 164,
			"height": 73,
			"seed": 749922746,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Mtt9XJxH"
				},
				{
					"id": "849kUUUd0Tys504eUX2-g",
					"type": "arrow"
				},
				{
					"id": "GW9ALQSaJhbpcfkLZSWj2",
					"type": "arrow"
				}
			],
			"updated": 1674594016215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 466,
			"versionNonce": 343810662,
			"isDeleted": false,
			"id": "Mtt9XJxH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 678.88671875,
			"y": 792.7578125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 118,
			"height": 60,
			"seed": 820093562,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Client\n- IP address\n- MAC Address",
			"rawText": "Client\n- IP address\n- MAC Address",
			"baseline": 54,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XeOANPyyynA6q9vmQvgxK",
			"originalText": "Client\n- IP address\n- MAC Address"
		},
		{
			"type": "rectangle",
			"version": 364,
			"versionNonce": 42718067,
			"isDeleted": false,
			"id": "uwP1E-LeGAz9AGLj1ZEL8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1633.185546875,
			"y": 806.15234375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 115,
			"height": 50,
			"seed": 886703546,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "fzsEiLfa"
				},
				{
					"id": "vDl86q409ERYxs_jHr2ZP",
					"type": "arrow"
				}
			],
			"updated": 1674619678915,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 349,
			"versionNonce": 788087014,
			"isDeleted": false,
			"id": "fzsEiLfa",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1675.185546875,
			"y": 821.15234375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 31,
			"height": 20,
			"seed": 1211016378,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "API",
			"rawText": "API",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "uwP1E-LeGAz9AGLj1ZEL8",
			"originalText": "API"
		},
		{
			"type": "diamond",
			"version": 409,
			"versionNonce": 1160524838,
			"isDeleted": false,
			"id": "dvsr6UlfH-TIic6zxIu2a",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1242.8203125,
			"y": 784.703125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 132,
			"height": 56,
			"seed": 310881638,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "AwFSTtKX"
				},
				{
					"id": "vDl86q409ERYxs_jHr2ZP",
					"type": "arrow"
				},
				{
					"id": "GW9ALQSaJhbpcfkLZSWj2",
					"type": "arrow"
				},
				{
					"id": "kWBhGKJQFtS2Hq_6yovtA",
					"type": "arrow"
				},
				{
					"id": "AwJlkduHcVaPecMT9TwB7",
					"type": "arrow"
				},
				{
					"id": "af8D3ms7LfUYb2L11u-t-",
					"type": "arrow"
				},
				{
					"id": "8ZnYHhXJonAdhMeq7LQea",
					"type": "arrow"
				},
				{
					"id": "78C94XgV_i6GCF6hL2FES",
					"type": "arrow"
				}
			],
			"updated": 1674594016215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 335,
			"versionNonce": 436013370,
			"isDeleted": false,
			"id": "AwFSTtKX",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1263.8203125,
			"y": 802.703125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 90,
			"height": 20,
			"seed": 659112442,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "rate limiter",
			"rawText": "rate limiter",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dvsr6UlfH-TIic6zxIu2a",
			"originalText": "rate limiter"
		},
		{
			"type": "arrow",
			"version": 1732,
			"versionNonce": 736781331,
			"isDeleted": false,
			"id": "849kUUUd0Tys504eUX2-g",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 827.6873461174242,
			"y": 816.4052465573803,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 149.9020333674589,
			"height": 3.0164268689983373,
			"seed": 1446077478,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "6v2GwkPk"
				}
			],
			"updated": 1674619700988,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "XeOANPyyynA6q9vmQvgxK",
				"focus": -0.21388153675664884,
				"gap": 7.800627367424227
			},
			"endBinding": {
				"elementId": "fa_q39CyydB5_xsbZwdsh",
				"focus": -0.13364989795372942,
				"gap": 6.140127052503416
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
					149.9020333674589,
					3.0164268689983373
				]
			]
		},
		{
			"id": "6v2GwkPk",
			"type": "text",
			"x": 872.1383628011537,
			"y": 807.9134599918796,
			"width": 61,
			"height": 20,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1766992445,
			"version": 8,
			"versionNonce": 1552982973,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674619702354,
			"link": null,
			"locked": false,
			"text": "request",
			"rawText": "request",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "849kUUUd0Tys504eUX2-g",
			"originalText": "request"
		},
		{
			"type": "arrow",
			"version": 741,
			"versionNonce": 1799810323,
			"isDeleted": false,
			"id": "vDl86q409ERYxs_jHr2ZP",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1377.8291465017996,
			"y": 815.5214710031769,
			"strokeColor": "#2b8a3e",
			"backgroundColor": "transparent",
			"width": 243.54780662320036,
			"height": 10.583505371386536,
			"seed": 1462860774,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "hOXpAlab"
				}
			],
			"updated": 1674619678916,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 4.122639475385771,
				"focus": -0.006455705695127041
			},
			"endBinding": {
				"elementId": "uwP1E-LeGAz9AGLj1ZEL8",
				"gap": 11.80859375,
				"focus": 0.07402256474500019
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
					243.54780662320036,
					10.583505371386536
				]
			]
		},
		{
			"type": "text",
			"version": 92,
			"versionNonce": 314335142,
			"isDeleted": false,
			"id": "hOXpAlab",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1469.7190629250995,
			"y": 810.8405045579914,
			"strokeColor": "#2b8a3e",
			"backgroundColor": "transparent",
			"width": 61,
			"height": 20,
			"seed": 1553585766,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "request",
			"rawText": "request",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vDl86q409ERYxs_jHr2ZP",
			"originalText": "request"
		},
		{
			"type": "arrow",
			"version": 1171,
			"versionNonce": 45638045,
			"isDeleted": false,
			"id": "GW9ALQSaJhbpcfkLZSWj2",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1262.2094528945222,
			"y": 836.4801663116673,
			"strokeColor": "#c92a2a",
			"backgroundColor": "transparent",
			"width": 509.8566683347145,
			"height": 87.01983368833271,
			"seed": 1233727418,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "ewEDBEjj"
				}
			],
			"updated": 1674619678916,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 14.316285246662844,
				"focus": -0.24068219655719475
			},
			"endBinding": {
				"elementId": "XeOANPyyynA6q9vmQvgxK",
				"gap": 7.265755208333303,
				"focus": 0.7586797782947886
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
					-238.0610153945222,
					87.01983368833271
				],
				[
					-509.8566683347145,
					30.043401396666013
				]
			]
		},
		{
			"type": "text",
			"version": 152,
			"versionNonce": 622382205,
			"isDeleted": false,
			"id": "ewEDBEjj",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 950.1484375,
			"y": 903.5,
			"strokeColor": "#c92a2a",
			"backgroundColor": "transparent",
			"width": 148,
			"height": 40,
			"seed": 734904870,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674619678914,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "too many requests\nHTTP status",
			"rawText": "too many requests\nHTTP status",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GW9ALQSaJhbpcfkLZSWj2",
			"originalText": "too many requests\nHTTP status"
		},
		{
			"type": "rectangle",
			"version": 118,
			"versionNonce": 546446438,
			"isDeleted": false,
			"id": "ZITk6T0vSDzRBfFLFIHD8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1144.0078125,
			"y": 360.7421875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 324.66015625,
			"height": 102.21484375000001,
			"seed": 2142633894,
			"groupIds": [
				"L2uRzWGJ2elHtTx0EcEfq"
			],
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1674593319207,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 124,
			"versionNonce": 2121843962,
			"isDeleted": false,
			"id": "vbWw8XdJ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1163,
			"y": 393.8046875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 295,
			"height": 40,
			"seed": 955628582,
			"groupIds": [
				"L2uRzWGJ2elHtTx0EcEfq"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674593319207,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "use a key value-store to track each\ntime a user logs in.",
			"rawText": "use a key value-store to track each\ntime a user logs in.",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "use a key value-store to track each\ntime a user logs in."
		},
		{
			"type": "ellipse",
			"version": 438,
			"versionNonce": 11257821,
			"isDeleted": false,
			"id": "hjQ2aexG7zgY_SC0fcoAm",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1233.103515625,
			"y": 595.43359375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 138,
			"height": 65,
			"seed": 1539970490,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "AdYqfc0i"
				},
				{
					"id": "kWBhGKJQFtS2Hq_6yovtA",
					"type": "arrow"
				},
				{
					"id": "8ZnYHhXJonAdhMeq7LQea",
					"type": "arrow"
				}
			],
			"updated": 1674619678918,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 324,
			"versionNonce": 1916349990,
			"isDeleted": false,
			"id": "AdYqfc0i",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1250.603515625,
			"y": 617.93359375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103,
			"height": 20,
			"seed": 675277926,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "bucket cache",
			"rawText": "bucket cache",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "hjQ2aexG7zgY_SC0fcoAm",
			"originalText": "bucket cache"
		},
		{
			"type": "arrow",
			"version": 713,
			"versionNonce": 727105405,
			"isDeleted": false,
			"id": "kWBhGKJQFtS2Hq_6yovtA",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1304.443501625256,
			"y": 774.1425390187537,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 0.37796013908337045,
			"height": 102.91496785854815,
			"seed": 1558215290,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674619678918,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 11.431642476065102,
				"focus": -0.064169625445825
			},
			"endBinding": {
				"elementId": "hjQ2aexG7zgY_SC0fcoAm",
				"gap": 10.939987019460492,
				"focus": -0.026305766431767102
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
					-0.37796013908337045,
					-102.91496785854815
				]
			]
		},
		{
			"type": "text",
			"version": 277,
			"versionNonce": 1857313958,
			"isDeleted": false,
			"id": "jOStqw6F",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1200.72265625,
			"y": 562.77734375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 216,
			"height": 20,
			"seed": 955974330,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "{ user1: 5, user2: 3, etc. }",
			"rawText": "{ user1: 5, user2: 3, etc. }",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "{ user1: 5, user2: 3, etc. }"
		},
		{
			"type": "text",
			"version": 259,
			"versionNonce": 1254729914,
			"isDeleted": false,
			"id": "Ug6XgJ4b",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1313.73828125,
			"y": 713.27734375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 267,
			"height": 40,
			"seed": 1576027238,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "check cache for tokens,\ndecrement if tokens are available",
			"rawText": "check cache for tokens,\ndecrement if tokens are available",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "check cache for tokens,\ndecrement if tokens are available"
		},
		{
			"type": "diamond",
			"version": 211,
			"versionNonce": 1586354150,
			"isDeleted": false,
			"id": "fa_q39CyydB5_xsbZwdsh",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 984.19921875,
			"y": 785.9140625,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 93,
			"height": 61,
			"seed": 2000095590,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "CyHtlmQV"
				},
				{
					"id": "849kUUUd0Tys504eUX2-g",
					"type": "arrow"
				},
				{
					"id": "AwJlkduHcVaPecMT9TwB7",
					"type": "arrow"
				}
			],
			"updated": 1674594016215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 197,
			"versionNonce": 2076737914,
			"isDeleted": false,
			"id": "CyHtlmQV",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1019.69921875,
			"y": 806.4140625,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 22,
			"height": 20,
			"seed": 942326630,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "LB",
			"rawText": "LB",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "fa_q39CyydB5_xsbZwdsh",
			"originalText": "LB"
		},
		{
			"type": "arrow",
			"version": 566,
			"versionNonce": 238498973,
			"isDeleted": false,
			"id": "AwJlkduHcVaPecMT9TwB7",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1080.073131534502,
			"y": 813.3006945121735,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 160.6415765732006,
			"height": 0.8709525441013284,
			"seed": 944966074,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674619678919,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "fa_q39CyydB5_xsbZwdsh",
				"gap": 4.237031380642215,
				"focus": -0.11085439930474476
			},
			"endBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 2.5671242444859885,
				"focus": -0.06563468233869608
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
					160.6415765732006,
					0.8709525441013284
				]
			]
		},
		{
			"type": "ellipse",
			"version": 188,
			"versionNonce": 2058305875,
			"isDeleted": false,
			"id": "gRIrJvI-h00A-gGdEoKQL",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1382.45703125,
			"y": 929.5390625,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 151,
			"height": 81,
			"seed": 852968058,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "ie8NT5Is"
				},
				{
					"id": "af8D3ms7LfUYb2L11u-t-",
					"type": "arrow"
				}
			],
			"updated": 1674619678920,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 96,
			"versionNonce": 1413863846,
			"isDeleted": false,
			"id": "ie8NT5Is",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1409.45703125,
			"y": 960.0390625,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 97,
			"height": 20,
			"seed": 295672186,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "blacklist DB",
			"rawText": "blacklist DB",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gRIrJvI-h00A-gGdEoKQL",
			"originalText": "blacklist DB"
		},
		{
			"type": "arrow",
			"version": 354,
			"versionNonce": 1442879741,
			"isDeleted": false,
			"id": "af8D3ms7LfUYb2L11u-t-",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1315.7673147701207,
			"y": 850.440345616269,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 125.71991770788645,
			"height": 67.89470742982223,
			"seed": 10112294,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674619678920,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 11.677058578142598,
				"focus": 0.9566382776034547
			},
			"endBinding": {
				"elementId": "gRIrJvI-h00A-gGdEoKQL",
				"gap": 12.32187250742636,
				"focus": 0.7483745391502031
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
					125.71991770788645,
					67.89470742982223
				]
			]
		},
		{
			"type": "text",
			"version": 186,
			"versionNonce": 474412154,
			"isDeleted": false,
			"id": "JnGHevAT",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1354.578125,
			"y": 1018.58984375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 227,
			"height": 40,
			"seed": 1261416806,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "if user is in the blacklist db,\ndon't allow.",
			"rawText": "if user is in the blacklist db,\ndon't allow.",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "if user is in the blacklist db,\ndon't allow."
		},
		{
			"type": "text",
			"version": 157,
			"versionNonce": 1730947110,
			"isDeleted": false,
			"id": "jvhGdHmk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1348.74609375,
			"y": 1067.03125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 266,
			"height": 20,
			"seed": 1656717626,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "{ user1: time_to_unblacklist, ... }",
			"rawText": "{ user1: time_to_unblacklist, ... }",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "{ user1: time_to_unblacklist, ... }"
		},
		{
			"type": "arrow",
			"version": 345,
			"versionNonce": 338329171,
			"isDeleted": false,
			"id": "8ZnYHhXJonAdhMeq7LQea",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1271.9019919050547,
			"y": 786.6150877145221,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 124.27699190505473,
			"height": 155.8464128258854,
			"seed": 1302830714,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "W5qUhAbI"
				}
			],
			"updated": 1674619692392,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 12.658326411928911,
				"focus": 0.1508972910790124
			},
			"endBinding": {
				"elementId": "hjQ2aexG7zgY_SC0fcoAm",
				"gap": 10.450371098112141,
				"focus": 1.029791474558127
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
					-124.27699190505473,
					-69.16196271452213
				],
				[
					-48.61651704661426,
					-155.8464128258854
				]
			]
		},
		{
			"id": "W5qUhAbI",
			"type": "text",
			"x": 1039.625,
			"y": 697.453125,
			"width": 216,
			"height": 40,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1447693309,
			"version": 5,
			"versionNonce": 856114579,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674619695563,
			"link": null,
			"locked": false,
			"text": "on a timer, increment\nall the values in the cache",
			"rawText": "on a timer, increment\nall the values in the cache",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "8ZnYHhXJonAdhMeq7LQea",
			"originalText": "on a timer, increment\nall the values in the cache"
		},
		{
			"type": "arrow",
			"version": 640,
			"versionNonce": 1830960573,
			"isDeleted": false,
			"id": "78C94XgV_i6GCF6hL2FES",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1289.1649963807095,
			"y": 840.8341570575371,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 191.5680924160165,
			"height": 215.31439859426837,
			"seed": 124734246,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "zCXxXfnU"
				}
			],
			"updated": 1674619678922,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dvsr6UlfH-TIic6zxIu2a",
				"gap": 7.797006425308844,
				"focus": -0.10648920389565689
			},
			"endBinding": {
				"elementId": "vjZ6rldP4pavj0UdcZfhx",
				"gap": 11.019201709241994,
				"focus": -0.3476910908803702
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
					-75.84468388070945,
					79.95881169246286
				],
				[
					-191.5680924160165,
					215.31439859426837
				]
			]
		},
		{
			"type": "text",
			"version": 113,
			"versionNonce": 311920102,
			"isDeleted": false,
			"id": "zCXxXfnU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1168.8203125,
			"y": 900.79296875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 89,
			"height": 40,
			"seed": 322467686,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674595243861,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "tunable\nparameters",
			"rawText": "tunable\nparameters",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "78C94XgV_i6GCF6hL2FES",
			"originalText": "tunable\nparameters"
		},
		{
			"type": "ellipse",
			"version": 363,
			"versionNonce": 1986645690,
			"isDeleted": false,
			"id": "-7iQfDZNu310u9L0hGPbd",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1019.796875,
			"y": 1172.77734375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 151,
			"height": 52,
			"seed": 1265463738,
			"groupIds": [
				"KHcl8WeJwtawarliaTVWr"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "WUbhw3UQ"
				},
				{
					"id": "msUgZcZRgNE7oIitkzRmr",
					"type": "arrow"
				}
			],
			"updated": 1674594016215,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 314,
			"versionNonce": 1282664314,
			"isDeleted": false,
			"id": "WUbhw3UQ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1059.796875,
			"y": 1188.77734375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 71,
			"height": 20,
			"seed": 126439290,
			"groupIds": [
				"KHcl8WeJwtawarliaTVWr"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "rules DB",
			"rawText": "rules DB",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "-7iQfDZNu310u9L0hGPbd",
			"originalText": "rules DB"
		},
		{
			"type": "text",
			"version": 376,
			"versionNonce": 1388045606,
			"isDeleted": false,
			"id": "teW5CVCy",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1003.82421875,
			"y": 1233.046875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 203,
			"height": 60,
			"seed": 1405601254,
			"groupIds": [
				"KHcl8WeJwtawarliaTVWr"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "globally distributed\nthrough database\nreplication (master/slave)",
			"rawText": "globally distributed\nthrough database\nreplication (master/slave)",
			"baseline": 54,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "globally distributed\nthrough database\nreplication (master/slave)"
		},
		{
			"type": "ellipse",
			"version": 167,
			"versionNonce": 2101788211,
			"isDeleted": false,
			"id": "vjZ6rldP4pavj0UdcZfhx",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1021.388671875,
			"y": 1066.91796875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 137,
			"height": 55,
			"seed": 1054789626,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "MZiGoFLU"
				},
				{
					"id": "78C94XgV_i6GCF6hL2FES",
					"type": "arrow"
				},
				{
					"id": "msUgZcZRgNE7oIitkzRmr",
					"type": "arrow"
				}
			],
			"updated": 1674619678922,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 144,
			"versionNonce": 1502629990,
			"isDeleted": false,
			"id": "MZiGoFLU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1044.888671875,
			"y": 1084.41796875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 90,
			"height": 20,
			"seed": 1084306086,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674594016215,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "rules cache",
			"rawText": "rules cache",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "vjZ6rldP4pavj0UdcZfhx",
			"originalText": "rules cache"
		},
		{
			"type": "arrow",
			"version": 320,
			"versionNonce": 1894612509,
			"isDeleted": false,
			"id": "msUgZcZRgNE7oIitkzRmr",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 1092.9796680354352,
			"y": 1130.982176253143,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 1.4521822606859587,
			"height": 34.84150821795333,
			"seed": 2013994150,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674619678922,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "vjZ6rldP4pavj0UdcZfhx",
				"gap": 9.1599861844795,
				"focus": -0.023040380927095858
			},
			"endBinding": {
				"elementId": "-7iQfDZNu310u9L0hGPbd",
				"gap": 6.955472820616981,
				"focus": 0.006734043494214011
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
					1.4521822606859587,
					34.84150821795333
				]
			]
		},
		{
			"type": "text",
			"version": 402,
			"versionNonce": 1449818163,
			"isDeleted": true,
			"id": "sIZYD7RV",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 866.3984375,
			"y": 790.5859375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 61,
			"height": 20,
			"seed": 1882620838,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674619703983,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "request",
			"rawText": "request",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "request"
		},
		{
			"type": "text",
			"version": 332,
			"versionNonce": 1945827133,
			"isDeleted": true,
			"id": "zZOib4bX",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 921.28125,
			"y": 684.12109375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 9,
			"height": 20,
			"seed": 2109523686,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674619691037,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "",
			"rawText": "",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": ""
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
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": -222.62615411931824,
		"scrollY": -122.56818181818187,
		"zoom": {
			"value": 1.1
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"colorPalette": {},
		"previousGridSize": null
	},
	"files": {}
}
```
%%