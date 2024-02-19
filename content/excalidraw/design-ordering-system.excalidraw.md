---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
User flows:
- user has to query product database,
filter, sort, etc.
- product details page, place order
operation. ^lIxVcbf3

client ^5q8lbxQg

Make Order Flow ^ccp47SF1

LB ^RM3HGu4z

products ^Yj4Scw7P

product db ^vHZHmk6n

handles filters,
sorting ^ZN7DeSj9

frequent query cache ^TnS7gdqk

cache frequently
searched items ^uflrCAdC

update on
query success ^pizY3kca

how often are
new products added
to the catalog? ^v1FtGwAz

shards ^FAWvDl3k

shards ^lbVBQYtc

regionally distributed,
different products are
available in different
regions. ^g4zRSREO

View Products Flow ^KdYX45d8

- order has a userid, productid(s), stripe id/credit card id, shipping+billing address.
    - should have statuses, grace period to cancel.
- products should be added to cart.
    - these carts can be saved in a auto-expiring cache, keyed by user session id.
    - for guests, just save the cart in the browser localstorage. ^bQcr5fhj

object storage ^5BQCvpd6

images ^gkZQZsV3

NoSQL ^GFYZ9lGx

a search
index/cluster like elastic
search, that grabs data 
from dbs and indexes it. ^cnlpFfS7

seller ^jsQYo7W6

post new product ^2xayUj21

data indexing
service ^ySk7BQWQ

queue ^W18e25Zf

enqueue data
indexing job ^MnptwUj4

client ^PTSmEjUB

order service ^kW7VnMQw

order info ^biQTVo8B

cart hash/cache ^yvQsG2l7

on cart update ^BWYQ7k4R

update cache ^lQCCrrXr

3rd party payment service ^zl8YRBBA

check CC
details ^pVLuyR1z

orders rdb ^MFu3NAgn

write to db ^uTKtJVZv

users can
query for their
orders from this ^Ut3GkyVi

Requirements:
- user can view products
- user can place order for a product
- keep track of stock of products
- assume there is another service 
down the line that manages order fulfillment ^rTzsiJ3q

Next Steps:
- User profile/management.
- Related items, user flows.
- Promotions, sales.
- Logging. ^ZxuTn3Pz

write-heavy,
could async
order writes to
improve latency, eventual
consistency is fine. ^5jBmR7OH

could be geospatially
partitioned. ^jlMZDsZM

