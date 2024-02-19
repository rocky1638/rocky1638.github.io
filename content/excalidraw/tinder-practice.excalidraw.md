---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Requirements: ^x3byKvL8

- user can create profile with bio and pictures
- user can "swipe" on users based on preferences and location
- two users can match
- real-time chat system
- notifications
- elo/ranking system? ^Ax20exJn

Estimations: ^MAjjjJVS

- 10M DAU
- each person swipes 30 times a day
- each person matches with 2 people/day
- 30M profiles * 3MB = 100TB of profile data
- 30M swipes/day = 350 SPS, 700 peak SPS ^9RRlYUZN

client ^VdRnS9EK

profile service ^9yx5Eocv

get/create profile ^9NRowfGp

user database ^sz3EzbsU

save user ^1kLf18Xb

cache ^VUURBoKs

check cache first ^0TlBE0ix

use caching
policy ^8SUP1ARn

blob
storage ^Vqdp08yR

save images ^b3O0dVSQ

update image
urls in db ^c1MS1VqN

load balancer ^VXl7igDL

* NoSQL - not much
relational data, just
storing raw user data. ^cz2n4FtW

feed generation service ^uXQZScsZ

feed message queue ^7CZT20yt

feed generation service ^fsHmYMke

feed generation service ^OLaeAUTt

feed database ^Py29VPIS

user_id:
other_user_ids[] ^Ia2MiNFa

save ^HYSJWC9a

* precompute for active
users, cache the feeds. ^94RtGUQq

feed service ^B1Sz9mJ2

load balancer ^Lb9uUzkr

read ^0UesJmBm

grab profiles
referenced in feed ^859SMYz5

* filter users
by preference, location
of user. ^ocMFJdZ9

on a job ^KeGgDJWL

* for a cache miss, we can
prioritize generating for a
user who's logged in but
doesn't have a precomputed
feed. ^TmRi3IrK

Tinder System Design ^sfVgSKwS

likes service ^G5iV695C

like a profile ^HP4R7KPK

likes/dislikes database ^pNmP36XD

user1, user2 ^ITY1uS4q

save like in db,
emit like event. ^RNFh8Gfk

match service ^6zQmDg2M

on like event,
check if it creates a match ^RZ0RoLPo

matches database ^55qO8EPM

save match ^ULECbezX

notification service ^fKy96TDi

notify user of match ^OIIalM3N

you got 
a match! ^N6JwKfEi

check likes? ^yFAM1LKt

image database ^YnoStR6k

* authentication can be
done in a separate gateway. ^YC1rFsZd

