---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Query Service ^f3nt1tA8

Posts Service ^j5YqeNcP

Comments Service ^Csidi2vS

Event Bus ^JXxbIRSd

event 
{postId, title} ^Cz53AwkR

post service saves post,
sends PostCreated event
to event bus ^Ol7FN5MR

query service subscribes
to PostCreated event ^4YI76qkU

maintains knowledge of
posts & comments ^Ha9vaqPj

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
			"version": 367,
			"versionNonce": 1441444476,
			"isDeleted": false,
			"id": "XHWD4xvZqnRBBrwLERLaa",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -259.26171875,
			"y": -301.662109375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 155,
			"height": 65,
			"seed": 1120213886,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "j5YqeNcP"
				},
				{
					"id": "7KlFqFo6cAQmQDbYkbFFq",
					"type": "arrow"
				}
			],
			"updated": 1671570529220,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 239,
			"versionNonce": 1496105796,
			"isDeleted": false,
			"id": "j5YqeNcP",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -250.26171875,
			"y": -281.662109375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 137,
			"height": 25,
			"seed": 1557199806,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671570529220,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Posts Service",
			"rawText": "Posts Service",
			"baseline": 18,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XHWD4xvZqnRBBrwLERLaa",
			"originalText": "Posts Service"
		},
		{
			"type": "rectangle",
			"version": 442,
			"versionNonce": 1844703102,
			"isDeleted": false,
			"id": "Hvapaheano6XdIjgRFLeR",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -259.328125,
			"y": -219.154296875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 155,
			"height": 65,
			"seed": 1756388834,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "Csidi2vS"
				},
				{
					"id": "VWthIXAZWUvi1SzaC7OOG",
					"type": "arrow"
				}
			],
			"updated": 1671569725056,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 323,
			"versionNonce": 253972322,
			"isDeleted": false,
			"id": "Csidi2vS",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -233.328125,
			"y": -211.654296875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103,
			"height": 50,
			"seed": 678318498,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671569725056,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Comments \nService",
			"rawText": "Comments Service",
			"baseline": 43,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Hvapaheano6XdIjgRFLeR",
			"originalText": "Comments Service"
		},
		{
			"type": "rectangle",
			"version": 543,
			"versionNonce": 1661292478,
			"isDeleted": false,
			"id": "CeioCN3c6IUQ6AwOWDMTf",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -259.70703125,
			"y": -134.333984375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 155,
			"height": 65,
			"seed": 1365008190,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "f3nt1tA8"
				},
				{
					"id": "VWthIXAZWUvi1SzaC7OOG",
					"type": "arrow"
				}
			],
			"updated": 1671569725056,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 455,
			"versionNonce": 914821922,
			"isDeleted": false,
			"id": "f3nt1tA8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -249.20703125,
			"y": -114.333984375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 134,
			"height": 25,
			"seed": 615934142,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671569725057,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Query Service",
			"rawText": "Query Service",
			"baseline": 18,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "CeioCN3c6IUQ6AwOWDMTf",
			"originalText": "Query Service"
		},
		{
			"type": "rectangle",
			"version": 482,
			"versionNonce": 662743038,
			"isDeleted": false,
			"id": "5NjWXapqoA-mD1iJZe-Pu",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 256.08984375,
			"y": -302.55859375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 108,
			"height": 235,
			"seed": 827646114,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "JXxbIRSd"
				},
				{
					"id": "l4BHEq6Jdx-QnpYesMOAx",
					"type": "arrow"
				},
				{
					"id": "VWthIXAZWUvi1SzaC7OOG",
					"type": "arrow"
				}
			],
			"updated": 1671569725057,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 299,
			"versionNonce": 205283042,
			"isDeleted": false,
			"id": "JXxbIRSd",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 276.58984375,
			"y": -210.05859375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 67,
			"height": 50,
			"seed": 555188158,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671569725057,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Event \nBus",
			"rawText": "Event Bus",
			"baseline": 43,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "5NjWXapqoA-mD1iJZe-Pu",
			"originalText": "Event Bus"
		},
		{
			"type": "rectangle",
			"version": 567,
			"versionNonce": 1557279394,
			"isDeleted": false,
			"id": "XTz-kDMsJZTCjncLf95b3",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 15.9453125,
			"y": -300.505859375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 119,
			"height": 70,
			"seed": 166481954,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [
				{
					"type": "text",
					"id": "Cz53AwkR"
				},
				{
					"id": "7KlFqFo6cAQmQDbYkbFFq",
					"type": "arrow"
				},
				{
					"id": "l4BHEq6Jdx-QnpYesMOAx",
					"type": "arrow"
				}
			],
			"updated": 1671569725057,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 202,
			"versionNonce": 823312124,
			"isDeleted": false,
			"id": "Cz53AwkR",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 32.4453125,
			"y": -295.505859375,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 86,
			"height": 60,
			"seed": 923726014,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671570528044,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 3,
			"text": "event \n{postId, \ntitle}",
			"rawText": "event \n{postId, title}",
			"baseline": 56,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XTz-kDMsJZTCjncLf95b3",
			"originalText": "event \n{postId, title}"
		},
		{
			"type": "arrow",
			"version": 945,
			"versionNonce": 549173956,
			"isDeleted": false,
			"id": "7KlFqFo6cAQmQDbYkbFFq",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -103.26171875,
			"y": -265.71753160342587,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 118.20703125,
			"height": 4.39294909229028,
			"seed": 973924222,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1671570529220,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "XHWD4xvZqnRBBrwLERLaa",
				"gap": 1,
				"focus": 0.17980836000740705
			},
			"endBinding": {
				"elementId": "XTz-kDMsJZTCjncLf95b3",
				"gap": 1,
				"focus": 0.18416476700461162
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
					118.20703125,
					-4.39294909229028
				]
			]
		},
		{
			"type": "arrow",
			"version": 886,
			"versionNonce": 319705596,
			"isDeleted": false,
			"id": "l4BHEq6Jdx-QnpYesMOAx",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 135.9453125,
			"y": -264.6745661362596,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 119.14453125,
			"height": 3.305376111892997,
			"seed": 661420094,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1671570528075,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "XTz-kDMsJZTCjncLf95b3",
				"gap": 1,
				"focus": 0.0684767356466546
			},
			"endBinding": {
				"elementId": "5NjWXapqoA-mD1iJZe-Pu",
				"gap": 1,
				"focus": 0.7096515893936157
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
					119.14453125,
					-3.305376111892997
				]
			]
		},
		{
			"type": "text",
			"version": 266,
			"versionNonce": 1266381346,
			"isDeleted": false,
			"id": "Ol7FN5MR",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -33.25,
			"y": -372.466796875,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 203,
			"height": 60,
			"seed": 2070330850,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671569725057,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "post service saves post,\nsends PostCreated event\nto event bus",
			"rawText": "post service saves post,\nsends PostCreated event\nto event bus",
			"baseline": 54,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "post service saves post,\nsends PostCreated event\nto event bus"
		},
		{
			"type": "arrow",
			"version": 437,
			"versionNonce": 1710055676,
			"isDeleted": false,
			"id": "VWthIXAZWUvi1SzaC7OOG",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 239.83984375,
			"y": -103.20055819236885,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 333.8671875,
			"height": 2.102901942368817,
			"seed": 637082594,
			"groupIds": [],
			"strokeSharpness": "round",
			"boundElements": [],
			"updated": 1671570528073,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "5NjWXapqoA-mD1iJZe-Pu",
				"gap": 16.25,
				"focus": -0.6908984300974927
			},
			"endBinding": {
				"elementId": "CeioCN3c6IUQ6AwOWDMTf",
				"gap": 10.679687499999986,
				"focus": 0.03915765469902355
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
					-333.8671875,
					2.102901942368817
				]
			]
		},
		{
			"type": "text",
			"version": 823,
			"versionNonce": 1632427490,
			"isDeleted": false,
			"id": "4YI76qkU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -17.6796875,
			"y": -152.23828125,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 190,
			"height": 40,
			"seed": 483830590,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671569725057,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "query service subscribes\nto PostCreated event",
			"rawText": "query service subscribes\nto PostCreated event",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "query service subscribes\nto PostCreated event"
		},
		{
			"type": "text",
			"version": 242,
			"versionNonce": 1289873726,
			"isDeleted": false,
			"id": "Ha9vaqPj",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -265.88954920703816,
			"y": -58.68210965665395,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 178,
			"height": 40,
			"seed": 1207378046,
			"groupIds": [],
			"strokeSharpness": "sharp",
			"boundElements": [],
			"updated": 1671569725057,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "maintains knowledge of\nposts & comments",
			"rawText": "maintains knowledge of\nposts & comments",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "maintains knowledge of\nposts & comments"
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
		"scrollX": 405.3998527285191,
		"scrollY": 384.68578139082695,
		"zoom": {
			"value": 2
		},
		"currentItemLinearStrokeSharpness": "round",
		"gridSize": null,
		"colorPalette": {}
	},
	"files": {}
}
```
%%