upload to search cluster ^c4COeoBl

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
			"version": 351,
			"versionNonce": 242808669,
			"isDeleted": false,
			"id": "l5U2oIV3YmmhXJwTJ-D0F",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -853.2505263338908,
			"y": -626.7879173922353,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 342,
			"height": 142,
			"seed": 1516873334,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 81,
			"versionNonce": 1798994163,
			"isDeleted": false,
			"id": "z_3SpRb7oEBdW2PqCi1dD",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -847.5071441207795,
			"y": -469.76887201533145,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 339.55047729743455,
			"height": 143.48132894972258,
			"seed": 498654198,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 228,
			"versionNonce": 1450967997,
			"isDeleted": false,
			"id": "lIxVcbf3",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -832.4353283410566,
			"y": -455.9158436139434,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 313,
			"height": 100,
			"seed": 1455032042,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "User flows:\n- user has to query product database,\nfilter, sort, etc.\n- product details page, place order\noperation.",
			"rawText": "User flows:\n- user has to query product database,\nfilter, sort, etc.\n- product details page, place order\noperation.",
			"baseline": 94,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "User flows:\n- user has to query product database,\nfilter, sort, etc.\n- product details page, place order\noperation."
		},
		{
			"type": "rectangle",
			"version": 256,
			"versionNonce": 1644487315,
			"isDeleted": false,
			"id": "L4na1ge0HyuKTJDi7uaaR",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -826.3969542310832,
			"y": -234.81501442216836,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 107,
			"height": 45,
			"seed": 1467824490,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "5q8lbxQg"
				},
				{
					"id": "oI-aITRoTYoB6FZfnl4Zs",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 205,
			"versionNonce": 1461617693,
			"isDeleted": false,
			"id": "5q8lbxQg",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -793.8969542310832,
			"y": -222.31501442216836,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 42,
			"height": 20,
			"seed": 1457273130,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client",
			"rawText": "client",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "L4na1ge0HyuKTJDi7uaaR",
			"originalText": "client"
		},
		{
			"type": "text",
			"version": 88,
			"versionNonce": 319887411,
			"isDeleted": false,
			"id": "KdYX45d8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -823.7190906232224,
			"y": -298.39765131824197,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 261,
			"height": 35,
			"seed": 919458346,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "View Products Flow",
			"rawText": "View Products Flow",
			"baseline": 25,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "View Products Flow"
		},
		{
			"type": "diamond",
			"version": 151,
			"versionNonce": 877787261,
			"isDeleted": false,
			"id": "wEGh_ZuHkMfoFWKwjl4mO",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -606.8137863270576,
			"y": -237.17432594476907,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103,
			"height": 44,
			"seed": 1626077546,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "RM3HGu4z"
				},
				{
					"id": "oI-aITRoTYoB6FZfnl4Zs",
					"type": "arrow"
				},
				{
					"id": "nuJzJY_2UYqKMRLnCZ8YU",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 19,
			"versionNonce": 1816500691,
			"isDeleted": false,
			"id": "RM3HGu4z",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -566.3137863270576,
			"y": -225.17432594476907,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 22,
			"height": 20,
			"seed": 264333738,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "LB",
			"rawText": "LB",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wEGh_ZuHkMfoFWKwjl4mO",
			"originalText": "LB"
		},
		{
			"type": "rectangle",
			"version": 213,
			"versionNonce": 400023773,
			"isDeleted": false,
			"id": "lE8cNT6R4vZBCVnaz61ZF",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -405.990909122573,
			"y": -236.34654986340314,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 107,
			"height": 45,
			"seed": 276304362,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Yj4Scw7P"
				},
				{
					"id": "nuJzJY_2UYqKMRLnCZ8YU",
					"type": "arrow"
				},
				{
					"id": "aT2GwaTPZNm2tcBxskOJY",
					"type": "arrow"
				},
				{
					"id": "3jTqyN-RV6YFVaelCYcWl",
					"type": "arrow"
				},
				{
					"id": "lNACT7dxgQYLZ4D5OyIiV",
					"type": "arrow"
				},
				{
					"id": "QW5H0IJ4BaJ1SVETm72yo",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 106,
			"versionNonce": 1522067315,
			"isDeleted": false,
			"id": "Yj4Scw7P",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -386.990909122573,
			"y": -223.84654986340314,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 69,
			"height": 20,
			"seed": 2029256310,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "products",
			"rawText": "products",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "lE8cNT6R4vZBCVnaz61ZF",
			"originalText": "products"
		},
		{
			"type": "arrow",
			"version": 84,
			"versionNonce": 2000796989,
			"isDeleted": false,
			"id": "oI-aITRoTYoB6FZfnl4Zs",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -709.8167918766258,
			"y": -212.22608754669642,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 98.86122504721857,
			"height": 0.3680984503566833,
			"seed": 1069726570,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "L4na1ge0HyuKTJDi7uaaR",
				"gap": 9.580162354457457,
				"focus": 0.014264759457191137
			},
			"endBinding": {
				"elementId": "wEGh_ZuHkMfoFWKwjl4mO",
				"gap": 4.879699568563932,
				"focus": -0.10786200681097814
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
					98.86122504721857,
					-0.3680984503566833
				]
			]
		},
		{
			"type": "arrow",
			"version": 220,
			"versionNonce": 1689354515,
			"isDeleted": false,
			"id": "nuJzJY_2UYqKMRLnCZ8YU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -501.4927578887643,
			"y": -214.37547155530206,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 87.74632186959877,
			"height": 2.9536613441768225,
			"seed": 1057198058,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "wEGh_ZuHkMfoFWKwjl4mO",
				"gap": 2.454657073185036,
				"focus": -0.04603792930702629
			},
			"endBinding": {
				"elementId": "lE8cNT6R4vZBCVnaz61ZF",
				"gap": 7.755526896592528,
				"focus": -0.18463051390673868
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
					87.74632186959877,
					2.9536613441768225
				]
			]
		},
		{
			"type": "arrow",
			"version": 1674,
			"versionNonce": 435228061,
			"isDeleted": false,
			"id": "aT2GwaTPZNm2tcBxskOJY",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -289.53501591770066,
			"y": -194.43308745440726,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 83.19174766373544,
			"height": 26.39843704085135,
			"seed": 683685110,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "lE8cNT6R4vZBCVnaz61ZF",
				"gap": 9.455893204872325,
				"focus": -0.014374930881569183
			},
			"endBinding": {
				"elementId": "R2yn0Qrt0lAljL6aHLAjH",
				"gap": 14.551517459019209,
				"focus": 0.18359866203643316
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
					83.19174766373544,
					26.39843704085135
				]
			]
		},
		{
			"type": "text",
			"version": 202,
			"versionNonce": 61204147,
			"isDeleted": false,
			"id": "ZN7DeSj9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -299.0484830047396,
			"y": -273.9800220548577,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 118,
			"height": 40,
			"seed": 717390454,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "handles filters,\nsorting",
			"rawText": "handles filters,\nsorting",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "handles filters,\nsorting"
		},
		{
			"type": "ellipse",
			"version": 538,
			"versionNonce": 1595363837,
			"isDeleted": false,
			"id": "aU14UpIQtiGNShHFwedUb",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -344.6512720299156,
			"y": -457.01925505072705,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 114,
			"height": 70,
			"seed": 1875476278,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "TnS7gdqk"
				},
				{
					"id": "3jTqyN-RV6YFVaelCYcWl",
					"type": "arrow"
				},
				{
					"id": "TpSdnbtsUD7jE8rc9m5wh",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 491,
			"versionNonce": 1044158547,
			"isDeleted": false,
			"id": "TnS7gdqk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -334.1512720299156,
			"y": -442.01925505072705,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 93,
			"height": 40,
			"seed": 1145230582,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "frequent \nquery cache",
			"rawText": "frequent query cache",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "aU14UpIQtiGNShHFwedUb",
			"originalText": "frequent query cache"
		},
		{
			"type": "arrow",
			"version": 685,
			"versionNonce": 1136003677,
			"isDeleted": false,
			"id": "3jTqyN-RV6YFVaelCYcWl",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -372.0046766754339,
			"y": -246.549810234804,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 62.38927250795041,
			"height": 135.06415170575832,
			"seed": 1339538090,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "uflrCAdC"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "lE8cNT6R4vZBCVnaz61ZF",
				"gap": 10.203260371400859,
				"focus": -0.541843644348009
			},
			"endBinding": {
				"elementId": "aU14UpIQtiGNShHFwedUb",
				"gap": 7.935988892865922,
				"focus": 0.05569742566880439
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
					62.38927250795041,
					-135.06415170575832
				]
			]
		},
		{
			"type": "text",
			"version": 56,
			"versionNonce": 38540787,
			"isDeleted": false,
			"id": "uflrCAdC",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -388.6960996818301,
			"y": -353.7436913999518,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 131,
			"height": 40,
			"seed": 837539190,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "cache frequently\nsearched items",
			"rawText": "cache frequently\nsearched items",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "3jTqyN-RV6YFVaelCYcWl",
			"originalText": "cache frequently\nsearched items"
		},
		{
			"type": "arrow",
			"version": 1684,
			"versionNonce": 681490109,
			"isDeleted": false,
			"id": "TpSdnbtsUD7jE8rc9m5wh",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -33.10908477790787,
			"y": -490.54251982521527,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 188.0961886362679,
			"height": 61.43123862400256,
			"seed": 447592246,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "pizY3kca"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "COzuY9ldB80YNcewk2XlY",
				"focus": 0.21376536688636608,
				"gap": 14.944858453873195
			},
			"endBinding": {
				"elementId": "aU14UpIQtiGNShHFwedUb",
				"gap": 10.276456612607625,
				"focus": 0.2830231088292042
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
					-95.84299149665168,
					36.56478614128065
				],
				[
					-188.0961886362679,
					61.43123862400256
				]
			]
		},
		{
			"type": "text",
			"version": 103,
			"versionNonce": 1054531475,
			"isDeleted": false,
			"id": "pizY3kca",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -244.01402719230697,
			"y": -356.47423786039815,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 110,
			"height": 40,
			"seed": 10837814,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "update on\nquery success",
			"rawText": "update on\nquery success",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TpSdnbtsUD7jE8rc9m5wh",
			"originalText": "update on\nquery success"
		},
		{
			"type": "text",
			"version": 125,
			"versionNonce": 1483921181,
			"isDeleted": false,
			"id": "v1FtGwAz",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -364.79485457043563,
			"y": -527.8981558631817,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 156,
			"height": 60,
			"seed": 1397031978,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "how often are\nnew products added\nto the catalog?",
			"rawText": "how often are\nnew products added\nto the catalog?",
			"baseline": 54,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "how often are\nnew products added\nto the catalog?"
		},
		{
			"type": "text",
			"version": 257,
			"versionNonce": 1042249011,
			"isDeleted": false,
			"id": "ccp47SF1",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -828.1052112491175,
			"y": 62.5041440827444,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 230,
			"height": 35,
			"seed": 213516074,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 28,
			"fontFamily": 1,
			"text": "Make Order Flow",
			"rawText": "Make Order Flow",
			"baseline": 25,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Make Order Flow"
		},
		{
			"type": "text",
			"version": 524,
			"versionNonce": 1302588285,
			"isDeleted": false,
			"id": "bQcr5fhj",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -830.091156165836,
			"y": 109.52659077728703,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 657,
			"height": 100,
			"seed": 1845980854,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "- order has a userid, productid(s), stripe id/credit card id, shipping+billing address.\n    - should have statuses, grace period to cancel.\n- products should be added to cart.\n    - these carts can be saved in a auto-expiring cache, keyed by user session id.\n    - for guests, just save the cart in the browser localstorage.",
			"rawText": "- order has a userid, productid(s), stripe id/credit card id, shipping+billing address.\n    - should have statuses, grace period to cancel.\n- products should be added to cart.\n    - these carts can be saved in a auto-expiring cache, keyed by user session id.\n    - for guests, just save the cart in the browser localstorage.",
			"baseline": 94,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- order has a userid, productid(s), stripe id/credit card id, shipping+billing address.\n    - should have statuses, grace period to cancel.\n- products should be added to cart.\n    - these carts can be saved in a auto-expiring cache, keyed by user session id.\n    - for guests, just save the cart in the browser localstorage."
		},
		{
			"type": "ellipse",
			"version": 195,
			"versionNonce": 1065375443,
			"isDeleted": false,
			"id": "QayOWwY7bEbHde9tX803G",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 210.81105405569252,
			"y": -107.04892338859577,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 143,
			"height": 71,
			"seed": 1208043882,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "5BQCvpd6"
				},
				{
					"id": "BjdWQwu8rAKkz5V3biJ0n",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 141,
			"versionNonce": 947090397,
			"isDeleted": false,
			"id": "5BQCvpd6",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 223.31105405569252,
			"y": -81.54892338859577,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 118,
			"height": 20,
			"seed": 352407274,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "object storage",
			"rawText": "object storage",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QayOWwY7bEbHde9tX803G",
			"originalText": "object storage"
		},
		{
			"type": "arrow",
			"version": 1300,
			"versionNonce": 1368654963,
			"isDeleted": false,
			"id": "BjdWQwu8rAKkz5V3biJ0n",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 46.066473677662955,
			"y": -154.85078930004394,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 182.78497885075814,
			"height": 48.95981165356983,
			"seed": 664827190,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "gkZQZsV3"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "R2yn0Qrt0lAljL6aHLAjH",
				"focus": -0.5784801600185744,
				"gap": 18.24208747026165
			},
			"endBinding": {
				"elementId": "QayOWwY7bEbHde9tX803G",
				"gap": 9.998415424745389,
				"focus": 0.08875249996691872
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
					100.43183141404732,
					3.3296548501137124
				],
				[
					182.78497885075814,
					48.95981165356983
				]
			]
		},
		{
			"type": "text",
			"version": 13,
			"versionNonce": 1156771901,
			"isDeleted": false,
			"id": "gkZQZsV3",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 92.04798662889937,
			"y": -235.83207805621976,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 51,
			"height": 20,
			"seed": 833527722,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "images",
			"rawText": "images",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BjdWQwu8rAKkz5V3biJ0n",
			"originalText": "images"
		},
		{
			"type": "ellipse",
			"version": 897,
			"versionNonce": 1814101523,
			"isDeleted": false,
			"id": "wRp1HVPOFrpi1n60LNvuq",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -198.775804850103,
			"y": -160.6277502781146,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 109,
			"height": 44,
			"seed": 1411090858,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "vHZHmk6n"
				},
				{
					"id": "aT2GwaTPZNm2tcBxskOJY",
					"type": "arrow"
				},
				{
					"id": "TpSdnbtsUD7jE8rc9m5wh",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 842,
			"versionNonce": 553902237,
			"isDeleted": false,
			"id": "vHZHmk6n",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -186.775804850103,
			"y": -148.6277502781146,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 85,
			"height": 20,
			"seed": 151512106,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "product db",
			"rawText": "product db",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wRp1HVPOFrpi1n60LNvuq",
			"originalText": "product db"
		},
		{
			"type": "ellipse",
			"version": 932,
			"versionNonce": 1243464627,
			"isDeleted": false,
			"id": "sABDQeIxooqGCgVhEoRTQ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -132.26993158377172,
			"y": -108.64437509235421,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 96,
			"height": 52,
			"seed": 2121016810,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "lbVBQYtc"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 888,
			"versionNonce": 1113048317,
			"isDeleted": false,
			"id": "lbVBQYtc",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -110.76993158377172,
			"y": -92.64437509235421,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 53,
			"height": 20,
			"seed": 2055461034,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "shards",
			"rawText": "shards",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "sABDQeIxooqGCgVhEoRTQ",
			"originalText": "shards"
		},
		{
			"type": "ellipse",
			"version": 1001,
			"versionNonce": 61920595,
			"isDeleted": false,
			"id": "b863xXFxF6QRP0HfegVHL",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -78.11902287765201,
			"y": -167.8523493328604,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 96,
			"height": 52,
			"seed": 14758454,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FAWvDl3k"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 958,
			"versionNonce": 1819286877,
			"isDeleted": false,
			"id": "FAWvDl3k",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -56.619022877652014,
			"y": -151.8523493328604,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 53,
			"height": 20,
			"seed": 239963178,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "shards",
			"rawText": "shards",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "b863xXFxF6QRP0HfegVHL",
			"originalText": "shards"
		},
		{
			"type": "ellipse",
			"version": 946,
			"versionNonce": 1748022003,
			"isDeleted": false,
			"id": "R2yn0Qrt0lAljL6aHLAjH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -218.84296439916625,
			"y": -191.71169606170776,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 260.01039625995304,
			"height": 154.0050895190558,
			"seed": 372082410,
			"groupIds": [
				"T8HT6KWefDHhdDV5WPBg8",
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "TpSdnbtsUD7jE8rc9m5wh",
					"type": "arrow"
				},
				{
					"id": "aT2GwaTPZNm2tcBxskOJY",
					"type": "arrow"
				},
				{
					"id": "BjdWQwu8rAKkz5V3biJ0n",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 890,
			"versionNonce": 1990093245,
			"isDeleted": false,
			"id": "g4zRSREO",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -170.54590350153683,
			"y": -29.908281735473565,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 179,
			"height": 80,
			"seed": 1339188202,
			"groupIds": [
				"vlt6SbhwxmJ4B8HOqc_Gn",
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "regionally distributed,\ndifferent products are\navailable in different\nregions.",
			"rawText": "regionally distributed,\ndifferent products are\navailable in different\nregions.",
			"baseline": 74,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "regionally distributed,\ndifferent products are\navailable in different\nregions."
		},
		{
			"type": "text",
			"version": 826,
			"versionNonce": 405003411,
			"isDeleted": false,
			"id": "GFYZ9lGx",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 28.858000386366825,
			"y": -71.53241194176576,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 51,
			"height": 20,
			"seed": 113597686,
			"groupIds": [
				"2GVsOI8a10L9Nio-JbvPJ"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655640,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "NoSQL",
			"rawText": "NoSQL",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "NoSQL"
		},
		{
			"type": "rectangle",
			"version": 104,
			"versionNonce": 1376004637,
			"isDeleted": false,
			"id": "-HI3vzJfRWw9cOjF-8vgJ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -829.8689683587289,
			"y": -105.31238010349267,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 110,
			"height": 46,
			"seed": 838383542,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "jsQYo7W6"
				},
				{
					"id": "lNACT7dxgQYLZ4D5OyIiV",
					"type": "arrow"
				}
			],
			"updated": 1674854655640,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 36,
			"versionNonce": 1598083635,
			"isDeleted": false,
			"id": "jsQYo7W6",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -795.8689683587289,
			"y": -92.31238010349267,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 42,
			"height": 20,
			"seed": 178210934,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "seller",
			"rawText": "seller",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "-HI3vzJfRWw9cOjF-8vgJ",
			"originalText": "seller"
		},
		{
			"type": "arrow",
			"version": 1463,
			"versionNonce": 1335025277,
			"isDeleted": false,
			"id": "lNACT7dxgQYLZ4D5OyIiV",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -712.2906571352207,
			"y": -81.13495181275754,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 357.0600944968012,
			"height": 101.59477054539714,
			"seed": 1610876854,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "2xayUj21"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "-HI3vzJfRWw9cOjF-8vgJ",
				"gap": 7.578311223508194,
				"focus": 0.2099385999543487
			},
			"endBinding": {
				"elementId": "lE8cNT6R4vZBCVnaz61ZF",
				"gap": 8.616827505248466,
				"focus": -0.4518666162743728
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
					249.47062274311156,
					-17.848851721593533
				],
				[
					357.0600944968012,
					-101.59477054539714
				]
			]
		},
		{
			"type": "text",
			"version": 37,
			"versionNonce": 1315836883,
			"isDeleted": false,
			"id": "2xayUj21",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -531.3200343921092,
			"y": -108.98380353435107,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 136,
			"height": 20,
			"seed": 1969319210,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "post new product",
			"rawText": "post new product",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "lNACT7dxgQYLZ4D5OyIiV",
			"originalText": "post new product"
		},
		{
			"type": "text",
			"version": 290,
			"versionNonce": 638322397,
			"isDeleted": false,
			"id": "cnlpFfS7",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 11.822518191876668,
			"y": -565.1046952120204,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 189,
			"height": 76,
			"seed": 2094972214,
			"groupIds": [
				"4n0cSnrdyAHZAN3lAH8dl"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 14.719709437602875,
			"fontFamily": 1,
			"text": "a search\nindex/cluster like elastic\nsearch, that grabs data \nfrom dbs and indexes it.",
			"rawText": "a search\nindex/cluster like elastic\nsearch, that grabs data \nfrom dbs and indexes it.",
			"baseline": 70,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "a search\nindex/cluster like elastic\nsearch, that grabs data \nfrom dbs and indexes it."
		},
		{
			"type": "ellipse",
			"version": 311,
			"versionNonce": 365044083,
			"isDeleted": false,
			"id": "COzuY9ldB80YNcewk2XlY",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -28.81195671086425,
			"y": -594.6923275366235,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 259.6910206953436,
			"height": 143.1638677282053,
			"seed": 1513373494,
			"groupIds": [
				"4n0cSnrdyAHZAN3lAH8dl"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "TpSdnbtsUD7jE8rc9m5wh",
					"type": "arrow"
				},
				{
					"id": "QLuzCIds3T_khYl4S8FDl",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 160,
			"versionNonce": 939598653,
			"isDeleted": false,
			"id": "QmhbxBOVc_zfNCFibrabX",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 236.05360882986963,
			"y": -355.72406605457394,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 143,
			"height": 58,
			"seed": 170771318,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "ySk7BQWQ"
				},
				{
					"id": "E5xXpaUDlnMZb08KqauKA",
					"type": "arrow"
				},
				{
					"id": "QLuzCIds3T_khYl4S8FDl",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 155,
			"versionNonce": 511933203,
			"isDeleted": false,
			"id": "ySk7BQWQ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 255.05360882986963,
			"y": -346.72406605457394,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 105,
			"height": 40,
			"seed": 2127670710,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "data indexing\nservice",
			"rawText": "data indexing\nservice",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QmhbxBOVc_zfNCFibrabX",
			"originalText": "data indexing\nservice"
		},
		{
			"type": "diamond",
			"version": 140,
			"versionNonce": 433304477,
			"isDeleted": false,
			"id": "oRfWERQmTVrqCH6pPmU9J",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -48.52542966367986,
			"y": -358.3110107025286,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 190,
			"height": 57,
			"seed": 1594718646,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "W18e25Zf"
				},
				{
					"id": "E5xXpaUDlnMZb08KqauKA",
					"type": "arrow"
				},
				{
					"id": "QW5H0IJ4BaJ1SVETm72yo",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 97,
			"versionNonce": 1697161395,
			"isDeleted": false,
			"id": "W18e25Zf",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 23.97457033632014,
			"y": -339.8110107025286,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 45,
			"height": 20,
			"seed": 1586487658,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "queue",
			"rawText": "queue",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "oRfWERQmTVrqCH6pPmU9J",
			"originalText": "queue"
		},
		{
			"type": "arrow",
			"version": 163,
			"versionNonce": 1471494141,
			"isDeleted": false,
			"id": "E5xXpaUDlnMZb08KqauKA",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 142.42233918362416,
			"y": -330.12996871242956,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 90.93246206764485,
			"height": 2.022003350816533,
			"seed": 455471082,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "oRfWERQmTVrqCH6pPmU9J",
				"gap": 1,
				"focus": 0.06367330700238566
			},
			"endBinding": {
				"elementId": "QmhbxBOVc_zfNCFibrabX",
				"gap": 2.698807578600622,
				"focus": 0.2313775192440389
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
					90.93246206764485,
					-2.022003350816533
				]
			]
		},
		{
			"type": "arrow",
			"version": 285,
			"versionNonce": 324538963,
			"isDeleted": false,
			"id": "QW5H0IJ4BaJ1SVETm72yo",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -288.6567639584671,
			"y": -215.26566036140284,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 272.0995005061683,
			"height": 91.58667181944534,
			"seed": 349033706,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "MnptwUj4"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "lE8cNT6R4vZBCVnaz61ZF",
				"gap": 10.334145164105905,
				"focus": 0.12659686372923207
			},
			"endBinding": {
				"elementId": "oRfWERQmTVrqCH6pPmU9J",
				"gap": 12.80444079573395,
				"focus": 0.43239055235800383
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
					198.73067215706317,
					-14.86282949855891
				],
				[
					272.0995005061683,
					-91.58667181944534
				]
			]
		},
		{
			"type": "text",
			"version": 67,
			"versionNonce": 2074554461,
			"isDeleted": false,
			"id": "MnptwUj4",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -200.4652706673869,
			"y": -256.13257317108474,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 109,
			"height": 40,
			"seed": 1127294314,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "enqueue data\nindexing job",
			"rawText": "enqueue data\nindexing job",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QW5H0IJ4BaJ1SVETm72yo",
			"originalText": "enqueue data\nindexing job"
		},
		{
			"type": "rectangle",
			"version": 204,
			"versionNonce": 1508397043,
			"isDeleted": false,
			"id": "JUgqH0JP1M60aaiWW3j-U",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -820.6243998545433,
			"y": 257.2067445652565,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103,
			"height": 41,
			"seed": 1029783990,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "PTSmEjUB"
				},
				{
					"id": "b8PyFWdusrHsaaGLf_Dts",
					"type": "arrow"
				},
				{
					"id": "YWwmzip2Ctz1S1oCD2lzS",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 147,
			"versionNonce": 1400577213,
			"isDeleted": false,
			"id": "PTSmEjUB",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -790.1243998545433,
			"y": 267.7067445652565,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 42,
			"height": 20,
			"seed": 1323788406,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client",
			"rawText": "client",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "JUgqH0JP1M60aaiWW3j-U",
			"originalText": "client"
		},
		{
			"type": "rectangle",
			"version": 342,
			"versionNonce": 182442387,
			"isDeleted": false,
			"id": "V4zgy11J_iw3K4fYqT4w9",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -523.6636773708105,
			"y": 259.91556280076014,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 117,
			"height": 38,
			"seed": 415014314,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "kW7VnMQw"
				},
				{
					"id": "b8PyFWdusrHsaaGLf_Dts",
					"type": "arrow"
				},
				{
					"id": "YWwmzip2Ctz1S1oCD2lzS",
					"type": "arrow"
				},
				{
					"id": "ItBFXVZ_GSxZHQ6IwSBk-",
					"type": "arrow"
				},
				{
					"id": "WE5dSgEollDPVRnPLWdO4",
					"type": "arrow"
				},
				{
					"id": "RGJ8cZrVQ356kVHlLYvge",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 309,
			"versionNonce": 1993506077,
			"isDeleted": false,
			"id": "kW7VnMQw",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -516.1636773708105,
			"y": 268.91556280076014,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 102,
			"height": 20,
			"seed": 2138234154,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "order service",
			"rawText": "order service",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "V4zgy11J_iw3K4fYqT4w9",
			"originalText": "order service"
		},
		{
			"type": "arrow",
			"version": 648,
			"versionNonce": 1937059635,
			"isDeleted": false,
			"id": "b8PyFWdusrHsaaGLf_Dts",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -708.7888091848164,
			"y": 279.69870301094375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 176.69113688640414,
			"height": 2.266217991880353,
			"seed": 1936306806,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "biQTVo8B"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "JUgqH0JP1M60aaiWW3j-U",
				"gap": 8.835590669726912,
				"focus": 0.1307063065152773
			},
			"endBinding": {
				"elementId": "V4zgy11J_iw3K4fYqT4w9",
				"gap": 8.433994927601702,
				"focus": 0.1185583540779958
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
					176.69113688640414,
					-2.266217991880353
				]
			]
		},
		{
			"type": "text",
			"version": 128,
			"versionNonce": 220123517,
			"isDeleted": false,
			"id": "biQTVo8B",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -692.9060396421262,
			"y": 271.3575732381618,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 77,
			"height": 20,
			"seed": 841552938,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "order info",
			"rawText": "order info",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "b8PyFWdusrHsaaGLf_Dts",
			"originalText": "order info"
		},
		{
			"type": "ellipse",
			"version": 356,
			"versionNonce": 1980682451,
			"isDeleted": false,
			"id": "tKEHq2xJzIbbDGg5KwhIa",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -767.1136530539749,
			"y": 385.6901634358236,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 139,
			"height": 51,
			"seed": 1980077686,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "yvQsG2l7"
				},
				{
					"id": "ItBFXVZ_GSxZHQ6IwSBk-",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 338,
			"versionNonce": 1403099613,
			"isDeleted": false,
			"id": "yvQsG2l7",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -741.6136530539749,
			"y": 391.1901634358236,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 88,
			"height": 40,
			"seed": 154168746,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "cart \nhash/cache",
			"rawText": "cart hash/cache",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tKEHq2xJzIbbDGg5KwhIa",
			"originalText": "cart hash/cache"
		},
		{
			"type": "arrow",
			"version": 569,
			"versionNonce": 1682128499,
			"isDeleted": false,
			"id": "YWwmzip2Ctz1S1oCD2lzS",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -761.9444901959378,
			"y": 307.7816271914632,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 238.91381670781266,
			"height": 19.78399917085619,
			"seed": 118005802,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "BWYQ7k4R"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "JUgqH0JP1M60aaiWW3j-U",
				"gap": 9.574882626206715,
				"focus": 0.9961906991555491
			},
			"endBinding": {
				"elementId": "V4zgy11J_iw3K4fYqT4w9",
				"gap": 11.775580747922561,
				"focus": -0.7949826861042134
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
					119.86380194009234,
					19.78399917085619
				],
				[
					238.91381670781266,
					1.909516357219502
				]
			]
		},
		{
			"type": "text",
			"version": 112,
			"versionNonce": 1668044349,
			"isDeleted": false,
			"id": "BWYQ7k4R",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -703.5806882558454,
			"y": 317.5656263623194,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 123,
			"height": 20,
			"seed": 1467575338,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "on cart update",
			"rawText": "on cart update",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YWwmzip2Ctz1S1oCD2lzS",
			"originalText": "on cart update"
		},
		{
			"type": "arrow",
			"version": 885,
			"versionNonce": 416872467,
			"isDeleted": false,
			"id": "ItBFXVZ_GSxZHQ6IwSBk-",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -501.96054648793864,
			"y": 311.2184701484698,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 119.8622495667135,
			"height": 83.89828836418974,
			"seed": 2036957814,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "lQCCrrXr"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "V4zgy11J_iw3K4fYqT4w9",
				"gap": 13.302907347709663,
				"focus": 0.2905848190339397
			},
			"endBinding": {
				"elementId": "tKEHq2xJzIbbDGg5KwhIa",
				"gap": 13.628444116634142,
				"focus": 0.419505342537682
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
					-21.89993360508555,
					41.84048113733172
				],
				[
					-119.8622495667135,
					83.89828836418974
				]
			]
		},
		{
			"type": "text",
			"version": 109,
			"versionNonce": 929072797,
			"isDeleted": false,
			"id": "lQCCrrXr",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -570.6531436939655,
			"y": 333.2935052173368,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 107,
			"height": 20,
			"seed": 264618294,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "update cache",
			"rawText": "update cache",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ItBFXVZ_GSxZHQ6IwSBk-",
			"originalText": "update cache"
		},
		{
			"type": "rectangle",
			"version": 222,
			"versionNonce": 1371962803,
			"isDeleted": false,
			"id": "g0djuBxIACFSq1CjvoOWO",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -172.1182513933781,
			"y": 252.27429348537692,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 142,
			"height": 57,
			"seed": 986741622,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "zl8YRBBA"
				},
				{
					"id": "WE5dSgEollDPVRnPLWdO4",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 225,
			"versionNonce": 1915726589,
			"isDeleted": false,
			"id": "zl8YRBBA",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -162.6182513933781,
			"y": 260.7742934853769,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 123,
			"height": 40,
			"seed": 1274191274,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "3rd party \npayment service",
			"rawText": "3rd party payment service",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "g0djuBxIACFSq1CjvoOWO",
			"originalText": "3rd party payment service"
		},
		{
			"type": "arrow",
			"version": 220,
			"versionNonce": 1244811091,
			"isDeleted": false,
			"id": "WE5dSgEollDPVRnPLWdO4",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -395.18278637657147,
			"y": 279.2325702506159,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 212.30874316695613,
			"height": 0.9646721951756376,
			"seed": 1990182262,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "pVLuyR1z"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "V4zgy11J_iw3K4fYqT4w9",
				"gap": 11.480890994239076,
				"focus": -0.000050159103535095616
			},
			"endBinding": {
				"elementId": "g0djuBxIACFSq1CjvoOWO",
				"gap": 10.755791816237263,
				"focus": 0.007132434536533524
			},
			"lastCommittedPoint": null,
			"startArrowhead": "arrow",
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					212.30874316695613,
					0.9646721951756376
				]
			]
		},
		{
			"type": "text",
			"version": 37,
			"versionNonce": 1683702621,
			"isDeleted": false,
			"id": "pVLuyR1z",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -389.9804185067896,
			"y": 258.914609777793,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 70,
			"height": 40,
			"seed": 198850090,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "check CC\ndetails",
			"rawText": "check CC\ndetails",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "WE5dSgEollDPVRnPLWdO4",
			"originalText": "check CC\ndetails"
		},
		{
			"type": "ellipse",
			"version": 145,
			"versionNonce": 343076083,
			"isDeleted": false,
			"id": "dF70dTvOwOqvQpAHM9WXT",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -333.35771388087073,
			"y": 396.9742672106674,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 118,
			"height": 54,
			"seed": 1862148586,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "MFu3NAgn"
				},
				{
					"id": "RGJ8cZrVQ356kVHlLYvge",
					"type": "arrow"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 108,
			"versionNonce": 1379192765,
			"isDeleted": false,
			"id": "MFu3NAgn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -315.35771388087073,
			"y": 413.9742672106674,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 82,
			"height": 20,
			"seed": 2041028854,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "orders rdb",
			"rawText": "orders rdb",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dF70dTvOwOqvQpAHM9WXT",
			"originalText": "orders rdb"
		},
		{
			"type": "arrow",
			"version": 151,
			"versionNonce": 873387667,
			"isDeleted": false,
			"id": "RGJ8cZrVQ356kVHlLYvge",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -438.6468327766088,
			"y": 304.5040512964365,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 134.23777151988168,
			"height": 87.19002110456813,
			"seed": 1520523190,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "uTKtJVZv"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "V4zgy11J_iw3K4fYqT4w9",
				"gap": 6.5884884956763585,
				"focus": 0.14676745263184174
			},
			"endBinding": {
				"elementId": "dF70dTvOwOqvQpAHM9WXT",
				"gap": 8.986604252867217,
				"focus": 0.27222283831595906
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
					134.23777151988168,
					87.19002110456813
				]
			]
		},
		{
			"type": "text",
			"version": 21,
			"versionNonce": 2044579869,
			"isDeleted": false,
			"id": "uTKtJVZv",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -416.5289298890779,
			"y": 338.0990997799879,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 90,
			"height": 20,
			"seed": 725778090,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "write to db",
			"rawText": "write to db",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RGJ8cZrVQ356kVHlLYvge",
			"originalText": "write to db"
		},
		{
			"type": "text",
			"version": 108,
			"versionNonce": 2008845363,
			"isDeleted": false,
			"id": "Ut3GkyVi",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -328.23757784620113,
			"y": 455.0231313345163,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 129,
			"height": 60,
			"seed": 444504246,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "users can\nquery for their\norders from this",
			"rawText": "users can\nquery for their\norders from this",
			"baseline": 54,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "users can\nquery for their\norders from this"
		},
		{
			"type": "text",
			"version": 231,
			"versionNonce": 1497875581,
			"isDeleted": false,
			"id": "rTzsiJ3q",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -831.4976623417059,
			"y": -608.7280623024855,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 307,
			"height": 102,
			"seed": 1730699370,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 13.978561207525122,
			"fontFamily": 1,
			"text": "Requirements:\n- user can view products\n- user can place order for a product\n- keep track of stock of products\n- assume there is another service \ndown the line that manages order fulfillment",
			"rawText": "Requirements:\n- user can view products\n- user can place order for a product\n- keep track of stock of products\n- assume there is another service \ndown the line that manages order fulfillment",
			"baseline": 97,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Requirements:\n- user can view products\n- user can place order for a product\n- keep track of stock of products\n- assume there is another service \ndown the line that manages order fulfillment"
		},
		{
			"type": "text",
			"version": 259,
			"versionNonce": 325225939,
			"isDeleted": false,
			"id": "ZxuTn3Pz",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 110.13526111242231,
			"y": 108.52486747183923,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 221,
			"height": 100,
			"seed": 628505974,
			"groupIds": [
				"ZP3BQkR_xoscbJwqh0aHI"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Next Steps:\n- User profile/management.\n- Related items, user flows.\n- Promotions, sales.\n- Logging.",
			"rawText": "Next Steps:\n- User profile/management.\n- Related items, user flows.\n- Promotions, sales.\n- Logging.",
			"baseline": 94,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Next Steps:\n- User profile/management.\n- Related items, user flows.\n- Promotions, sales.\n- Logging."
		},
		{
			"type": "rectangle",
			"version": 171,
			"versionNonce": 875834589,
			"isDeleted": false,
			"id": "hAxI_K7YuWI2iuJkTGZ0J",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 90.28736110040973,
			"y": 90.93147497482471,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 260.3905541383733,
			"height": 132.8542205388759,
			"seed": 82442294,
			"groupIds": [
				"ZP3BQkR_xoscbJwqh0aHI"
			],
			"roundness": {
				"type": 3
			},
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 299,
			"versionNonce": 2048351091,
			"isDeleted": false,
			"id": "5jBmR7OH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -197.91118224113518,
			"y": 367.45923236441695,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 197,
			"height": 100,
			"seed": 271764342,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "write-heavy,\ncould async\norder writes to\nimprove latency, eventual\nconsistency is fine.",
			"rawText": "write-heavy,\ncould async\norder writes to\nimprove latency, eventual\nconsistency is fine.",
			"baseline": 94,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "write-heavy,\ncould async\norder writes to\nimprove latency, eventual\nconsistency is fine."
		},
		{
			"type": "text",
			"version": 94,
			"versionNonce": 1513392445,
			"isDeleted": false,
			"id": "jlMZDsZM",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -776.3156988428211,
			"y": 446.07903475908927,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 164,
			"height": 40,
			"seed": 842911594,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "could be geospatially\npartitioned.",
			"rawText": "could be geospatially\npartitioned.",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "could be geospatially\npartitioned."
		},
		{
			"type": "arrow",
			"version": 79,
			"versionNonce": 2015458579,
			"isDeleted": false,
			"id": "QLuzCIds3T_khYl4S8FDl",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 305.61526443487,
			"y": -366.06877799654274,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 97.90860740701723,
			"height": 105.23422280126988,
			"seed": 70682707,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "c4COeoBl"
				}
			],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "QmhbxBOVc_zfNCFibrabX",
				"gap": 10.344711941968797,
				"focus": 0.35203616049356073
			},
			"endBinding": {
				"elementId": "COzuY9ldB80YNcewk2XlY",
				"gap": 9.192680532332915,
				"focus": -0.40068902620241786
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
					-97.90860740701723,
					-105.23422280126988
				]
			]
		},
		{
			"type": "text",
			"version": 50,
			"versionNonce": 749361565,
			"isDeleted": false,
			"id": "c4COeoBl",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 157.67214021895836,
			"y": -428.5391269581615,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 198,
			"height": 20,
			"seed": 1448660957,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "upload to search cluster",
			"rawText": "upload to search cluster",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "QLuzCIds3T_khYl4S8FDl",
			"originalText": "upload to search cluster"
		},
		{
			"id": "O1VTy-BZJsOajNfrt1Pox",
			"type": "freedraw",
			"x": 567.4442445509696,
			"y": -565.1117647628389,
			"width": 269.93370211978913,
			"height": 199.40201328005293,
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
			"seed": 1565281373,
			"version": 157,
			"versionNonce": 1502310163,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674854661083,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0.7060834933329261,
					-0.47610201264740226
				],
				[
					9.457484047842854,
					-3.845128966550419
				],
				[
					30.115469681356444,
					-9.352580214547743
				],
				[
					42.022054760360106,
					-12.156740373784373
				],
				[
					51.564268827402884,
					-13.520490206621844
				],
				[
					70.6446621986695,
					-14.22253893713571
				],
				[
					76.24087822868569,
					-13.601185463002707
				],
				[
					79.47272324674123,
					-11.987280335384526
				],
				[
					82.55931680331128,
					-6.790505824453703
				],
				[
					84.43951627698652,
					5.192739748111762
				],
				[
					85.13753024468133,
					17.09932482711531
				],
				[
					83.51555559142503,
					23.563014863226385
				],
				[
					82.03883239965444,
					26.0201854200252
				],
				[
					79.29922844552243,
					29.243960912442617
				],
				[
					79.06117743919867,
					29.71602816227096
				],
				[
					79.29519368270326,
					29.239926149623557
				],
				[
					81.26012317557843,
					27.270961893929325
				],
				[
					84.49196819363397,
					25.65302200349197
				],
				[
					94.89762150395268,
					20.75481994117058
				],
				[
					101.28465104650195,
					20.11329265294239
				],
				[
					112.47708310653434,
					18.866550941857213
				],
				[
					118.07329913655076,
					19.48790441599033
				],
				[
					126.48981437707971,
					24.898521356330434
				],
				[
					129.49571267726878,
					29.106778976595024
				],
				[
					133.51433644503823,
					36.54688161491515
				],
				[
					134.0025427461428,
					39.004052171713965
				],
				[
					133.01806061829552,
					45.48388125910117
				],
				[
					130.0081275552875,
					49.69213887936576
				],
				[
					124.60961490340446,
					54.0012655701064
				],
				[
					113.09843658066734,
					59.76290687570349
				],
				[
					112.19464970920126,
					60.06147932431293
				],
				[
					111.9565987028775,
					60.06147932431293
				],
				[
					112.42866595270584,
					59.82342831798928
				],
				[
					114.88583650950454,
					59.33118725406564
				],
				[
					118.90849504009316,
					58.754216170942186
				],
				[
					124.50471107010935,
					58.754216170942186
				],
				[
					130.10092710012555,
					59.37556964507519
				],
				[
					132.55809765692447,
					60.3560170101033
				],
				[
					155.181012783313,
					107.11488332002284
				],
				[
					153.93427107222806,
					112.71109935003904
				],
				[
					121.66020328268223,
					137.62172499482665
				],
				[
					113.69154671506703,
					140.27659892975868
				],
				[
					92.23467804338247,
					142.4029189353957
				],
				[
					84.2660214757675,
					142.4029189353957
				],
				[
					73.06148512727782,
					138.07361843055975
				],
				[
					70.36222880133641,
					135.91502032237037
				],
				[
					66.88022848850005,
					132.13444756092463
				],
				[
					66.6421774821763,
					131.89639655460093
				],
				[
					66.6421774821763,
					131.65834554827723
				],
				[
					68.9258532377562,
					139.1670391545211
				],
				[
					68.9258532377562,
					143.9764764348235
				],
				[
					64.8346037392439,
					160.0106238777107
				],
				[
					58.69772949147546,
					167.50721319549746
				],
				[
					37.591885185047886,
					180.8421043124432
				],
				[
					21.73930206901764,
					184.44111274703187
				],
				[
					-7.597458388262794,
					185.17947434291722
				],
				[
					-20.294856979799306,
					181.6490568762523
				],
				[
					-45.984191848662704,
					167.3579269711928
				],
				[
					-63.56768821406354,
					149.78653489424914
				],
				[
					-69.1275913787083,
					140.05468697471116
				],
				[
					-71.78650007645956,
					132.08603040709608
				],
				[
					-71.87526485847843,
					123.24989983338617
				],
				[
					-69.47054621832717,
					119.03760745030257
				],
				[
					-64.27377170739646,
					115.45070330417104
				],
				[
					-62.595310374673545,
					114.60743787499052
				],
				[
					-60.444781792122285,
					114.18378777899068
				],
				[
					-60.444781792122285,
					118.20644630957918
				],
				[
					-63.89853876522534,
					125.1018559673281
				],
				[
					-68.11083114830899,
					127.50657460747931
				],
				[
					-83.25733077100608,
					128.1440671328885
				],
				[
					-92.90041390852502,
					124.00843524336676
				],
				[
					-108.69651034508865,
					111.7145129337348
				],
				[
					-112.73934268977246,
					103.63288300718648
				],
				[
					-114.75268933647612,
					86.1220123725285
				],
				[
					-112.68689077312479,
					75.78898479295276
				],
				[
					-102.93083427667261,
					54.84856576210598
				],
				[
					-96.87062052246597,
					48.11454661711889
				],
				[
					-81.3892355857879,
					40.02888192775151
				],
				[
					-77.36657705519951,
					39.451910844627946
				],
				[
					-65.23001049551044,
					42.64340823449311
				],
				[
					-61.21945625337912,
					51.08816681475548
				],
				[
					-61.64310634937874,
					52.766628147478514
				],
				[
					-66.57358651425261,
					52.48822951296438
				],
				[
					-72.32715829421159,
					49.29269736028027
				],
				[
					-87.23560691058515,
					37.75731046062879
				],
				[
					-93.21109064559164,
					31.781826725622295
				],
				[
					-97.68564261191318,
					19.63719064029499
				],
				[
					-98.29085703476994,
					14.823718597173638
				],
				[
					-96.3743446957235,
					8.432654291805306
				],
				[
					-93.96962605557223,
					3.6191822486839555
				],
				[
					-88.8616163266604,
					-0.2178771922284568
				],
				[
					-81.56273038700692,
					-4.204222857445529
				],
				[
					-51.70145076325048,
					-10.030420368147361
				],
				[
					-42.15923669620747,
					-10.71229528456604
				],
				[
					-34.985428403944525,
					-10.06269847069973
				],
				[
					-19.846998306885325,
					-5.535694587730518
				],
				[
					-12.67319001462215,
					-2.929237806627043
				],
				[
					-5.204844036568829,
					1.0893859611423977
				],
				[
					-3.945998037026584,
					2.3482319606845294
				],
				[
					-1.5735574994278068,
					4.914341113597629
				],
				[
					0.39137199344736473,
					6.387029542549271
				],
				[
					3.542521755121925,
					9.191189701785902
				],
				[
					4.014589004950267,
					9.663256951614244
				],
				[
					4.248605248455078,
					9.4252059452906
				],
				[
					4.248605248455078,
					9.187154938966842
				],
				[
					4.482621491959662,
					8.949103932643197
				],
				[
					4.482621491959662,
					8.71105292631944
				],
				[
					4.482621491959662,
					8.23495091367215
				],
				[
					4.482621491959662,
					7.758848901024749
				],
				[
					4.482621491959662,
					6.0763528054826565
				],
				[
					4.482621491959662,
					5.124148780187966
				],
				[
					4.482621491959662,
					4.886097773864208
				],
				[
					4.482621491959662,
					4.6480467675405635
				],
				[
					4.482621491959662,
					4.409995761216919
				],
				[
					4.482621491959662,
					4.171944754893161
				],
				[
					4.482621491959662,
					3.933893748569517
				],
				[
					4.482621491959662,
					3.695842742245759
				],
				[
					4.482621491959662,
					2.9816897232747124
				],
				[
					4.482621491959662,
					-0.38330246780935795
				],
				[
					4.482621491959662,
					-1.2870893392755534
				],
				[
					4.482621491959662,
					-3.094663082207944
				],
				[
					4.482621491959662,
					-3.9984499536741396
				],
				[
					4.716637735464246,
					-5.378338837787737
				],
				[
					4.716637735464246,
					-5.8544408504351395
				],
				[
					4.716637735464246,
					-6.330542863082542
				],
				[
					4.950653978969058,
					-6.330542863082542
				],
				[
					0,
					0
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				4.950653978969058,
				-6.330542863082542
			]
		},
		{
			"id": "rckx4_-wFMcG2PGn2Hi-V",
			"type": "freedraw",
			"x": 253.78178299836418,
			"y": -600.0164979104024,
			"width": 47.48512361734788,
			"height": 31.749548623069813,
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
			"seed": 1832276157,
			"version": 15,
			"versionNonce": 1690770941,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674854655641,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					0.7060834933329261
				],
				[
					1.2588459995422454,
					1.9649294928751715
				],
				[
					7.908135125329409,
					9.142772547957293
				],
				[
					12.261644207079598,
					13.496281629707482
				],
				[
					23.119190953131465,
					20.520803697665997
				],
				[
					29.643402431528102,
					24.434523632140213
				],
				[
					40.190272440513354,
					29.417455713661525
				],
				[
					43.42211745856889,
					30.494737386346742
				],
				[
					46.77904012401473,
					31.28151613606053
				],
				[
					47.25110737384307,
					31.51553237956523
				],
				[
					47.48512361734788,
					31.749548623069813
				],
				[
					47.48512361734788,
					31.749548623069813
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				47.48512361734788,
				31.749548623069813
			]
		},
		{
			"id": "pt3FULsoW4wmJlS_PANvs",
			"type": "line",
			"x": 465.2194937676302,
			"y": -605.6772701455235,
			"width": 440.208762609152,
			"height": 213.16055449299853,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 1786052509,
			"version": 883,
			"versionNonce": 1656797437,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674854688856,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					100.25982129046429,
					3.2076364411412897
				],
				[
					69.51492860933672,
					28.00932348981462
				],
				[
					102.46683655248239,
					39.036330274266334
				],
				[
					104.9522504490144,
					77.18097796552343
				],
				[
					151.33184905394364,
					33.56115712882138
				],
				[
					173.47462740486594,
					77.49972422822805
				],
				[
					185.7403063747647,
					29.381142848290096
				],
				[
					200.32193920279542,
					29.3327256944616
				],
				[
					217.57458501703445,
					107.74430631979396
				],
				[
					275.57833530363405,
					21.50528582551317
				],
				[
					355.10351046702317,
					60.00902740766537
				],
				[
					401.7776467577428,
					47.703000809576224
				],
				[
					409.9964586201386,
					53.266938737040164
				],
				[
					416.6901301369353,
					59.30294391433233
				],
				[
					424.49336142896937,
					68.118900673947
				],
				[
					435.73824540564965,
					83.37837365557755
				],
				[
					440.208762609152,
					105.94480210249958
				],
				[
					435.8592882902208,
					128.00285043422195
				],
				[
					426.16375323605416,
					146.89360995299347
				],
				[
					390.9483433514242,
					168.8064068232302
				],
				[
					333.67085037225297,
					194.16892590375085
				],
				[
					258.4749757136997,
					213.16055449299853
				],
				[
					175.5686693079506,
					202.2223124905659
				],
				[
					68.75235843653718,
					144.54941275512795
				],
				[
					8.743331028871808,
					102.06739503339679
				],
				[
					0,
					0
				]
			],
			"lastCommittedPoint": [
				3.808816101179218,
				-2.4692748452558817
			],
			"startBinding": null,
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": null
		},
		{
			"id": "hEQnB04oRCF6y_r0zqotP",
			"type": "line",
			"x": 505.9584939515337,
			"y": -491.2756051743043,
			"width": 279.56064620603206,
			"height": 219.08762107417647,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"seed": 328471037,
			"version": 613,
			"versionNonce": 692259005,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674854712559,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					5.684341886080802e-14,
					-74.2154272935249
				],
				[
					83.71729373237736,
					-71.36688474327872
				],
				[
					105.93673257686146,
					-130.0323361322018
				],
				[
					179.45011113987243,
					-62.79301375280676
				],
				[
					222.2912227524987,
					-97.37496587484674
				],
				[
					180.31355038314837,
					37.11174840958148
				],
				[
					249.79216612711366,
					66.3839526617574
				],
				[
					-29.7684800789184,
					89.05528494197466
				],
				[
					82.87402830319684,
					-6.600871971958611
				],
				[
					0,
					0
				]
			],
			"lastCommittedPoint": [
				4.559281985521693,
				0.42768485881885
			],
			"startBinding": null,
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": null
		},
		{
			"id": "UoTry-uobIjzEWkJ1yuHH",
			"type": "freedraw",
			"x": 395.26074124819866,
			"y": -597.2365463280801,
			"width": 156.94420413523608,
			"height": 102.70488755880598,
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
			"seed": 1188867475,
			"version": 239,
			"versionNonce": 1867980979,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674854741424,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					0,
					-0.4761020126472886
				],
				[
					0.5366234549330784,
					-3.711981793521886
				],
				[
					1.3758541212944237,
					-5.394477889063978
				],
				[
					3.3206098000744078,
					-8.331785221329142
				],
				[
					4.79329822902605,
					-10.792990540946903
				],
				[
					9.687465528528492,
					-14.714780001059353
				],
				[
					16.941969077172416,
					-17.482627294924555
				],
				[
					21.751406357474707,
					-19.29020103785706
				],
				[
					29.80479294428983,
					-20.536942748942124
				],
				[
					35.40100897430602,
					-20.536942748942124
				],
				[
					41.88890758733146,
					-19.93576308890431
				],
				[
					43.56736892005438,
					-19.516147755723523
				],
				[
					48.47767527083283,
					-17.599635416676847
				],
				[
					48.71169151433742,
					-17.365619173172263
				],
				[
					50.204553757384474,
					-15.634705923801675
				],
				[
					50.62416909056515,
					-13.956244591078757
				],
				[
					50.62416909056515,
					-11.0270067844516
				],
				[
					50.62416909056515,
					-10.554939534623259
				],
				[
					50.62416909056515,
					-9.421171182471426
				],
				[
					50.62416909056515,
					-9.187154938966842
				],
				[
					50.38611808424139,
					-9.187154938966842
				],
				[
					50.85818533406973,
					-9.66325695161413
				],
				[
					51.092201577574315,
					-9.901307957937888
				],
				[
					59.92429738846522,
					-14.036939847459621
				],
				[
					63.946955919053835,
					-15.186847250887695
				],
				[
					69.64807578236514,
					-15.610497346887428
				],
				[
					72.87992080042068,
					-15.610497346887428
				],
				[
					74.5583821331436,
					-14.771266680525969
				],
				[
					80.46124013740746,
					-11.002798207537353
				],
				[
					85.27067741770975,
					-8.598079567386094
				],
				[
					95.82965171515207,
					-3.0018635373699
				],
				[
					99.275339162617,
					-0.12911241020947273
				],
				[
					100.17509127126414,
					0.47206724982834203
				],
				[
					100.64312375827353,
					1.416201749485026
				],
				[
					100.40507275194977,
					2.36033624914171
				],
				[
					100.16702174562624,
					2.594352492646294
				],
				[
					99.02518386783618,
					3.195532152684109
				],
				[
					98.54908185518889,
					3.195532152684109
				],
				[
					97.35882682357033,
					3.6635646396935044
				],
				[
					98.06491031690348,
					3.4255136333697465
				],
				[
					102.87434759720577,
					3.4255136333697465
				],
				[
					107.79675823644129,
					3.4255136333697465
				],
				[
					112.60619551674381,
					3.4255136333697465
				],
				[
					119.89297716794022,
					5.301678344225934
				],
				[
					120.1269934114448,
					5.535694587730632
				],
				[
					121.84983713517727,
					11.23681445104205
				],
				[
					121.84983713517727,
					12.136566559689186
				],
				[
					121.84983713517727,
					17.05090767328676
				],
				[
					120.76852069967299,
					19.201436255838075
				],
				[
					120.53046969334923,
					19.673503505666417
				],
				[
					120.22786248192097,
					20.573255614313553
				],
				[
					116.86287029083678,
					22.64712370330301
				],
				[
					116.38676827818949,
					22.64712370330301
				],
				[
					115.0068793940759,
					22.945696151912443
				],
				[
					114.5307773814286,
					22.945696151912443
				],
				[
					114.5307773814286,
					23.179712395417027
				],
				[
					115.00284463125695,
					23.65177964524537
				],
				[
					118.35976729670278,
					25.423040522806446
				],
				[
					119.25951940534992,
					26.024220182844203
				],
				[
					122.70520685281485,
					28.896971310004687
				],
				[
					128.4022919533072,
					35.215409884630105
				],
				[
					129.38273931833533,
					37.67258044142886
				],
				[
					129.80235465151623,
					41.808212330950596
				],
				[
					129.80235465151623,
					44.26538288774941
				],
				[
					127.34114933189835,
					49.179724001346926
				],
				[
					125.18255122370897,
					51.874945564469385
				],
				[
					118.85604312344549,
					57.04347673566684
				],
				[
					115.62016334257078,
					58.65738186328508
				],
				[
					110.68968317769713,
					60.678798035626926
				],
				[
					106.66298988428957,
					61.82467067623588
				],
				[
					102.51928846912983,
					62.80511804126394
				],
				[
					101.61550159766352,
					62.80511804126394
				],
				[
					101.37745059133977,
					62.80511804126394
				],
				[
					100.42524656604496,
					62.32901602861659
				],
				[
					99.94914455339767,
					62.09096502229289
				],
				[
					99.71109354707392,
					61.85291401596919
				],
				[
					99.94510979057873,
					62.32094650297847
				],
				[
					101.74864877069194,
					67.13038378328088
				],
				[
					102.6564704049772,
					71.26601567280261
				],
				[
					102.6564704049772,
					74.49786069085815
				],
				[
					100.61488041854022,
					79.40816704163666
				],
				[
					100.00966599568346,
					80.3079191502838
				],
				[
					97.42338302867506,
					81.74832947668307
				],
				[
					95.7408869331332,
					82.16794480986385
				],
				[
					86.90072159660417,
					82.16794480986385
				],
				[
					82.0872495534827,
					82.16794480986385
				],
				[
					68.51834219303237,
					80.21915436826481
				],
				[
					61.340499137950246,
					78.25825963820864
				],
				[
					50.785559603326874,
					73.84422911417272
				],
				[
					46.57326722024345,
					70.8342960511647
				],
				[
					43.01057165102611,
					66.12169307851946
				],
				[
					42.16730622184559,
					64.43919698297742
				],
				[
					41.182824093998306,
					61.9779916633596
				],
				[
					40.88021688257004,
					60.598102779246005
				],
				[
					40.64216587624628,
					60.360051772922304
				],
				[
					40.64216587624628,
					60.12200076659866
				],
				[
					40.64216587624628,
					60.82808425993164
				],
				[
					40.64216587624628,
					64.85074279052009
				],
				[
					39.419632742075464,
					67.77998059714719
				],
				[
					37.45066848638112,
					69.74491009002242
				],
				[
					31.51553237956523,
					72.97675510807795
				],
				[
					26.702060336443765,
					72.97675510807795
				],
				[
					20.310996031075547,
					72.97675510807795
				],
				[
					1.222533134170817,
					69.61176291699388
				],
				[
					-5.955309920911304,
					67.0012713730714
				],
				[
					-20.048736447837655,
					55.51833639006759
				],
				[
					-23.058669510845675,
					51.306044006983996
				],
				[
					-25.991942080291892,
					42.46587867045503
				],
				[
					-27.141849483719852,
					34.41249208364002
				],
				[
					-27.141849483719852,
					31.9512867640222
				],
				[
					-22.429246511074552,
					24.543462228254498
				],
				[
					-19.072323845628716,
					23.446006741474093
				],
				[
					-16.615153288830015,
					22.953765677550507
				],
				[
					-11.692742649594265,
					24.12788165789277
				],
				[
					-8.247055202129332,
					26.423661701929746
				],
				[
					-4.7126029726453,
					30.25668638002304
				],
				[
					-4.414030524035979,
					31.156438488670233
				],
				[
					-4.414030524035979,
					31.390454732174874
				],
				[
					-10.881755322966,
					27.31534428493876
				],
				[
					-15.239299167535364,
					23.57915391450257
				],
				[
					-22.83272279297921,
					13.29454348875538
				],
				[
					-25.132537599835132,
					9.844821278471272
				],
				[
					-25.73775202269212,
					5.031349235349921
				],
				[
					-25.73775202269212,
					-4.595594850892894
				],
				[
					-24.66047035000679,
					-7.831474631767492
				],
				[
					-19.63315587747593,
					-13.407516847688498
				],
				[
					-17.175985320677228,
					-14.8842400394592
				],
				[
					-11.48696974582299,
					-17.486662057743615
				],
				[
					-9.808508413100071,
					-17.91031215374346
				],
				[
					-6.451585747654008,
					-18.40255321766699
				],
				[
					-5.5518336390068725,
					-18.40255321766699
				],
				[
					-3.4013050564556124,
					-17.09125530147719
				],
				[
					-1.2467417110851784,
					-14.396033738354731
				],
				[
					3.373061716722077,
					-6.955931100034604
				],
				[
					5.777780356873109,
					-2.7476734797700146
				],
				[
					7.036626356415354,
					0.6092491856759352
				],
				[
					7.036626356415354,
					1.3153326790088613
				],
				[
					7.036626356415354,
					1.077281672685217
				],
				[
					6.798575350091824,
					1.077281672685217
				],
				[
					6.560524343768066,
					0.8392306663615727
				],
				[
					6.560524343768066,
					0.6011796600378148
				],
				[
					6.322473337444308,
					0.36312865371417047
				],
				[
					6.084422331120777,
					-0.1129733589332318
				],
				[
					5.370269312149503,
					-0.8271263779042783
				],
				[
					5.1322183058259725,
					-1.3032283905516806
				],
				[
					4.6561162931784565,
					-2.017381409522727
				],
				[
					4.418065286854926,
					-2.7315344284938874
				],
				[
					0,
					0
				]
			],
			"pressures": [],
			"simulatePressure": true,
			"lastCommittedPoint": [
				4.418065286854926,
				-2.7315344284938874
			]
		},
		{
			"id": "vSty2d4b",
			"type": "text",
			"x": 399.99351803493914,
			"y": -577.9984837158265,
			"width": 108,
			"height": 20,
			"angle": 0,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 0.5,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 2037290675,
			"version": 144,
			"versionNonce": 1220123997,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674854740549,
			"link": null,
			"locked": false,
			"text": "ElasticSearch",
			"rawText": "ElasticSearch",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 14,
			"containerId": null,
			"originalText": "ElasticSearch"
		}
	],
	"appState": {
		"theme": "light",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#000000",
		"currentItemBackgroundColor": "transparent",
		"currentItemFillStyle": "hachure",
		"currentItemStrokeWidth": 0.5,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 16,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 1268.138821871277,
		"scrollY": 748.0196676386335,
		"zoom": {
			"value": 0.9681486062975057
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