* we might not to precompute these feeds
for users, maybe we can just geographically
shard our user databases, and then filter
on those databases based on user preferences. ^cm69ZQMP

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://excalidraw.com",
	"elements": [
		{
			"type": "text",
			"version": 168,
			"versionNonce": 170110301,
			"isDeleted": false,
			"id": "x3byKvL8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -395.8931978604321,
			"y": -439.1271374634946,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 132,
			"height": 25,
			"seed": 136394611,
			"groupIds": [
				"xdT7OkEFFKbQjX5f-wQAA"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674948335394,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Requirements:",
			"rawText": "Requirements:",
			"baseline": 18,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Requirements:"
		},
		{
			"type": "text",
			"version": 445,
			"versionNonce": 1564353267,
			"isDeleted": false,
			"id": "Ax20exJn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -393.7135103604321,
			"y": -403.1076062134946,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 492,
			"height": 120,
			"seed": 1073767379,
			"groupIds": [
				"xdT7OkEFFKbQjX5f-wQAA"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674948335394,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "- user can create profile with bio and pictures\n- user can \"swipe\" on users based on preferences and location\n- two users can match\n- real-time chat system\n- notifications\n- elo/ranking system?",
			"rawText": "- user can create profile with bio and pictures\n- user can \"swipe\" on users based on preferences and location\n- two users can match\n- real-time chat system\n- notifications\n- elo/ranking system?",
			"baseline": 114,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- user can create profile with bio and pictures\n- user can \"swipe\" on users based on preferences and location\n- two users can match\n- real-time chat system\n- notifications\n- elo/ranking system?"
		},
		{
			"type": "text",
			"version": 156,
			"versionNonce": 929036733,
			"isDeleted": false,
			"id": "MAjjjJVS",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 168.30520654413954,
			"y": -430.9376843384946,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 119,
			"height": 25,
			"seed": 34953139,
			"groupIds": [
				"1KNmKBGkEVY9whQsZi6_c"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674948335394,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "Estimations:",
			"rawText": "Estimations:",
			"baseline": 18,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Estimations:"
		},
		{
			"type": "text",
			"version": 539,
			"versionNonce": 1778601107,
			"isDeleted": false,
			"id": "9RRlYUZN",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 168.30520654413954,
			"y": -391.2970593384946,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 377,
			"height": 100,
			"seed": 1161225203,
			"groupIds": [
				"1KNmKBGkEVY9whQsZi6_c"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674948335394,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "- 10M DAU\n- each person swipes 30 times a day\n- each person matches with 2 people/day\n- 30M profiles * 3MB = 100TB of profile data\n- 30M swipes/day = 350 SPS, 700 peak SPS",
			"rawText": "- 10M DAU\n- each person swipes 30 times a day\n- each person matches with 2 people/day\n- 30M profiles * 3MB = 100TB of profile data\n- 30M swipes/day = 350 SPS, 700 peak SPS",
			"baseline": 94,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- 10M DAU\n- each person swipes 30 times a day\n- each person matches with 2 people/day\n- 30M profiles * 3MB = 100TB of profile data\n- 30M swipes/day = 350 SPS, 700 peak SPS"
		},
		{
			"type": "rectangle",
			"version": 315,
			"versionNonce": 783223571,
			"isDeleted": false,
			"id": "I29l_wrFYhX3JadBt6H_d",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -634.5471600468954,
			"y": -130.55869608554167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 97,
			"height": 45,
			"seed": 321094579,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "VdRnS9EK"
				},
				{
					"id": "mHst7whVa98MBHc6YasYp",
					"type": "arrow"
				},
				{
					"id": "Quo_Dg0JH_uoaExVJj9QU",
					"type": "arrow"
				},
				{
					"id": "Zj-dOe3pnZeZ0cN452z_Y",
					"type": "arrow"
				},
				{
					"id": "S-CnEOVxW0pbROHhZwqyj",
					"type": "arrow"
				}
			],
			"updated": 1674947366355,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 276,
			"versionNonce": 1233725341,
			"isDeleted": false,
			"id": "VdRnS9EK",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -607.0471600468954,
			"y": -118.05869608554167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 42,
			"height": 20,
			"seed": 1297108435,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client",
			"rawText": "client",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "I29l_wrFYhX3JadBt6H_d",
			"originalText": "client"
		},
		{
			"type": "rectangle",
			"version": 312,
			"versionNonce": 797597267,
			"isDeleted": false,
			"id": "q7xFDoA5D1lqPsfeDZegJ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -56.48466004689544,
			"y": -136.75986796054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 100,
			"height": 50,
			"seed": 2140605885,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "9yx5Eocv"
				},
				{
					"id": "KFIs1epQQm16ZY-IuVa8a",
					"type": "arrow"
				},
				{
					"id": "DiMZliUkEMLdyKIa0QGpX",
					"type": "arrow"
				},
				{
					"id": "gn645T7AbnTRtnB4AqQRW",
					"type": "arrow"
				},
				{
					"id": "h3wroTwqJx-D8QQ7LO4nY",
					"type": "arrow"
				},
				{
					"id": "yivKDbnnVpVsm0cKJQN1U",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 225,
			"versionNonce": 730834013,
			"isDeleted": false,
			"id": "9yx5Eocv",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -34.98466004689544,
			"y": -131.75986796054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 57,
			"height": 40,
			"seed": 777601053,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "profile \nservice",
			"rawText": "profile service",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "q7xFDoA5D1lqPsfeDZegJ",
			"originalText": "profile service"
		},
		{
			"type": "arrow",
			"version": 703,
			"versionNonce": 590125939,
			"isDeleted": false,
			"id": "mHst7whVa98MBHc6YasYp",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -528.7307537968956,
			"y": -106.98333406666279,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 218.92570075516426,
			"height": 3.492035410309728,
			"seed": 2081846803,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "9NRowfGp"
				}
			],
			"updated": 1674946675569,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "I29l_wrFYhX3JadBt6H_d",
				"focus": 0.08548751550473459,
				"gap": 8.816406249999886
			},
			"endBinding": {
				"elementId": "915xKgFvGrcMaTaz4LO4U",
				"focus": -0.04360570999696278,
				"gap": 4.799977289543278
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
					218.92570075516426,
					-3.492035410309728
				]
			]
		},
		{
			"type": "text",
			"version": 173,
			"versionNonce": 817568979,
			"isDeleted": false,
			"id": "9NRowfGp",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -261.66044129689544,
			"y": -117.59580546054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 143,
			"height": 20,
			"seed": 1403472733,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "get/create profile",
			"rawText": "get/create profile",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "mHst7whVa98MBHc6YasYp",
			"originalText": "get/create profile"
		},
		{
			"type": "ellipse",
			"version": 564,
			"versionNonce": 1679330845,
			"isDeleted": false,
			"id": "Wbt35Utay8pVyYWB8KBcg",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 246.5198972447712,
			"y": 30.85146016445833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 92,
			"height": 71,
			"seed": 620813075,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "sz3EzbsU"
				},
				{
					"id": "KFIs1epQQm16ZY-IuVa8a",
					"type": "arrow"
				},
				{
					"id": "NcqMscFm3bUTe-Ij1VIRw",
					"type": "arrow"
				},
				{
					"id": "ODeOyMYJJDHYax6X_1j_Q",
					"type": "arrow"
				}
			],
			"updated": 1674948131056,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 574,
			"versionNonce": 461769331,
			"isDeleted": false,
			"id": "sz3EzbsU",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 254.0198972447712,
			"y": 46.35146016445833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 77,
			"height": 40,
			"seed": 503888563,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "user \ndatabase",
			"rawText": "user database",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Wbt35Utay8pVyYWB8KBcg",
			"originalText": "user database"
		},
		{
			"type": "arrow",
			"version": 1187,
			"versionNonce": 280041885,
			"isDeleted": false,
			"id": "KFIs1epQQm16ZY-IuVa8a",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 50.47457176666478,
			"y": -99.87962578189456,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 205.793231543284,
			"height": 133.30677983379275,
			"seed": 506851197,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "1kLf18Xb"
				}
			],
			"updated": 1674946675569,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "q7xFDoA5D1lqPsfeDZegJ",
				"focus": -0.4359106127340677,
				"gap": 6.959231813560223
			},
			"endBinding": {
				"elementId": "Wbt35Utay8pVyYWB8KBcg",
				"focus": 0.20370391268402852,
				"gap": 8.500929155053733
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
					205.793231543284,
					133.30677983379275
				]
			]
		},
		{
			"type": "text",
			"version": 163,
			"versionNonce": 635608829,
			"isDeleted": false,
			"id": "1kLf18Xb",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 31.394812845193712,
			"y": -65.34459614206264,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 79,
			"height": 20,
			"seed": 1432691101,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "save user",
			"rawText": "save user",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KFIs1epQQm16ZY-IuVa8a",
			"originalText": "save user"
		},
		{
			"type": "ellipse",
			"version": 460,
			"versionNonce": 374905683,
			"isDeleted": false,
			"id": "7eYZAyEhfrVSVAnVwB-KM",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 276.91377745310456,
			"y": -140.05478983554167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 78,
			"height": 57,
			"seed": 1443728979,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "VUURBoKs"
				},
				{
					"id": "DiMZliUkEMLdyKIa0QGpX",
					"type": "arrow"
				},
				{
					"id": "NcqMscFm3bUTe-Ij1VIRw",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 418,
			"versionNonce": 227522397,
			"isDeleted": false,
			"id": "VUURBoKs",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 293.91377745310456,
			"y": -121.55478983554167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 44,
			"height": 20,
			"seed": 1832661939,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "cache",
			"rawText": "cache",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7eYZAyEhfrVSVAnVwB-KM",
			"originalText": "cache"
		},
		{
			"type": "arrow",
			"version": 775,
			"versionNonce": 435543549,
			"isDeleted": false,
			"id": "DiMZliUkEMLdyKIa0QGpX",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 52.51924620310456,
			"y": -119.26782992036715,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 216.85878521789218,
			"height": 6.4581979696629315,
			"seed": 73571965,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "0TlBE0ix"
				}
			],
			"updated": 1674946675569,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "q7xFDoA5D1lqPsfeDZegJ",
				"focus": -0.34977257465262385,
				"gap": 9.00390625
			},
			"endBinding": {
				"elementId": "7eYZAyEhfrVSVAnVwB-KM",
				"focus": -0.0045934911674610805,
				"gap": 7.563486653011857
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
					216.85878521789218,
					6.4581979696629315
				]
			]
		},
		{
			"type": "text",
			"version": 185,
			"versionNonce": 260391965,
			"isDeleted": false,
			"id": "0TlBE0ix",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 77.67158995310456,
			"y": -99.69150858554167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 137,
			"height": 20,
			"seed": 229362771,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "check cache first",
			"rawText": "check cache first",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "DiMZliUkEMLdyKIa0QGpX",
			"originalText": "check cache first"
		},
		{
			"type": "arrow",
			"version": 732,
			"versionNonce": 987960925,
			"isDeleted": false,
			"id": "NcqMscFm3bUTe-Ij1VIRw",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 299.6314517762804,
			"y": 21.88457211428954,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 13.38907167415357,
			"height": 98.29892410239731,
			"seed": 829320893,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "8SUP1ARn"
				}
			],
			"updated": 1674946675569,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Wbt35Utay8pVyYWB8KBcg",
				"focus": 0.02280525210628391,
				"gap": 9.335243628626756
			},
			"endBinding": {
				"elementId": "7eYZAyEhfrVSVAnVwB-KM",
				"focus": -0.04830347782364309,
				"gap": 6.710176089049
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
					13.38907167415357,
					-98.29892410239731
				]
			]
		},
		{
			"type": "text",
			"version": 178,
			"versionNonce": 836810877,
			"isDeleted": false,
			"id": "8SUP1ARn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 198.91768370310456,
			"y": -58.26182108554167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 89,
			"height": 40,
			"seed": 2111929469,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "use caching\npolicy",
			"rawText": "use caching\npolicy",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "NcqMscFm3bUTe-Ij1VIRw",
			"originalText": "use caching\npolicy"
		},
		{
			"type": "ellipse",
			"version": 471,
			"versionNonce": 1677908435,
			"isDeleted": false,
			"id": "tVsReU9KGHE-Tt_tJ_xZ_",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -94.03283713022881,
			"y": 28.87489766445833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 98,
			"height": 77,
			"seed": 697125331,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Vqdp08yR"
				},
				{
					"id": "gn645T7AbnTRtnB4AqQRW",
					"type": "arrow"
				},
				{
					"id": "P1eAV9joFfWdeIqtbzmES",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 449,
			"versionNonce": 1972281565,
			"isDeleted": false,
			"id": "Vqdp08yR",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -76.03283713022881,
			"y": 47.37489766445833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 62,
			"height": 40,
			"seed": 793149651,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "blob\nstorage",
			"rawText": "blob\nstorage",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "tVsReU9KGHE-Tt_tJ_xZ_",
			"originalText": "blob\nstorage"
		},
		{
			"type": "arrow",
			"version": 1039,
			"versionNonce": 1313489597,
			"isDeleted": false,
			"id": "gn645T7AbnTRtnB4AqQRW",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -17.919704099681724,
			"y": -77.88877421054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 16.760222054843283,
			"height": 98.86713879389399,
			"seed": 1381842749,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "b3O0dVSQ"
				}
			],
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "q7xFDoA5D1lqPsfeDZegJ",
				"focus": 0.10496549532570457,
				"gap": 8.87109375
			},
			"endBinding": {
				"elementId": "tVsReU9KGHE-Tt_tJ_xZ_",
				"focus": 0.050323853252595405,
				"gap": 8.65740996014516
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
					-16.760222054843283,
					98.86713879389399
				]
			]
		},
		{
			"type": "text",
			"version": 165,
			"versionNonce": 150457757,
			"isDeleted": false,
			"id": "b3O0dVSQ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -80.66825379689544,
			"y": -21.29893046054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 95,
			"height": 20,
			"seed": 1378579603,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "save images",
			"rawText": "save images",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "gn645T7AbnTRtnB4AqQRW",
			"originalText": "save images"
		},
		{
			"type": "arrow",
			"version": 2016,
			"versionNonce": 295081875,
			"isDeleted": false,
			"id": "P1eAV9joFfWdeIqtbzmES",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 6.368022099934002,
			"y": 90.01635052777549,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 128.3312854150996,
			"height": 110.29207324535035,
			"seed": 454777235,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "c1MS1VqN"
				}
			],
			"updated": 1674948147249,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "tVsReU9KGHE-Tt_tJ_xZ_",
				"gap": 9.34695098415143,
				"focus": -0.37648384547551356
			},
			"endBinding": {
				"elementId": "ouVseCINFe68lD3fMNUUH",
				"gap": 13.329225709735322,
				"focus": -0.7806373498505652
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
					128.3312854150996,
					110.29207324535035
				]
			]
		},
		{
			"type": "text",
			"version": 252,
			"versionNonce": 1061556733,
			"isDeleted": false,
			"id": "c1MS1VqN",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 113.27185036977119,
			"y": 82.76161641445833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 105,
			"height": 40,
			"seed": 329067133,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "update image\nurls in db",
			"rawText": "update image\nurls in db",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "P1eAV9joFfWdeIqtbzmES",
			"originalText": "update image\nurls in db"
		},
		{
			"type": "diamond",
			"version": 260,
			"versionNonce": 1323071357,
			"isDeleted": false,
			"id": "915xKgFvGrcMaTaz4LO4U",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -302.91434754689544,
			"y": -141.58018046054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 57,
			"seed": 181960371,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Lb9uUzkr"
				},
				{
					"id": "mHst7whVa98MBHc6YasYp",
					"type": "arrow"
				},
				{
					"id": "h3wroTwqJx-D8QQ7LO4nY",
					"type": "arrow"
				}
			],
			"updated": 1674946675570,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 236,
			"versionNonce": 806144605,
			"isDeleted": false,
			"id": "Lb9uUzkr",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -277.91434754689544,
			"y": -123.08018046054167,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 107,
			"height": 20,
			"seed": 1935421523,
			"groupIds": [],
			"roundness": null,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "load balancer",
			"rawText": "load balancer",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "915xKgFvGrcMaTaz4LO4U",
			"originalText": "load balancer"
		},
		{
			"type": "arrow",
			"version": 476,
			"versionNonce": 1961265875,
			"isDeleted": false,
			"id": "h3wroTwqJx-D8QQ7LO4nY",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -144.73446020804545,
			"y": -111.6072594942284,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 74.17167516115,
			"height": 1.7327641814305172,
			"seed": 1007872221,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "915xKgFvGrcMaTaz4LO4U",
				"focus": 0.11699527856260476,
				"gap": 1.787149803466555
			},
			"endBinding": {
				"elementId": "q7xFDoA5D1lqPsfeDZegJ",
				"focus": 0.11759057042715405,
				"gap": 14.078125
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
					74.17167516115,
					-1.7327641814305172
				]
			]
		},
		{
			"type": "text",
			"version": 447,
			"versionNonce": 1761217341,
			"isDeleted": false,
			"id": "cz2n4FtW",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 351.3435970269253,
			"y": 35.97038231519764,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 182,
			"height": 60,
			"seed": 312667869,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674948108759,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "* NoSQL - not much\nrelational data, just\nstoring raw user data.",
			"rawText": "* NoSQL - not much\nrelational data, just\nstoring raw user data.",
			"baseline": 54,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "* NoSQL - not much\nrelational data, just\nstoring raw user data."
		},
		{
			"type": "diamond",
			"version": 348,
			"versionNonce": 396894099,
			"isDeleted": false,
			"id": "kxnThiWAMGL5XriZaBhI2",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -478.09794129689544,
			"y": 365.79872578945833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 236,
			"height": 73,
			"seed": 644715347,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "7CZT20yt"
				},
				{
					"id": "1Ee2U196esT9IQoADBLcC",
					"type": "arrow"
				},
				{
					"id": "BiBNvie8GsNPxLgj2R7Rh",
					"type": "arrow"
				},
				{
					"id": "vsI2nLp2QxkEU_27zg3su",
					"type": "arrow"
				},
				{
					"id": "4nW9v-ktQb_ZWOl4kpi_S",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 345,
			"versionNonce": 773429021,
			"isDeleted": false,
			"id": "7CZT20yt",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -439.59794129689544,
			"y": 392.29872578945833,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 159,
			"height": 20,
			"seed": 84343731,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "feed message queue",
			"rawText": "feed message queue",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kxnThiWAMGL5XriZaBhI2",
			"originalText": "feed message queue"
		},
		{
			"type": "rectangle",
			"version": 260,
			"versionNonce": 107562099,
			"isDeleted": false,
			"id": "HJbqu_7O_ZUpQt3L-oN36",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -86.16369650522881,
			"y": 368.1769809977917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 109,
			"height": 70,
			"seed": 870906045,
			"groupIds": [
				"aJ-uPblBFHC1gUk1OBYBz"
			],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "OLaeAUTt"
				},
				{
					"id": "BiBNvie8GsNPxLgj2R7Rh",
					"type": "arrow"
				},
				{
					"id": "D-SfrLm9_9yIYEUtuD_Z6",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 230,
			"versionNonce": 222994589,
			"isDeleted": false,
			"id": "OLaeAUTt",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -75.66369650522881,
			"y": 373.1769809977917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 88,
			"height": 60,
			"seed": 1160042781,
			"groupIds": [
				"aJ-uPblBFHC1gUk1OBYBz"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "feed \ngeneration \nservice",
			"rawText": "feed generation service",
			"baseline": 54,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HJbqu_7O_ZUpQt3L-oN36",
			"originalText": "feed generation service"
		},
		{
			"type": "rectangle",
			"version": 277,
			"versionNonce": 983761843,
			"isDeleted": false,
			"id": "1KjOpSEH1eRK9cslDzd_e",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -86.16369650522881,
			"y": 460.8644809977917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 109,
			"height": 70,
			"seed": 1219338301,
			"groupIds": [
				"aJ-uPblBFHC1gUk1OBYBz"
			],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "uXQZScsZ"
				},
				{
					"id": "vsI2nLp2QxkEU_27zg3su",
					"type": "arrow"
				},
				{
					"id": "eDwLxc_Ppl9H2dfJS1N_h",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 249,
			"versionNonce": 101113181,
			"isDeleted": false,
			"id": "uXQZScsZ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -75.66369650522881,
			"y": 465.8644809977917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 88,
			"height": 60,
			"seed": 819935549,
			"groupIds": [
				"aJ-uPblBFHC1gUk1OBYBz"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "feed \ngeneration \nservice",
			"rawText": "feed generation service",
			"baseline": 54,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "1KjOpSEH1eRK9cslDzd_e",
			"originalText": "feed generation service"
		},
		{
			"type": "rectangle",
			"version": 301,
			"versionNonce": 1751511795,
			"isDeleted": false,
			"id": "PE7KrF0SzWWHJpHBMw451",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -86.16369650522881,
			"y": 278.5363559977917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 109,
			"height": 70,
			"seed": 984867197,
			"groupIds": [
				"aJ-uPblBFHC1gUk1OBYBz"
			],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "fsHmYMke"
				},
				{
					"id": "1Ee2U196esT9IQoADBLcC",
					"type": "arrow"
				},
				{
					"id": "8CEqIyCVFZ5SSTbyWk9yN",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 272,
			"versionNonce": 82504221,
			"isDeleted": false,
			"id": "fsHmYMke",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -75.66369650522881,
			"y": 283.5363559977917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 88,
			"height": 60,
			"seed": 739551709,
			"groupIds": [
				"aJ-uPblBFHC1gUk1OBYBz"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "feed \ngeneration \nservice",
			"rawText": "feed generation service",
			"baseline": 54,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "PE7KrF0SzWWHJpHBMw451",
			"originalText": "feed generation service"
		},
		{
			"id": "1Ee2U196esT9IQoADBLcC",
			"type": "arrow",
			"x": -256.70601421356173,
			"y": 387.7036737061251,
			"width": 164.10807291666663,
			"height": 72.51302083333337,
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
			"seed": 1145607059,
			"version": 516,
			"versionNonce": 1679014003,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					164.10807291666663,
					-72.51302083333337
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "kxnThiWAMGL5XriZaBhI2",
				"focus": 0.8517766656354866,
				"gap": 9.626442111703007
			},
			"endBinding": {
				"elementId": "PE7KrF0SzWWHJpHBMw451",
				"focus": 0.427717920882807,
				"gap": 6.434244791666288
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "BiBNvie8GsNPxLgj2R7Rh",
			"type": "arrow",
			"x": -233.7209881718951,
			"y": 403.06825703945833,
			"width": 137.81575520833337,
			"height": 1.0546875,
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
			"seed": 2011474963,
			"version": 514,
			"versionNonce": 2089431571,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					137.81575520833337,
					1.0546875
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "kxnThiWAMGL5XriZaBhI2",
				"focus": -0.005414149727674389,
				"gap": 3.2106193209379583
			},
			"endBinding": {
				"elementId": "HJbqu_7O_ZUpQt3L-oN36",
				"focus": -0.04059047951222207,
				"gap": 9.741536458332916
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "vsI2nLp2QxkEU_27zg3su",
			"type": "arrow",
			"x": -275.32906108856173,
			"y": 423.1398716227917,
			"width": 181.47135416666663,
			"height": 74.84700520833337,
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
			"seed": 1857831357,
			"version": 528,
			"versionNonce": 1598060467,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					181.47135416666663,
					74.84700520833337
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "kxnThiWAMGL5XriZaBhI2",
				"focus": -0.38688710975984375,
				"gap": 10.090331501793735
			},
			"endBinding": {
				"elementId": "1KjOpSEH1eRK9cslDzd_e",
				"focus": -0.4832091031553637,
				"gap": 7.694010416666288
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "7Rm4xL0cdmFLq8cW-BIpC",
			"type": "ellipse",
			"x": 182.85681130727176,
			"y": 348.85829610195833,
			"width": 111,
			"height": 83,
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
			"seed": 784498877,
			"version": 201,
			"versionNonce": 1581434589,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "Py29VPIS"
				},
				{
					"id": "8CEqIyCVFZ5SSTbyWk9yN",
					"type": "arrow"
				},
				{
					"id": "D-SfrLm9_9yIYEUtuD_Z6",
					"type": "arrow"
				},
				{
					"id": "eDwLxc_Ppl9H2dfJS1N_h",
					"type": "arrow"
				},
				{
					"id": "65S1RDNZcY32m6Yjp9kqI",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"id": "Py29VPIS",
			"type": "text",
			"x": 199.85681130727176,
			"y": 370.35829610195833,
			"width": 77,
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
			"seed": 1577446717,
			"version": 190,
			"versionNonce": 827810163,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "feed \ndatabase",
			"rawText": "feed database",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "7Rm4xL0cdmFLq8cW-BIpC",
			"originalText": "feed database"
		},
		{
			"id": "Ia2MiNFa",
			"type": "text",
			"x": 205.2764076614385,
			"y": 440.14703308112485,
			"width": 139,
			"height": 40,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 396664979,
			"version": 347,
			"versionNonce": 576976893,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "user_id:\nother_user_ids[]",
			"rawText": "user_id:\nother_user_ids[]",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 34,
			"containerId": null,
			"originalText": "user_id:\nother_user_ids[]"
		},
		{
			"id": "8CEqIyCVFZ5SSTbyWk9yN",
			"type": "arrow",
			"x": 33.44047016143827,
			"y": 310.95144459880896,
			"width": 144.30906863814664,
			"height": 60.18935350475226,
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
			"seed": 660282973,
			"version": 459,
			"versionNonce": 1247611219,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HYSJWC9a"
				}
			],
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					144.30906863814664,
					60.18935350475226
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "PE7KrF0SzWWHJpHBMw451",
				"focus": -0.5151282198231586,
				"gap": 10.604166666667084
			},
			"endBinding": {
				"elementId": "7Rm4xL0cdmFLq8cW-BIpC",
				"focus": -0.12754732304118246,
				"gap": 9.807646467159081
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "HYSJWC9a",
			"type": "text",
			"x": 142.70251443227153,
			"y": 319.642150268625,
			"width": 37,
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
			"seed": 465799027,
			"version": 105,
			"versionNonce": 41807965,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "save",
			"rawText": "save",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "8CEqIyCVFZ5SSTbyWk9yN",
			"originalText": "save"
		},
		{
			"id": "D-SfrLm9_9yIYEUtuD_Z6",
			"type": "arrow",
			"x": 31.226928494771528,
			"y": 410.0237697371542,
			"width": 142.35559619297976,
			"height": 3.4583878245584856,
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
			"seed": 1608608349,
			"version": 432,
			"versionNonce": 1932945139,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675570,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					142.35559619297976,
					-3.4583878245584856
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "HJbqu_7O_ZUpQt3L-oN36",
				"focus": 0.23055414116037007,
				"gap": 8.390625000000341
			},
			"endBinding": {
				"elementId": "7Rm4xL0cdmFLq8cW-BIpC",
				"focus": -0.3524275089263157,
				"gap": 12.375506069790603
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "eDwLxc_Ppl9H2dfJS1N_h",
			"type": "arrow",
			"x": 33.52836078643827,
			"y": 497.8114251030298,
			"width": 154.5411160246694,
			"height": 65.58919460443315,
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
			"seed": 1242394835,
			"version": 492,
			"versionNonce": 542314643,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675571,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					154.5411160246694,
					-65.58919460443315
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "1KjOpSEH1eRK9cslDzd_e",
				"focus": 0.509462001352119,
				"gap": 10.692057291667084
			},
			"endBinding": {
				"elementId": "7Rm4xL0cdmFLq8cW-BIpC",
				"focus": -0.43004768751425315,
				"gap": 16.652473010411654
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "94RtGUQq",
			"type": "text",
			"x": -460.4364829635616,
			"y": 443.52919453945833,
			"width": 189,
			"height": 40,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 227691667,
			"version": 185,
			"versionNonce": 19732883,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "* precompute for active\nusers, cache the feeds.",
			"rawText": "* precompute for active\nusers, cache the feeds.",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 34,
			"containerId": null,
			"originalText": "* precompute for active\nusers, cache the feeds."
		},
		{
			"id": "Quo_Dg0JH_uoaExVJj9QU",
			"type": "arrow",
			"x": -583.7535402552282,
			"y": -75.07627421054161,
			"width": 48.76302083333337,
			"height": 97.21028645833343,
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
			"seed": 2036529459,
			"version": 767,
			"versionNonce": 57247283,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675571,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					48.76302083333337,
					97.21028645833343
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "I29l_wrFYhX3JadBt6H_d",
				"focus": 0.23836731311119144,
				"gap": 10.482421875000057
			},
			"endBinding": {
				"elementId": "V-xEinbXSJTga3RyOMI4j",
				"focus": 0.12443731173758399,
				"gap": 10.479300402710859
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "rzTUx1WPDDpUYnB1CRbsn",
			"type": "rectangle",
			"x": -486.039347546895,
			"y": 185.54840026862507,
			"width": 117,
			"height": 46,
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
				"type": 3
			},
			"seed": 1956794845,
			"version": 177,
			"versionNonce": 773484339,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "B1Sz9mJ2"
				},
				{
					"id": "PpUhSYvFWgM-7RAeD6U3_",
					"type": "arrow"
				},
				{
					"id": "65S1RDNZcY32m6Yjp9kqI",
					"type": "arrow"
				},
				{
					"id": "yivKDbnnVpVsm0cKJQN1U",
					"type": "arrow"
				},
				{
					"id": "4nW9v-ktQb_ZWOl4kpi_S",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"id": "B1Sz9mJ2",
			"type": "text",
			"x": -475.539347546895,
			"y": 198.54840026862507,
			"width": 96,
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
			"seed": 2014645075,
			"version": 113,
			"versionNonce": 711823741,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "feed service",
			"rawText": "feed service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "rzTUx1WPDDpUYnB1CRbsn",
			"originalText": "feed service"
		},
		{
			"type": "diamond",
			"version": 294,
			"versionNonce": 1585854483,
			"isDeleted": false,
			"id": "V-xEinbXSJTga3RyOMI4j",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -604.9293215052287,
			"y": 30.17437683112496,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 57,
			"seed": 1696054451,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "VXl7igDL"
				},
				{
					"id": "mHst7whVa98MBHc6YasYp",
					"type": "arrow"
				},
				{
					"id": "h3wroTwqJx-D8QQ7LO4nY",
					"type": "arrow"
				},
				{
					"id": "Quo_Dg0JH_uoaExVJj9QU",
					"type": "arrow"
				},
				{
					"id": "PpUhSYvFWgM-7RAeD6U3_",
					"type": "arrow"
				}
			],
			"updated": 1674946675271,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 271,
			"versionNonce": 1579632285,
			"isDeleted": false,
			"id": "VXl7igDL",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -579.9293215052287,
			"y": 48.67437683112496,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 107,
			"height": 20,
			"seed": 1277149693,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "load balancer",
			"rawText": "load balancer",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "V-xEinbXSJTga3RyOMI4j",
			"originalText": "load balancer"
		},
		{
			"id": "PpUhSYvFWgM-7RAeD6U3_",
			"type": "arrow",
			"x": -499.765910046895,
			"y": 83.8820591227917,
			"width": 66.27604166666663,
			"height": 91.46484375,
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
			"seed": 140994707,
			"version": 346,
			"versionNonce": 1398818771,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675571,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					66.27604166666663,
					91.46484375
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "V-xEinbXSJTga3RyOMI4j",
				"focus": -0.10697777238170768,
				"gap": 6.004543634060443
			},
			"endBinding": {
				"elementId": "rzTUx1WPDDpUYnB1CRbsn",
				"focus": 0.24090038868329222,
				"gap": 10.201497395833371
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "65S1RDNZcY32m6Yjp9kqI",
			"type": "arrow",
			"x": -356.93713400522836,
			"y": 210.65614766445833,
			"width": 558.8997395833334,
			"height": 130.62825520833314,
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
			"seed": 1154561725,
			"version": 448,
			"versionNonce": 642635123,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "0UesJmBm"
				}
			],
			"updated": 1674946675571,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					321.10026041666663,
					17.080078125
				],
				[
					558.8997395833334,
					130.62825520833314
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzTUx1WPDDpUYnB1CRbsn",
				"focus": -0.0631037844953531,
				"gap": 12.102213541666629
			},
			"endBinding": {
				"elementId": "7Rm4xL0cdmFLq8cW-BIpC",
				"focus": 0.6437040096239574,
				"gap": 15.532580199052958
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "0UesJmBm",
			"type": "text",
			"x": -53.83687358856173,
			"y": 217.73622578945833,
			"width": 36,
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
			"seed": 1184387741,
			"version": 105,
			"versionNonce": 1646800115,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "read",
			"rawText": "read",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "65S1RDNZcY32m6Yjp9kqI",
			"originalText": "read"
		},
		{
			"id": "yivKDbnnVpVsm0cKJQN1U",
			"type": "arrow",
			"x": -385.2607017135616,
			"y": 173.5402622477917,
			"width": 323.1738281249999,
			"height": 252.94921874999994,
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
			"seed": 1979137981,
			"version": 355,
			"versionNonce": 192458515,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "859SMYz5"
				}
			],
			"updated": 1674946675571,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					323.1738281249999,
					-252.94921874999994
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzTUx1WPDDpUYnB1CRbsn",
				"focus": -0.027860947101895576,
				"gap": 12.008138020833371
			},
			"endBinding": {
				"elementId": "q7xFDoA5D1lqPsfeDZegJ",
				"focus": 0.17414976843262414,
				"gap": 7.350911458333428
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "859SMYz5",
			"type": "text",
			"x": -295.6737876510617,
			"y": 27.065652872791702,
			"width": 144,
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
			"seed": 930452029,
			"version": 158,
			"versionNonce": 421271187,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "grab profiles\nreferenced in feed",
			"rawText": "grab profiles\nreferenced in feed",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "yivKDbnnVpVsm0cKJQN1U",
			"originalText": "grab profiles\nreferenced in feed"
		},
		{
			"id": "ocMFJdZ9",
			"type": "text",
			"x": -108.90327983856253,
			"y": 539.1639601644584,
			"width": 176,
			"height": 60,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1464420563,
			"version": 205,
			"versionNonce": 658804765,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "* filter users\nby preference, location\nof user.",
			"rawText": "* filter users\nby preference, location\nof user.",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 54,
			"containerId": null,
			"originalText": "* filter users\nby preference, location\nof user."
		},
		{
			"id": "4nW9v-ktQb_ZWOl4kpi_S",
			"type": "arrow",
			"x": -411.54325379689567,
			"y": 243.31239766445833,
			"width": 28.684895833333258,
			"height": 119.41406250000011,
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
			"seed": 1706766547,
			"version": 413,
			"versionNonce": 1700222131,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KeGgDJWL"
				}
			],
			"updated": 1674946675571,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					28.684895833333258,
					119.41406250000011
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "rzTUx1WPDDpUYnB1CRbsn",
				"focus": -0.11941139872562728,
				"gap": 11.763997395833258
			},
			"endBinding": {
				"elementId": "kxnThiWAMGL5XriZaBhI2",
				"focus": -0.11232725122681143,
				"gap": 9.660940160869721
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "KeGgDJWL",
			"type": "text",
			"x": -430.20080588022904,
			"y": 293.0194289144584,
			"width": 66,
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
			"seed": 1260786291,
			"version": 122,
			"versionNonce": 735478909,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "on a job",
			"rawText": "on a job",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "4nW9v-ktQb_ZWOl4kpi_S",
			"originalText": "on a job"
		},
		{
			"id": "TmRi3IrK",
			"type": "text",
			"x": -705.6252850468957,
			"y": 170.0363559977917,
			"width": 221,
			"height": 100,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 91805139,
			"version": 349,
			"versionNonce": 102747603,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674946675271,
			"link": null,
			"locked": false,
			"text": "* for a cache miss, we can\nprioritize generating for a\nuser who's logged in but\ndoesn't have a precomputed\nfeed.",
			"rawText": "* for a cache miss, we can\nprioritize generating for a\nuser who's logged in but\ndoesn't have a precomputed\nfeed.",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 94,
			"containerId": null,
			"originalText": "* for a cache miss, we can\nprioritize generating for a\nuser who's logged in but\ndoesn't have a precomputed\nfeed."
		},
		{
			"id": "sfVgSKwS",
			"type": "text",
			"x": -399.87395537747943,
			"y": -521.0702939302639,
			"width": 378,
			"height": 45,
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
			"seed": 1969687123,
			"version": 138,
			"versionNonce": 605272605,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674948335394,
			"link": null,
			"locked": false,
			"text": "Tinder System Design",
			"rawText": "Tinder System Design",
			"fontSize": 36,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 32,
			"containerId": null,
			"originalText": "Tinder System Design"
		},
		{
			"id": "Ew3_Ov-36YNrbLvyYcSsr",
			"type": "rectangle",
			"x": -1001.1975268205965,
			"y": -88.26540041010463,
			"width": 112,
			"height": 46,
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
				"type": 3
			},
			"seed": 1766865747,
			"version": 196,
			"versionNonce": 1552409843,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "G5iV695C"
				},
				{
					"id": "Zj-dOe3pnZeZ0cN452z_Y",
					"type": "arrow"
				},
				{
					"id": "cLdcwj9ZF4u-WE20m36aG",
					"type": "arrow"
				},
				{
					"id": "ZZBIAg0BVGD93wvjRZjWK",
					"type": "arrow"
				}
			],
			"updated": 1674947386609,
			"link": null,
			"locked": false
		},
		{
			"id": "G5iV695C",
			"type": "text",
			"x": -992.6975268205965,
			"y": -75.26540041010463,
			"width": 95,
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
			"seed": 2095401501,
			"version": 172,
			"versionNonce": 2081118141,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386609,
			"link": null,
			"locked": false,
			"text": "likes service",
			"rawText": "likes service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "Ew3_Ov-36YNrbLvyYcSsr",
			"originalText": "likes service"
		},
		{
			"id": "Zj-dOe3pnZeZ0cN452z_Y",
			"type": "arrow",
			"x": -640.8040217759592,
			"y": -107.77360297569165,
			"width": 239.03517283843257,
			"height": 35.63817139720177,
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
			"seed": 571490877,
			"version": 305,
			"versionNonce": 933451805,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "HP4R7KPK"
				}
			],
			"updated": 1674947386609,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-239.03517283843257,
					35.63817139720177
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "I29l_wrFYhX3JadBt6H_d",
				"focus": 0.26484482355657657,
				"gap": 6.256861729063758
			},
			"endBinding": {
				"elementId": "Ew3_Ov-36YNrbLvyYcSsr",
				"focus": 0.09168854172293295,
				"gap": 9.35833220620475
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "HP4R7KPK",
			"type": "text",
			"x": -853.8758283350671,
			"y": -75.59108112627445,
			"width": 100,
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
			"seed": 1239012541,
			"version": 15,
			"versionNonce": 1370273011,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947201506,
			"link": null,
			"locked": false,
			"text": "like a profile",
			"rawText": "like a profile",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "Zj-dOe3pnZeZ0cN452z_Y",
			"originalText": "like a profile"
		},
		{
			"id": "wS5kgvg5stUln1cWokBTj",
			"type": "ellipse",
			"x": -1289.2030702368581,
			"y": 91.5191223591251,
			"width": 138,
			"height": 70,
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
			"seed": 1696738141,
			"version": 202,
			"versionNonce": 1256907005,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "pNmP36XD"
				},
				{
					"id": "cLdcwj9ZF4u-WE20m36aG",
					"type": "arrow"
				},
				{
					"id": "lmuPIiYD4XHKfPx4iBTsa",
					"type": "arrow"
				}
			],
			"updated": 1674947611360,
			"link": null,
			"locked": false
		},
		{
			"id": "pNmP36XD",
			"type": "text",
			"x": -1272.2030702368581,
			"y": 106.5191223591251,
			"width": 104,
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
			"seed": 341729619,
			"version": 197,
			"versionNonce": 1450015059,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947611361,
			"link": null,
			"locked": false,
			"text": "likes/dislikes \ndatabase",
			"rawText": "likes/dislikes database",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "wS5kgvg5stUln1cWokBTj",
			"originalText": "likes/dislikes database"
		},
		{
			"id": "ITY1uS4q",
			"type": "text",
			"x": -1284.1535872149307,
			"y": 171.15819024455476,
			"width": 96,
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
			"seed": 1358694045,
			"version": 173,
			"versionNonce": 1082593597,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "user1, user2",
			"rawText": "user1, user2",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 14,
			"containerId": null,
			"originalText": "user1, user2"
		},
		{
			"id": "cLdcwj9ZF4u-WE20m36aG",
			"type": "arrow",
			"x": -1009.6767773177589,
			"y": -40.576937084670476,
			"width": 185.4254575316204,
			"height": 125.06477905530117,
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
			"seed": 1820471923,
			"version": 427,
			"versionNonce": 1157014035,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RNFh8Gfk"
				}
			],
			"updated": 1674947611359,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-185.4254575316204,
					125.06477905530117
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Ew3_Ov-36YNrbLvyYcSsr",
				"gap": 8.64572711777123,
				"focus": 0.30937934042358933
			},
			"endBinding": {
				"elementId": "wS5kgvg5stUln1cWokBTj",
				"gap": 9.245872939779638,
				"focus": -0.43484163989690666
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "RNFh8Gfk",
			"type": "text",
			"x": -1167.1517105856199,
			"y": 2.456057274057521,
			"width": 119,
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
			"seed": 113525907,
			"version": 143,
			"versionNonce": 929816989,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "save like in db,\nemit like event.",
			"rawText": "save like in db,\nemit like event.",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "cLdcwj9ZF4u-WE20m36aG",
			"originalText": "save like in db,\nemit like event."
		},
		{
			"id": "4hE2F0ZTQ7Zb-3QCfqp_7",
			"type": "rectangle",
			"x": -1087.085118068891,
			"y": -322.9297588657031,
			"width": 119,
			"height": 50,
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
				"type": 3
			},
			"seed": 432652445,
			"version": 167,
			"versionNonce": 1982046909,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "6zQmDg2M"
				},
				{
					"id": "ZZBIAg0BVGD93wvjRZjWK",
					"type": "arrow"
				},
				{
					"id": "SQs4ddQu9Cy-K5LUN6K2b",
					"type": "arrow"
				},
				{
					"id": "zYGmgpXo81QCUB0x47zVb",
					"type": "arrow"
				},
				{
					"id": "lmuPIiYD4XHKfPx4iBTsa",
					"type": "arrow"
				}
			],
			"updated": 1674947412130,
			"link": null,
			"locked": false
		},
		{
			"id": "6zQmDg2M",
			"type": "text",
			"x": -1081.585118068891,
			"y": -307.9297588657031,
			"width": 108,
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
			"seed": 1364984605,
			"version": 129,
			"versionNonce": 773301757,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "match service",
			"rawText": "match service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "4hE2F0ZTQ7Zb-3QCfqp_7",
			"originalText": "match service"
		},
		{
			"id": "ZZBIAg0BVGD93wvjRZjWK",
			"type": "arrow",
			"x": -958.4521906351372,
			"y": -99.08030712038521,
			"width": 57.589410557533256,
			"height": 165.1532104457271,
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
			"seed": 1064973491,
			"version": 319,
			"versionNonce": 1636550803,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "RZ0RoLPo"
				}
			],
			"updated": 1674947387798,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-57.589410557533256,
					-165.1532104457271
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Ew3_Ov-36YNrbLvyYcSsr",
				"focus": -0.022856958582648954,
				"gap": 10.814906710280582
			},
			"endBinding": {
				"elementId": "4hE2F0ZTQ7Zb-3QCfqp_7",
				"focus": 0.0030265168945683898,
				"gap": 8.696241299590781
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "RZ0RoLPo",
			"type": "text",
			"x": -1077.3822566095948,
			"y": -193.32705714281695,
			"width": 177,
			"height": 60,
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
			"seed": 1201729203,
			"version": 115,
			"versionNonce": 200199059,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "on like event,\ncheck if it creates a \nmatch",
			"rawText": "on like event,\ncheck if it creates a match",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 54,
			"containerId": "ZZBIAg0BVGD93wvjRZjWK",
			"originalText": "on like event,\ncheck if it creates a match"
		},
		{
			"id": "SympGkijdQ7gsc5Z6AFRO",
			"type": "ellipse",
			"x": -1388.6311713590628,
			"y": -239.78776159954037,
			"width": 112,
			"height": 73,
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
			"seed": 1767147261,
			"version": 148,
			"versionNonce": 132360989,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "55qO8EPM"
				},
				{
					"id": "SQs4ddQu9Cy-K5LUN6K2b",
					"type": "arrow"
				}
			],
			"updated": 1674947386610,
			"link": null,
			"locked": false
		},
		{
			"id": "55qO8EPM",
			"type": "text",
			"x": -1371.1311713590628,
			"y": -223.28776159954037,
			"width": 77,
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
			"seed": 72972467,
			"version": 136,
			"versionNonce": 433447219,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "matches \ndatabase",
			"rawText": "matches database",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "SympGkijdQ7gsc5Z6AFRO",
			"originalText": "matches database"
		},
		{
			"id": "SQs4ddQu9Cy-K5LUN6K2b",
			"type": "arrow",
			"x": -1097.46628466656,
			"y": -293.9968006941604,
			"width": 186.29088677588265,
			"height": 60.01518668003894,
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
			"seed": 1014995955,
			"version": 281,
			"versionNonce": 214646323,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "ULECbezX"
				}
			],
			"updated": 1674947387798,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-186.29088677588265,
					60.01518668003894
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4hE2F0ZTQ7Zb-3QCfqp_7",
				"focus": 0.42065909713343397,
				"gap": 10.38116659766888
			},
			"endBinding": {
				"elementId": "SympGkijdQ7gsc5Z6AFRO",
				"focus": -0.3671527875719037,
				"gap": 9.377828936218684
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "ULECbezX",
			"type": "text",
			"x": -1205.8876867006472,
			"y": -284.07349507550197,
			"width": 91,
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
			"seed": 1221377555,
			"version": 75,
			"versionNonce": 2025801693,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "save match",
			"rawText": "save match",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "SQs4ddQu9Cy-K5LUN6K2b",
			"originalText": "save match"
		},
		{
			"id": "uXM_3z3T1dv-tp372HYet",
			"type": "rectangle",
			"x": -841.5739664351183,
			"y": -460.2552270586165,
			"width": 119,
			"height": 55,
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
				"type": 3
			},
			"seed": 2066715965,
			"version": 119,
			"versionNonce": 1805611123,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fKy96TDi"
				},
				{
					"id": "zYGmgpXo81QCUB0x47zVb",
					"type": "arrow"
				},
				{
					"id": "S-CnEOVxW0pbROHhZwqyj",
					"type": "arrow"
				}
			],
			"updated": 1674947386610,
			"link": null,
			"locked": false
		},
		{
			"id": "fKy96TDi",
			"type": "text",
			"x": -830.5739664351183,
			"y": -452.7552270586165,
			"width": 97,
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
			"seed": 1432162301,
			"version": 103,
			"versionNonce": 883180605,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"text": "notification \nservice",
			"rawText": "notification service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "uXM_3z3T1dv-tp372HYet",
			"originalText": "notification service"
		},
		{
			"id": "zYGmgpXo81QCUB0x47zVb",
			"type": "arrow",
			"x": -967.152023238413,
			"y": -330.710687613119,
			"width": 116.74950499672536,
			"height": 76.78886512365034,
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
			"seed": 780678611,
			"version": 265,
			"versionNonce": 936050643,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "OIIalM3N"
				}
			],
			"updated": 1674947387798,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					116.74950499672536,
					-76.78886512365034
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4hE2F0ZTQ7Zb-3QCfqp_7",
				"focus": 0.10863606560239572,
				"gap": 7.780928747415885
			},
			"endBinding": {
				"elementId": "uXM_3z3T1dv-tp372HYet",
				"focus": 0.2954264461892024,
				"gap": 8.828551806569294
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "OIIalM3N",
			"type": "text",
			"x": -987.1022754492494,
			"y": -376.9896147405438,
			"width": 165,
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
			"seed": 1991552595,
			"version": 85,
			"versionNonce": 602128723,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947386611,
			"link": null,
			"locked": false,
			"text": "notify user of match",
			"rawText": "notify user of match",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "zYGmgpXo81QCUB0x47zVb",
			"originalText": "notify user of match"
		},
		{
			"id": "S-CnEOVxW0pbROHhZwqyj",
			"type": "arrow",
			"x": -731.6811382639048,
			"y": -396.05276349683857,
			"width": 106.48823234764939,
			"height": 257.50903868615467,
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
			"seed": 2016750035,
			"version": 198,
			"versionNonce": 1363029939,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "N6JwKfEi"
				}
			],
			"updated": 1674947386610,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					106.48823234764939,
					257.50903868615467
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "uXM_3z3T1dv-tp372HYet",
				"focus": -0.49697069890454126,
				"gap": 9.20246356177796
			},
			"endBinding": {
				"elementId": "I29l_wrFYhX3JadBt6H_d",
				"focus": -0.4591203802675842,
				"gap": 7.985028725142229
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "N6JwKfEi",
			"type": "text",
			"x": -760.0480002744819,
			"y": -304.46926367677804,
			"width": 70,
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
			"seed": 1503438845,
			"version": 43,
			"versionNonce": 787220595,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947373267,
			"link": null,
			"locked": false,
			"text": "you got \na match!",
			"rawText": "you got \na match!",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "S-CnEOVxW0pbROHhZwqyj",
			"originalText": "you got \na match!"
		},
		{
			"id": "lmuPIiYD4XHKfPx4iBTsa",
			"type": "arrow",
			"x": -1079.4578853684382,
			"y": -262.6629014441013,
			"width": 128.55604253201614,
			"height": 345.4783472540036,
			"angle": 0,
			"strokeColor": "#d9480f",
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
			"seed": 480349555,
			"version": 200,
			"versionNonce": 1084155827,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yFAM1LKt"
				}
			],
			"updated": 1674947611360,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-128.55604253201614,
					345.4783472540036
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "4hE2F0ZTQ7Zb-3QCfqp_7",
				"gap": 10.266857421601799,
				"focus": 0.5631984711791952
			},
			"endBinding": {
				"elementId": "wS5kgvg5stUln1cWokBTj",
				"gap": 9.193941747063946,
				"focus": -0.06467911050949872
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "yFAM1LKt",
			"type": "text",
			"x": -1195.2394363994013,
			"y": -99.69486321650584,
			"width": 90,
			"height": 20,
			"angle": 0,
			"strokeColor": "#d9480f",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1059793619,
			"version": 14,
			"versionNonce": 1979478749,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674947421304,
			"link": null,
			"locked": false,
			"text": "check likes?",
			"rawText": "check likes?",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "lmuPIiYD4XHKfPx4iBTsa",
			"originalText": "check likes?"
		},
		{
			"id": "ouVseCINFe68lD3fMNUUH",
			"type": "ellipse",
			"x": 144.6828863635244,
			"y": 185.12822809455923,
			"width": 109,
			"height": 56,
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
			"seed": 1106938291,
			"version": 426,
			"versionNonce": 1753469533,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "YnoStR6k"
				},
				{
					"id": "P1eAV9joFfWdeIqtbzmES",
					"type": "arrow"
				},
				{
					"id": "ODeOyMYJJDHYax6X_1j_Q",
					"type": "arrow"
				}
			],
			"updated": 1674948147249,
			"link": null,
			"locked": false
		},
		{
			"id": "YnoStR6k",
			"type": "text",
			"x": 160.6828863635244,
			"y": 193.12822809455923,
			"width": 77,
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
			"seed": 362895133,
			"version": 419,
			"versionNonce": 807325171,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674948147249,
			"link": null,
			"locked": false,
			"text": "image \ndatabase",
			"rawText": "image database",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "ouVseCINFe68lD3fMNUUH",
			"originalText": "image database"
		},
		{
			"id": "ODeOyMYJJDHYax6X_1j_Q",
			"type": "arrow",
			"x": 263.83172731186124,
			"y": 104.7257804067471,
			"width": 46.45420868986622,
			"height": 69.32086781224496,
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
			"seed": 961369331,
			"version": 777,
			"versionNonce": 816065843,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674948147250,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-46.45420868986622,
					69.32086781224496
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "Wbt35Utay8pVyYWB8KBcg",
				"focus": 0.05950493707273758,
				"gap": 9.366924397230278
			},
			"endBinding": {
				"elementId": "ouVseCINFe68lD3fMNUUH",
				"focus": -0.13871060192702725,
				"gap": 12.602630052153799
			},
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "YC1rFsZd",
			"type": "text",
			"x": -114.6656222331942,
			"y": -193.39576270564862,
			"width": 229,
			"height": 40,
			"angle": 0,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"roundness": null,
			"seed": 1496346237,
			"version": 136,
			"versionNonce": 1389929757,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674948362834,
			"link": null,
			"locked": false,
			"text": "* authentication can be\ndone in a separate gateway.",
			"rawText": "* authentication can be\ndone in a separate gateway.",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 34,
			"containerId": null,
			"originalText": "* authentication can be\ndone in a separate gateway."
		},
		{
			"id": "cm69ZQMP",
			"type": "text",
			"x": -1006.8430845263454,
			"y": 381.0129449969965,
			"width": 476,
			"height": 100,
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
			"seed": 1792906867,
			"version": 329,
			"versionNonce": 453558269,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674957793888,
			"link": null,
			"locked": false,
			"text": "* we might not to precompute these feeds\nfor users, maybe we can just geographically\nshard our user databases, and then filter\non those databases based on user preferences.",
			"rawText": "* we might not to precompute these feeds\nfor users, maybe we can just geographically\nshard our user databases, and then filter\non those databases based on user preferences.",
			"fontSize": 20,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 93,
			"containerId": null,
			"originalText": "* we might not to precompute these feeds\nfor users, maybe we can just geographically\nshard our user databases, and then filter\non those databases based on user preferences."
		},
		{
			"id": "zg-rvWTexiGamPF46QJIG",
			"type": "rectangle",
			"x": -1030.0107974091889,
			"y": 356.974410851959,
			"width": 513.3574545957417,
			"height": 152.85830143330884,
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
				"type": 3
			},
			"seed": 1493051443,
			"version": 85,
			"versionNonce": 115411539,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674957793888,
			"link": null,
			"locked": false
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
		"currentItemFontSize": 20,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": "arrow",
		"currentItemEndArrowhead": "arrow",
		"scrollX": 2068.4895763512077,
		"scrollY": 447.7885885359164,
		"zoom": {
			"value": 0.8679913766926646
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