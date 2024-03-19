---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
job ^yQueqvX5

id: primary key
interval: int
scheduled_at: date
completed_at: date
retry_policy: RetryPolicyEnum ^wEdTJunX

Task
Scheduler ^7oWb8udb

grab jobs
for time
slot ^845AoZgZ

on an interval ^W369xFpO

client ^PF1JIsJB

worker nodes ^Q1SmFqUk

Load
Balancer ^o1lisKqr

Job
Scheduler ^zwLP5bOU

Enqueue
Service ^22t2GlxM

jobs shard 2 ^mswUPzxZ

jobs shard 0 ^JeKpWfgo

jobs shard 1 ^KcAYUJp0

Orchestrator ^6vzYPLym

shard health,
redirecting requests
to shards ^zqXpuWPK

Task
Scheduler ^3uSqLfz3

grab jobs
for time
slot ^TwH9GZr4

post job
to queue ^915ZA3ze

grab jobs ^VtF7QMcY

update job
status? ^lxklzhpd

in-memory message broker ^qLXZtNfG

output object store ^KJ1ySnWj

distributed
lock service ^Es6hPJ6F

request
lock on jobId ^fxFCoaaG

heartbeat ^WeKA25v5

write
new jobs ^PTJ7YYy2

database
links to this ^aLiokkeq

read in data
when processing job ^CTb4yOfh

input object store ^NmxZ6ocz

write output
to object store ^KIQQK9DV

database links
to this for job output ^53CZXVoz

in-memory because durability/retry
logic is handled by the task scheduler
along with the jobs database. ^przj2y1M

%%
# Drawing
```json
{
	"type": "excalidraw",
	"version": 2,
	"source": "https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.0.18",
	"elements": [
		{
			"type": "ellipse",
			"version": 563,
			"versionNonce": 566555170,
			"isDeleted": false,
			"id": "7j5FQDPTS3baFkwDabAEd",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 397.74696690543783,
			"y": 479.00715775821334,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 243.06085773920586,
			"height": 243.06085773920586,
			"seed": 2050577251,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"id": "Ccl5t2mU9wO8JAyRV4Zii",
					"type": "arrow"
				},
				{
					"id": "VihqTQBgWdnFOBYkeF9fw",
					"type": "arrow"
				}
			],
			"updated": 1710738126868,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1120,
			"versionNonce": 1436256930,
			"isDeleted": false,
			"id": "w8YaTO6FsjrgScvL8VkeS",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 634.5592028586544,
			"y": 350.79272314081027,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 270.12152099609375,
			"height": 149.41595458984375,
			"seed": 1987996900,
			"groupIds": [
				"RHWBtJl9Mzd_CA6we4wLF"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 1092,
			"versionNonce": 196175998,
			"isDeleted": false,
			"id": "ZkBoQFYJ9SwDA0TggIgqm",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 636.9845568625607,
			"y": 389.34933324823214,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 269.38385009765625,
			"height": 1.72381591796875,
			"seed": 627519588,
			"groupIds": [
				"RHWBtJl9Mzd_CA6we4wLF"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					269.38385009765625,
					-1.72381591796875
				]
			]
		},
		{
			"type": "text",
			"version": 990,
			"versionNonce": 1356195426,
			"isDeleted": false,
			"id": "yQueqvX5",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 648.5003710421202,
			"y": 355.4463336185595,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 27.799972534179688,
			"height": 25,
			"seed": 1304486620,
			"groupIds": [
				"RHWBtJl9Mzd_CA6we4wLF"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"fontSize": 20,
			"fontFamily": 1,
			"text": "job",
			"rawText": "job",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "job",
			"lineHeight": 1.25,
			"baseline": 17
		},
		{
			"type": "text",
			"version": 1185,
			"versionNonce": 1017882814,
			"isDeleted": false,
			"id": "wEdTJunX",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 642.2347461287727,
			"y": 394.78693345584895,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 227.32785034179688,
			"height": 100,
			"seed": 1809941852,
			"groupIds": [
				"RHWBtJl9Mzd_CA6we4wLF"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "id: primary key\ninterval: int\nscheduled_at: date\ncompleted_at: date\nretry_policy: RetryPolicyEnum",
			"rawText": "id: primary key\ninterval: int\nscheduled_at: date\ncompleted_at: date\nretry_policy: RetryPolicyEnum",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "id: primary key\ninterval: int\nscheduled_at: date\ncompleted_at: date\nretry_policy: RetryPolicyEnum",
			"lineHeight": 1.25,
			"baseline": 94
		},
		{
			"type": "line",
			"version": 6401,
			"versionNonce": 1942932002,
			"isDeleted": false,
			"id": "oIwpAbclmN7BSFCdXw1yZ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 479.1628165951712,
			"y": 435.332110312934,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 75.01121630306868,
			"height": 96.81388324216653,
			"seed": 227389699,
			"groupIds": [
				"kXOe3SVESHRelKo_XHczn",
				"al2ggyopUYHD85PQ3kSOM",
				"u2RnBFpEoYVGeuxOQlyOC"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.24734846976242794,
					73.1714082159101
				],
				[
					0.011575327725072006,
					81.50165529728328
				],
				[
					3.8632435379119165,
					85.10105205208878
				],
				[
					17.276485894102954,
					88.14730719194147
				],
				[
					39.948665011120255,
					89.0958655364321
				],
				[
					61.61043288740646,
					87.58135319133916
				],
				[
					73.11948965218787,
					83.95942431004657
				],
				[
					74.74268637210398,
					80.90610026776591
				],
				[
					74.9706584753909,
					74.19947908967055
				],
				[
					74.79172688269483,
					6.138672737165569
				],
				[
					74.38835763792527,
					-0.2918194398554754
				],
				[
					69.57188081608908,
					-3.885863818744892
				],
				[
					59.42940850758881,
					-5.967344146345569
				],
				[
					36.31608449133351,
					-7.7180177057344235
				],
				[
					17.785060590062127,
					-6.674087120295436
				],
				[
					3.210536142559118,
					-3.1332019499277424
				],
				[
					-0.04055782767777212,
					-0.04396604849106378
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "ellipse",
			"version": 7124,
			"versionNonce": 217309438,
			"isDeleted": false,
			"id": "gkrG0qjGYD_EDASgwSWoN",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 479.42874918585517,
			"y": 426.57914215690596,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 74.53008207714048,
			"height": 15.073148387271289,
			"seed": 1935055011,
			"groupIds": [
				"kXOe3SVESHRelKo_XHczn",
				"al2ggyopUYHD85PQ3kSOM",
				"u2RnBFpEoYVGeuxOQlyOC"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "q1WtUcMNzcj6u3qQIyc8u",
					"type": "arrow"
				}
			],
			"updated": 1710738077492,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 846,
			"versionNonce": 1433744866,
			"isDeleted": false,
			"id": "q1WtUcMNzcj6u3qQIyc8u",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 275.96193546632395,
			"y": 231.35498642230465,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 236.02888739113195,
			"height": 182.48485599926897,
			"seed": 1541817133,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "TwH9GZr4"
				}
			],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"startBinding": {
				"focus": -0.21115531649691058,
				"gap": 11.132709764955962,
				"elementId": "vMrJ3O9Mkm8Fh1XzHnTO8"
			},
			"endBinding": {
				"focus": 0.35156212105484147,
				"gap": 12.8292494081193,
				"elementId": "gkrG0qjGYD_EDASgwSWoN"
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
					106.00781023562018,
					36.13598689239211
				],
				[
					236.02888739113195,
					182.48485599926897
				]
			]
		},
		{
			"type": "text",
			"version": 41,
			"versionNonce": 1342902590,
			"isDeleted": false,
			"id": "TwH9GZr4",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 306.97207526693836,
			"y": 404.46080414519906,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 72.62393188476562,
			"height": 60,
			"seed": 368006541,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "grab jobs\nfor time\nslot",
			"rawText": "grab jobs\nfor time\nslot",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "q1WtUcMNzcj6u3qQIyc8u",
			"originalText": "grab jobs\nfor time\nslot",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "arrow",
			"version": 1430,
			"versionNonce": 1457007010,
			"isDeleted": false,
			"id": "nexOo5DKK0bpzkY6JQGem",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -518.7136738023376,
			"y": 435.2002800705453,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 97.22681011595671,
			"height": 1.8286593338929151,
			"seed": 1304309732,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GtNe7mP1ndW_AGfpdWS_N",
				"gap": 9.720973726251657,
				"focus": 0.30109064058782037
			},
			"endBinding": {
				"elementId": "Qu_VMS2JGfB4EyI63jG9t",
				"gap": 11.24064274609077,
				"focus": 0.07532437967055533
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
					97.22681011595671,
					-1.8286593338929151
				]
			]
		},
		{
			"type": "arrow",
			"version": 1654,
			"versionNonce": 1095907710,
			"isDeleted": false,
			"id": "f3bZbY9qTeWu5dcC_qWxS",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 453.45438449631695,
			"y": 148.76321808718072,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 32.780435849871424,
			"height": 94.45118037938352,
			"seed": 10531164,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "W369xFpO",
				"focus": -1.0888693420540496,
				"gap": 8.865133361902508
			},
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					14.597924627840825,
					43.79430833704933
				],
				[
					-18.182511222030598,
					94.45118037938352
				]
			]
		},
		{
			"type": "text",
			"version": 592,
			"versionNonce": 1596368226,
			"isDeleted": false,
			"id": "W369xFpO",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 335.2132898307035,
			"y": 137.63661936712384,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 109.37596130371094,
			"height": 20,
			"seed": 1976320220,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "f3bZbY9qTeWu5dcC_qWxS",
					"type": "arrow"
				}
			],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "on an interval",
			"rawText": "on an interval",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "on an interval",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 1246,
			"versionNonce": 134896062,
			"isDeleted": false,
			"id": "GtNe7mP1ndW_AGfpdWS_N",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -656.318483260728,
			"y": 386.43283478724754,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 127.88383573213892,
			"height": 76.53703389977764,
			"seed": 635831644,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "nexOo5DKK0bpzkY6JQGem",
					"type": "arrow"
				}
			],
			"updated": 1710738077492,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 1031,
			"versionNonce": 397388066,
			"isDeleted": false,
			"id": "zrn8nIvTsxIfJQhNiqLPs",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -657.3940810116233,
			"y": 397.1493691794917,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 128.84193229844433,
			"height": 0,
			"seed": 1312094684,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					128.84193229844433,
					0
				]
			]
		},
		{
			"type": "ellipse",
			"version": 851,
			"versionNonce": 995389950,
			"isDeleted": false,
			"id": "0KHgnpClLS73Qu-AgiXDb",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"angle": 0,
			"x": -651.8304477917732,
			"y": 390.70440458725636,
			"strokeColor": "#000000",
			"backgroundColor": "#fa5252",
			"width": 5.001953125,
			"height": 5.001953125,
			"seed": 1773231708,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077492,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 896,
			"versionNonce": 669136098,
			"isDeleted": false,
			"id": "C3-zBYOBirOS6mOQZo7rT",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"angle": 0,
			"x": -641.5677524792732,
			"y": 390.70440458725636,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 5.001953125,
			"height": 5.001953125,
			"seed": 288174812,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 954,
			"versionNonce": 1714520638,
			"isDeleted": false,
			"id": "fqwguLjwKsRUipBBVKqsY",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"angle": 0,
			"x": -630.854336012927,
			"y": 391.15512574110255,
			"strokeColor": "#000000",
			"backgroundColor": "#40c057",
			"width": 5.001953125,
			"height": 5.001953125,
			"seed": 1933211484,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 1233,
			"versionNonce": 1900890274,
			"isDeleted": false,
			"id": "6_Om5gi2kSx19zTpATb1H",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 90,
			"angle": 0,
			"x": -614.8272750232998,
			"y": 407.2074946191184,
			"strokeColor": "#000000",
			"backgroundColor": "#04aaf7",
			"width": 42.72020253937572,
			"height": 42.72020253937572,
			"seed": 472591324,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 1850,
			"versionNonce": 193104510,
			"isDeleted": false,
			"id": "WDvXV7HPEOTPc-pyb95Yd",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 100,
			"angle": 0,
			"x": -587.7491109613242,
			"y": 423.431846683576,
			"strokeColor": "#087f5b",
			"backgroundColor": "#40c057",
			"width": 28.226201983883442,
			"height": 24.44112284281997,
			"seed": 1041322076,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-1.8305638688608794,
					-0.4146385831511896
				],
				[
					-7.572250391862635,
					-6.271625431345418
				],
				[
					-11.35769254157424,
					-4.347633009945142
				],
				[
					-12.611765400987878,
					2.3733287939365098
				],
				[
					-11.26889653301009,
					6.740045588043412
				],
				[
					-17.42450906516472,
					8.886103861507927
				],
				[
					-17.203202089974113,
					13.643170786196503
				],
				[
					-12.380895778721076,
					13.349974465892952
				],
				[
					-8.695178377089249,
					9.477701170522828
				],
				[
					-3.6201449645383086,
					17.867626643824725
				],
				[
					-0.415292101592283,
					18.169497411474552
				],
				[
					-3.7772455950748833,
					4.800439161419844
				],
				[
					1.3865838260401944,
					4.3476330099451115
				],
				[
					3.162503997323137,
					5.86739618500973
				],
				[
					9.236150983110862,
					5.86739618500973
				],
				[
					10.80169291871872,
					0.6349695457461695
				],
				[
					4.221225637895673,
					1.1103292603211785
				],
				[
					5.486227236824892,
					-5.759833037916143
				],
				[
					2.472627315401658,
					-5.345194454764953
				],
				[
					-0.23770008446403423,
					-0.9229611976419838
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "line",
			"version": 1270,
			"versionNonce": 1268769890,
			"isDeleted": false,
			"id": "urGSTHIhJlFP1WOy42SZd",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 90,
			"angle": 0,
			"x": -613.7682125492722,
			"y": 428.1703681822994,
			"strokeColor": "#000000",
			"backgroundColor": "#99bcff",
			"width": 42.095115772272244,
			"height": 0,
			"seed": 2025776348,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					42.095115772272244,
					0
				]
			]
		},
		{
			"type": "line",
			"version": 3477,
			"versionNonce": 705202878,
			"isDeleted": false,
			"id": "sDnG_kUDqmwjWwx2XPTTS",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 90,
			"angle": 0,
			"x": -608.6728835194979,
			"y": 412.73583925533325,
			"strokeColor": "#000000",
			"backgroundColor": "#99bcff",
			"width": 29.31860660384862,
			"height": 5.711199931375845,
			"seed": 566618460,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.7724193963150375,
					2.2765797384357125
				],
				[
					4.103544916365185,
					4.186609221587683
				],
				[
					8.536129150893453,
					5.343311508306209
				],
				[
					15.480325949120388,
					5.448716592152419
				],
				[
					23.583965316012858,
					4.712296432964328
				],
				[
					28.316582284417855,
					2.033216518393959
				],
				[
					29.31860660384862,
					-0.2624833392234258
				]
			]
		},
		{
			"type": "ellipse",
			"version": 1294,
			"versionNonce": 1084819490,
			"isDeleted": false,
			"id": "vssrW2N7sl0CTOQnyHfaV",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 90,
			"angle": 0,
			"x": -600.5989675955784,
			"y": 405.8249649895257,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 15.528434353116108,
			"height": 44.82230388130942,
			"seed": 209214940,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 3682,
			"versionNonce": 1080328958,
			"isDeleted": false,
			"id": "6oG8LyqkyMryldJCkT78g",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 0,
			"opacity": 90,
			"angle": 0,
			"x": -607.156932009872,
			"y": 444.47293131377415,
			"strokeColor": "#000000",
			"backgroundColor": "#99bcff",
			"width": 29.31860660384862,
			"height": 5.896061363392446,
			"seed": 1374175836,
			"groupIds": [
				"U9Rr-_5P17BpkW7HEANYv",
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					4.103544916365185,
					-4.322122351104391
				],
				[
					8.536129150893453,
					-5.516265043290966
				],
				[
					15.480325949120388,
					-5.625081903117008
				],
				[
					23.583965316012858,
					-4.8648251269605955
				],
				[
					28.316582284417855,
					-2.0990281379671547
				],
				[
					29.31860660384862,
					0.2709794602754383
				]
			]
		},
		{
			"type": "text",
			"version": 471,
			"versionNonce": 1213707234,
			"isDeleted": false,
			"id": "PF1JIsJB",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -614.5085196591042,
			"y": 472.45347810282635,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 41.00798034667969,
			"height": 20,
			"seed": 617534172,
			"groupIds": [
				"NzuHvbIiVHkfIzwV1caB6"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client",
			"rawText": "client",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "client",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 1250,
			"versionNonce": 922624354,
			"isDeleted": false,
			"id": "9qNpybOUKHPQcIZZBTTFx",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -444.68059082895365,
			"y": 182.32320954034327,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 70.81644178885557,
			"height": 108.30428902193904,
			"seed": 2010730332,
			"groupIds": [
				"JDwCWvUjUy7ANhk0K7xYw",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "GhuZxlqNaE6EyOiWBnEJb",
					"type": "arrow"
				},
				{
					"id": "eVKV9HM-J-EfYfX6oI8s4",
					"type": "arrow"
				}
			],
			"updated": 1710738083522,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1396,
			"versionNonce": 79357858,
			"isDeleted": false,
			"id": "EwdVFNqslmaHMDXmP7smJ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -436.57288673886205,
			"y": 190.5803908907402,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 55.801163535143246,
			"height": 82.83278895375764,
			"seed": 1462698972,
			"groupIds": [
				"JDwCWvUjUy7ANhk0K7xYw",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 1442,
			"versionNonce": 1719819134,
			"isDeleted": false,
			"id": "G0r-25UGcj7MdirbmBVpF",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -414.3862169745099,
			"y": 276.95807401332496,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 11.427824006438863,
			"height": 11.427824006438863,
			"seed": 450504796,
			"groupIds": [
				"JDwCWvUjUy7ANhk0K7xYw",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1089,
			"versionNonce": 2114036578,
			"isDeleted": false,
			"id": "vkHQAKqeBaDzKNGcnSh2q",
			"fillStyle": "cross-hatch",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -428.29319633889156,
			"y": 201.12454756688038,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 39.2417827352022,
			"height": 19.889460471185775,
			"seed": 1991032028,
			"groupIds": [
				"JDwCWvUjUy7ANhk0K7xYw",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1131,
			"versionNonce": 384187326,
			"isDeleted": false,
			"id": "Nd0YFM_-xN87lU-njDbk_",
			"fillStyle": "cross-hatch",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -428.29319633889156,
			"y": 236.6823076118348,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 39.2417827352022,
			"height": 19.889460471185775,
			"seed": 1413005660,
			"groupIds": [
				"JDwCWvUjUy7ANhk0K7xYw",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1543,
			"versionNonce": 1585112866,
			"isDeleted": false,
			"id": "qqyOcYtv3rHRZgmgCZgVy",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -436.50325813697077,
			"y": 175.2818448118195,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 70.81644178885557,
			"height": 108.30428902193904,
			"seed": 155524964,
			"groupIds": [
				"hpLgpp7U-ZVgW5lUecsK_",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1693,
			"versionNonce": 140776446,
			"isDeleted": false,
			"id": "8plRHe0Isjk1RFAbFtCmh",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -428.39555404687917,
			"y": 183.53902616221643,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 55.801163535143246,
			"height": 82.83278895375764,
			"seed": 1102287588,
			"groupIds": [
				"hpLgpp7U-ZVgW5lUecsK_",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 1739,
			"versionNonce": 781562594,
			"isDeleted": false,
			"id": "mibxLfQa3HoZkLH_AM8bD",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -406.20888428252704,
			"y": 269.9167092848012,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 11.427824006438863,
			"height": 11.427824006438863,
			"seed": 1527223908,
			"groupIds": [
				"hpLgpp7U-ZVgW5lUecsK_",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1386,
			"versionNonce": 1962730558,
			"isDeleted": false,
			"id": "WZdOQ2oqTec_EjA_cvYSX",
			"fillStyle": "cross-hatch",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -420.1158636469087,
			"y": 194.0831828383566,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 39.2417827352022,
			"height": 19.889460471185775,
			"seed": 1108290020,
			"groupIds": [
				"hpLgpp7U-ZVgW5lUecsK_",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1428,
			"versionNonce": 283182754,
			"isDeleted": false,
			"id": "j-7oq9Qcw_dGb-PrRF76G",
			"fillStyle": "cross-hatch",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -420.1158636469087,
			"y": 229.64094288331103,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 39.2417827352022,
			"height": 19.889460471185775,
			"seed": 433605988,
			"groupIds": [
				"hpLgpp7U-ZVgW5lUecsK_",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1623,
			"versionNonce": 781298814,
			"isDeleted": false,
			"id": "FrMjTDi7KoWYGdzQANUEW",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -429.28598135666755,
			"y": 166.43517890126623,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 70.81644178885557,
			"height": 108.30428902193904,
			"seed": 1914482148,
			"groupIds": [
				"ejY17v6zTtIpVdt_diBNa",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "LsGTDUQYx9QHNTg7GICxo",
					"type": "arrow"
				},
				{
					"id": "Ue8j7jSbzHi5WGmdq2uwg",
					"type": "arrow"
				}
			],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1773,
			"versionNonce": 2114708066,
			"isDeleted": false,
			"id": "lzTxAZRZeg_gvXlbOcRxg",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -421.17827726657595,
			"y": 174.69236025166316,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 55.801163535143246,
			"height": 82.83278895375764,
			"seed": 1972719972,
			"groupIds": [
				"ejY17v6zTtIpVdt_diBNa",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 1817,
			"versionNonce": 585329854,
			"isDeleted": false,
			"id": "e1ggtemzjEY20QQBg1xpb",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -398.9916075022238,
			"y": 261.0700433742479,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 11.427824006438863,
			"height": 11.427824006438863,
			"seed": 1496155364,
			"groupIds": [
				"ejY17v6zTtIpVdt_diBNa",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1464,
			"versionNonce": 15025698,
			"isDeleted": false,
			"id": "o14f7HH103E6zKs7ZCK8e",
			"fillStyle": "cross-hatch",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -412.89858686660546,
			"y": 185.23651692780334,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 39.2417827352022,
			"height": 19.889460471185775,
			"seed": 309545060,
			"groupIds": [
				"ejY17v6zTtIpVdt_diBNa",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "rectangle",
			"version": 1506,
			"versionNonce": 1603478782,
			"isDeleted": false,
			"id": "AFR6fsiuaxIPTaXJkPF6e",
			"fillStyle": "cross-hatch",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -412.89858686660546,
			"y": 220.79427697275776,
			"strokeColor": "#000000",
			"backgroundColor": "#fab005",
			"width": 39.2417827352022,
			"height": 19.889460471185775,
			"seed": 892640228,
			"groupIds": [
				"ejY17v6zTtIpVdt_diBNa",
				"QGy4qyFNc2-THg8BbY4Mz",
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 541,
			"versionNonce": 1918644706,
			"isDeleted": false,
			"id": "Q1SmFqUk",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -451.15727257313563,
			"y": 134.3237077114048,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 99.79193115234375,
			"height": 20,
			"seed": 1490459740,
			"groupIds": [
				"FFHOxzArBrEiD1kf81FF-"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "zwAPnbutGd4pO7-i_Tg8M",
					"type": "arrow"
				},
				{
					"id": "Lrq7MqRyGmQCRegKJe_fT",
					"type": "arrow"
				}
			],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "worker nodes",
			"rawText": "worker nodes",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "worker nodes",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 1709,
			"versionNonce": 371316030,
			"isDeleted": false,
			"id": "jqLXCviZg32Qhs1DhiB1B",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -176.7996078837303,
			"y": 396.7743175552694,
			"strokeColor": "#000000",
			"backgroundColor": "#eeeeee",
			"width": 96.04882870779743,
			"height": 94.20173584803199,
			"seed": 123432525,
			"groupIds": [
				"U3w_Q8jcxhz62uPfg0z1l",
				"JzVqddAaQ0OvUQ47ebXy0"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1129,
			"versionNonce": 897557922,
			"isDeleted": false,
			"id": "zwLP5bOU",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -162.44084294389415,
			"y": 423.7914526132143,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 67.331298828125,
			"height": 40.167465732141956,
			"seed": 1808932013,
			"groupIds": [
				"U3w_Q8jcxhz62uPfg0z1l",
				"JzVqddAaQ0OvUQ47ebXy0"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"fontSize": 14.876839160052583,
			"fontFamily": 1,
			"text": "Job\nScheduler",
			"rawText": "Job\nScheduler",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Job\nScheduler",
			"lineHeight": 1.3499999999999994,
			"baseline": 34
		},
		{
			"type": "rectangle",
			"version": 1887,
			"versionNonce": 535854462,
			"isDeleted": false,
			"id": "pFA6fqXfridtVAk1-5h8N",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -185.0437241287188,
			"y": 387.12802925785667,
			"strokeColor": "#000000",
			"backgroundColor": "#eeeeee",
			"width": 96.04882870779743,
			"height": 94.20173584803199,
			"seed": 1042546445,
			"groupIds": [
				"p3RCYceN8Hs9zKfG8PJa_",
				"JzVqddAaQ0OvUQ47ebXy0"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "uSX6cLUctsQBVIp7CGl7e",
					"type": "arrow"
				},
				{
					"id": "nXLaU2dWnzilLu2Dd3GvT",
					"type": "arrow"
				},
				{
					"id": "Ue8j7jSbzHi5WGmdq2uwg",
					"type": "arrow"
				}
			],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1349,
			"versionNonce": 1937678690,
			"isDeleted": false,
			"id": "22t2GlxM",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -166.14218117374594,
			"y": 414.0049027779234,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 58.24574279785156,
			"height": 40.167465732141956,
			"seed": 80385389,
			"groupIds": [
				"p3RCYceN8Hs9zKfG8PJa_",
				"JzVqddAaQ0OvUQ47ebXy0"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"fontSize": 14.876839160052583,
			"fontFamily": 1,
			"text": "Enqueue\nService",
			"rawText": "Enqueue\nService",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Enqueue\nService",
			"lineHeight": 1.3499999999999994,
			"baseline": 34
		},
		{
			"type": "rectangle",
			"version": 1778,
			"versionNonce": 37756350,
			"isDeleted": false,
			"id": "Qu_VMS2JGfB4EyI63jG9t",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -410.2462209402901,
			"y": 386.72262892730635,
			"strokeColor": "#000000",
			"backgroundColor": "#eeeeee",
			"width": 97.35601825028085,
			"height": 98.60970239702232,
			"seed": 1805832803,
			"groupIds": [
				"gyUyPWtc1v7F0J-KFQ5a5"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "nexOo5DKK0bpzkY6JQGem",
					"type": "arrow"
				},
				{
					"type": "text",
					"id": "o1lisKqr"
				},
				{
					"id": "nXLaU2dWnzilLu2Dd3GvT",
					"type": "arrow"
				}
			],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 338,
			"versionNonce": 1470637346,
			"isDeleted": false,
			"id": "o1lisKqr",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -395.72819258907543,
			"y": 416.02748012581753,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 68.31996154785156,
			"height": 40,
			"seed": 781477741,
			"groupIds": [
				"gyUyPWtc1v7F0J-KFQ5a5"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Load\nBalancer",
			"rawText": "Load\nBalancer",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Qu_VMS2JGfB4EyI63jG9t",
			"originalText": "Load\nBalancer",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 717,
			"versionNonce": 1915860478,
			"isDeleted": false,
			"id": "nXLaU2dWnzilLu2Dd3GvT",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -297.1722657572289,
			"y": 435.02728338490454,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 99.72395338179592,
			"height": 0.4175338823307584,
			"seed": 1688596301,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "Qu_VMS2JGfB4EyI63jG9t",
				"gap": 15.717936932780333,
				"focus": -0.014756560934398838
			},
			"endBinding": {
				"elementId": "pFA6fqXfridtVAk1-5h8N",
				"gap": 12.40458824671419,
				"focus": -0.002702686853540695
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
					99.72395338179592,
					-0.4175338823307584
				]
			]
		},
		{
			"type": "rectangle",
			"version": 1854,
			"versionNonce": 1265316066,
			"isDeleted": false,
			"id": "1aMVHuULPTuU7i8fNzWU0",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 158.15254879440704,
			"y": 167.22616437044462,
			"strokeColor": "#000000",
			"backgroundColor": "#eeeeee",
			"width": 96.04882870779743,
			"height": 94.20173584803199,
			"seed": 550166509,
			"groupIds": [
				"K3ZfS_iAg1ipeqFF5iixx",
				"caGxLkr45wMRa23HfVZui"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1300,
			"versionNonce": 1489389118,
			"isDeleted": false,
			"id": "3uSqLfz3",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 172.65609151299128,
			"y": 194.10303789051136,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 67.331298828125,
			"height": 40.167465732141956,
			"seed": 899832397,
			"groupIds": [
				"K3ZfS_iAg1ipeqFF5iixx",
				"caGxLkr45wMRa23HfVZui"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"fontSize": 14.876839160052583,
			"fontFamily": 1,
			"text": "Task\nScheduler",
			"rawText": "Task\nScheduler",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Task\nScheduler",
			"lineHeight": 1.3499999999999994,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 1463,
			"versionNonce": 844547234,
			"isDeleted": false,
			"id": "uSX6cLUctsQBVIp7CGl7e",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -69.49036949958945,
			"y": 438.9632263443224,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 146.79718359430774,
			"height": 2.174448399686355,
			"seed": 260248099,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "pFA6fqXfridtVAk1-5h8N",
				"gap": 19.504525921331897,
				"focus": 0.12001655453869282
			},
			"endBinding": {
				"elementId": "_dmH0UrFLIgqml67ToQEq",
				"gap": 9.869760538521703,
				"focus": -0.017237819037477474
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
					146.79718359430774,
					-2.174448399686355
				]
			]
		},
		{
			"type": "line",
			"version": 6616,
			"versionNonce": 1457442430,
			"isDeleted": false,
			"id": "UgdHnQpTeWJB31I3i4W6l",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 370.68200120182144,
			"y": 615.8547097106242,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 75.01121630306868,
			"height": 96.81388324216653,
			"seed": 449195981,
			"groupIds": [
				"2tA1L7LVtq-ZiKiVxU8lV",
				"HUCdDQAfG8nTWCMD4rHF0",
				"rws6sgyVIuubPxJpVerRV"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.24734846976242794,
					73.1714082159101
				],
				[
					0.011575327725072006,
					81.50165529728328
				],
				[
					3.8632435379119165,
					85.10105205208878
				],
				[
					17.276485894102954,
					88.14730719194147
				],
				[
					39.948665011120255,
					89.0958655364321
				],
				[
					61.61043288740646,
					87.58135319133916
				],
				[
					73.11948965218787,
					83.95942431004657
				],
				[
					74.74268637210398,
					80.90610026776591
				],
				[
					74.9706584753909,
					74.19947908967055
				],
				[
					74.79172688269483,
					6.138672737165569
				],
				[
					74.38835763792527,
					-0.2918194398554754
				],
				[
					69.57188081608908,
					-3.885863818744892
				],
				[
					59.42940850758881,
					-5.967344146345569
				],
				[
					36.31608449133351,
					-7.7180177057344235
				],
				[
					17.785060590062127,
					-6.674087120295436
				],
				[
					3.210536142559118,
					-3.1332019499277424
				],
				[
					-0.04055782767777212,
					-0.04396604849106378
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "ellipse",
			"version": 7337,
			"versionNonce": 639230050,
			"isDeleted": false,
			"id": "sNSrymkcDCr2-w5ynsdOQ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 370.9479337925054,
			"y": 607.1017415545962,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 74.53008207714048,
			"height": 15.073148387271289,
			"seed": 392736301,
			"groupIds": [
				"2tA1L7LVtq-ZiKiVxU8lV",
				"HUCdDQAfG8nTWCMD4rHF0",
				"rws6sgyVIuubPxJpVerRV"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "P0fCsojpiU_RA6FcIWuAG",
					"type": "arrow"
				}
			],
			"updated": 1710738077493,
			"link": null,
			"locked": false
		},
		{
			"type": "line",
			"version": 6785,
			"versionNonce": 1228689086,
			"isDeleted": false,
			"id": "S7DGdy-AsbmekzWR2OxuE",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 580.1214457131094,
			"y": 618.184122233664,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 75.01121630306868,
			"height": 96.81388324216653,
			"seed": 464203748,
			"groupIds": [
				"cE1nuwlOWcQr0oUDitrh9",
				"BL5vQ-qJvC3RmL-1XirEv",
				"bBJvlVEqifhOAw7LtyWiW"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077493,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.24734846976242794,
					73.1714082159101
				],
				[
					0.011575327725072006,
					81.50165529728328
				],
				[
					3.8632435379119165,
					85.10105205208878
				],
				[
					17.276485894102954,
					88.14730719194147
				],
				[
					39.948665011120255,
					89.0958655364321
				],
				[
					61.61043288740646,
					87.58135319133916
				],
				[
					73.11948965218787,
					83.95942431004657
				],
				[
					74.74268637210398,
					80.90610026776591
				],
				[
					74.9706584753909,
					74.19947908967055
				],
				[
					74.79172688269483,
					6.138672737165569
				],
				[
					74.38835763792527,
					-0.2918194398554754
				],
				[
					69.57188081608908,
					-3.885863818744892
				],
				[
					59.42940850758881,
					-5.967344146345569
				],
				[
					36.31608449133351,
					-7.7180177057344235
				],
				[
					17.785060590062127,
					-6.674087120295436
				],
				[
					3.210536142559118,
					-3.1332019499277424
				],
				[
					-0.04055782767777212,
					-0.04396604849106378
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "ellipse",
			"version": 7505,
			"versionNonce": 847479842,
			"isDeleted": false,
			"id": "eROdoEs-Up5OzQ99tWBtA",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 580.3873783037934,
			"y": 609.4311540776359,
			"strokeColor": "#000000",
			"backgroundColor": "#fff",
			"width": 74.53008207714048,
			"height": 15.073148387271289,
			"seed": 771986276,
			"groupIds": [
				"cE1nuwlOWcQr0oUDitrh9",
				"BL5vQ-qJvC3RmL-1XirEv",
				"bBJvlVEqifhOAw7LtyWiW"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "P0fCsojpiU_RA6FcIWuAG",
					"type": "arrow"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 275,
			"versionNonce": 1283442430,
			"isDeleted": false,
			"id": "KcAYUJp0",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 576.1663529299503,
			"y": 716.9160169483313,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 94.51191711425781,
			"height": 20,
			"seed": 629961261,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "jobs shard 1",
			"rawText": "jobs shard 1",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "jobs shard 1",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 393,
			"versionNonce": 293777378,
			"isDeleted": false,
			"id": "JeKpWfgo",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 463.0084539738607,
			"y": 532.2366049361298,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 101.18391418457031,
			"height": 20,
			"seed": 390285645,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "jobs shard 0",
			"rawText": "jobs shard 0",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "jobs shard 0",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "text",
			"version": 465,
			"versionNonce": 1093285694,
			"isDeleted": false,
			"id": "mswUPzxZ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 344.7437188773837,
			"y": 717.3049943226953,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 101.56791687011719,
			"height": 20,
			"seed": 459078413,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "jobs shard 2",
			"rawText": "jobs shard 2",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "jobs shard 2",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "rectangle",
			"version": 158,
			"versionNonce": 1730569122,
			"isDeleted": false,
			"id": "_dmH0UrFLIgqml67ToQEq",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 87.17657463323997,
			"y": 385.90490565420214,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 129.18823140656912,
			"height": 97.84216484670365,
			"seed": 1049280781,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"type": "text",
					"id": "6vzYPLym"
				},
				{
					"id": "uSX6cLUctsQBVIp7CGl7e",
					"type": "arrow"
				},
				{
					"id": "Ccl5t2mU9wO8JAyRV4Zii",
					"type": "arrow"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 109,
			"versionNonce": 1335664510,
			"isDeleted": false,
			"id": "6vzYPLym",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 100.14672793418077,
			"y": 424.825988077554,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 103.2479248046875,
			"height": 20,
			"seed": 493695597,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "Orchestrator",
			"rawText": "Orchestrator",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "_dmH0UrFLIgqml67ToQEq",
			"originalText": "Orchestrator",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "arrow",
			"version": 1170,
			"versionNonce": 2107481954,
			"isDeleted": false,
			"id": "Ccl5t2mU9wO8JAyRV4Zii",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 225.9989325588042,
			"y": 439.4368109958365,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 184.15230869548566,
			"height": 72.26344572360313,
			"seed": 1065538509,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"type": "text",
					"id": "PTJ7YYy2"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "_dmH0UrFLIgqml67ToQEq",
				"focus": -0.6010665315278291,
				"gap": 9.634126518995117
			},
			"endBinding": {
				"elementId": "7j5FQDPTS3baFkwDabAEd",
				"focus": 0.727283125667035,
				"gap": 19.184136068560335
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
					74.74140359458613,
					71.8127229336182
				],
				[
					184.15230869548566,
					72.26344572360313
				]
			]
		},
		{
			"id": "PTJ7YYy2",
			"type": "text",
			"x": 255.05165694216413,
			"y": 435.93141394687746,
			"width": 64.89595031738281,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1470255678,
			"version": 17,
			"versionNonce": 1813512126,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"text": "write\nnew jobs",
			"rawText": "write\nnew jobs",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "Ccl5t2mU9wO8JAyRV4Zii",
			"originalText": "write\nnew jobs",
			"lineHeight": 1.25
		},
		{
			"type": "text",
			"version": 174,
			"versionNonce": 20407074,
			"isDeleted": false,
			"id": "zqXpuWPK",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 64.60804796705054,
			"y": 493.2777537153155,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 156.5598907470703,
			"height": 60,
			"seed": 1486800259,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "shard health,\nredirecting requests\nto shards",
			"rawText": "shard health,\nredirecting requests\nto shards",
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "shard health,\nredirecting requests\nto shards",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "rectangle",
			"version": 1902,
			"versionNonce": 1522358270,
			"isDeleted": false,
			"id": "vMrJ3O9Mkm8Fh1XzHnTO8",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 168.78039699357055,
			"y": 177.49094738550218,
			"strokeColor": "#000000",
			"backgroundColor": "#eeeeee",
			"width": 96.04882870779743,
			"height": 94.20173584803199,
			"seed": 568136548,
			"groupIds": [
				"BbmaqmNei6SpjcAUiu61W",
				"VXk5YStHJQK07WZjrJNig"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "q1WtUcMNzcj6u3qQIyc8u",
					"type": "arrow"
				},
				{
					"id": "nXLaU2dWnzilLu2Dd3GvT",
					"type": "arrow"
				},
				{
					"id": "P0fCsojpiU_RA6FcIWuAG",
					"type": "arrow"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 1344,
			"versionNonce": 1013100258,
			"isDeleted": false,
			"id": "7oWb8udb",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 183.2839397121548,
			"y": 204.36782090556892,
			"strokeColor": "#000000",
			"backgroundColor": "#ced4da",
			"width": 67.331298828125,
			"height": 40.167465732141956,
			"seed": 1798112996,
			"groupIds": [
				"BbmaqmNei6SpjcAUiu61W",
				"VXk5YStHJQK07WZjrJNig"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 14.876839160052583,
			"fontFamily": 1,
			"text": "Task\nScheduler",
			"rawText": "Task\nScheduler",
			"textAlign": "center",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "Task\nScheduler",
			"lineHeight": 1.3499999999999994,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 1693,
			"versionNonce": 864921662,
			"isDeleted": false,
			"id": "P0fCsojpiU_RA6FcIWuAG",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 247.41114096563757,
			"y": 286.30457219430735,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 129.47528341696108,
			"height": 312.0514759093863,
			"seed": 1199088740,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "845AoZgZ"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "vMrJ3O9Mkm8Fh1XzHnTO8",
				"focus": -0.020867414034278872,
				"gap": 14.611888960773172
			},
			"endBinding": {
				"elementId": "sNSrymkcDCr2-w5ynsdOQ",
				"focus": -0.6660569107679283,
				"gap": 13.225088703820095
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
					38.412755962279164,
					81.35039019748751
				],
				[
					129.47528341696108,
					312.0514759093863
				]
			]
		},
		{
			"type": "text",
			"version": 40,
			"versionNonce": 1403945634,
			"isDeleted": false,
			"id": "845AoZgZ",
			"fillStyle": "solid",
			"strokeWidth": 2,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 306.97207526693836,
			"y": 404.46080414519906,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "transparent",
			"width": 72.62393188476562,
			"height": 60,
			"seed": 1362523492,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "grab jobs\nfor time\nslot",
			"rawText": "grab jobs\nfor time\nslot",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "P0fCsojpiU_RA6FcIWuAG",
			"originalText": "grab jobs\nfor time\nslot",
			"lineHeight": 1.25,
			"baseline": 54
		},
		{
			"type": "line",
			"version": 4974,
			"versionNonce": 1718218878,
			"isDeleted": false,
			"id": "fNl1nH5STdfmguj9MaKj3",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 1.5707963267948957,
			"x": -116.9157306539816,
			"y": 156.68653715212022,
			"strokeColor": "#087f5b",
			"backgroundColor": "#40c057",
			"width": 52.317507746132115,
			"height": 154.56722543646003,
			"seed": 345487565,
			"groupIds": [
				"Ka_ZC03AKgTu5OZNeEAwL"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.1725162731731403,
					116.82107121890462
				],
				[
					0.008073356596080744,
					130.12064288619618
				],
				[
					2.694467356765587,
					135.86722334556717
				],
				[
					12.049700419984944,
					140.7306911579349
				],
				[
					27.86269432990675,
					142.2451023824676
				],
				[
					42.97096432627199,
					139.82712302629713
				],
				[
					50.998099415101294,
					134.0445691284302
				],
				[
					52.13021819883883,
					129.16981553143583
				],
				[
					52.28922018370778,
					118.46242736729553
				],
				[
					52.16442211418855,
					9.800635828982735
				],
				[
					51.88308720685254,
					-0.46590137319512337
				],
				[
					48.52377541516831,
					-6.203936550968926
				],
				[
					41.449781688403746,
					-9.527102901326515
				],
				[
					25.329105770103325,
					-12.322123053992442
				],
				[
					12.404412180527922,
					-10.655446243436785
				],
				[
					2.239228448568725,
					-5.00228186200372
				],
				[
					-0.028287562424331975,
					-0.07019354973772352
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "line",
			"version": 2613,
			"versionNonce": 30006882,
			"isDeleted": false,
			"id": "_biUErLr1mF_X1fTDuHxx",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 1.5707963267948957,
			"x": -141.44314105833854,
			"y": 215.79149370968543,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 50.7174766392476,
			"height": 12.698053371678215,
			"seed": 1344345901,
			"groupIds": [
				"Ka_ZC03AKgTu5OZNeEAwL"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					1.3361877396713384,
					5.061656285093649
				],
				[
					7.098613049589299,
					9.308339392337079
				],
				[
					14.766422451441104,
					11.880105003906111
				],
				[
					26.779003528407447,
					12.114458425450186
				],
				[
					40.79727342221974,
					10.477131310135727
				],
				[
					48.98410145879092,
					4.5205722256349645
				],
				[
					50.7174766392476,
					-0.5835949462280285
				]
			]
		},
		{
			"type": "line",
			"version": 2746,
			"versionNonce": 1058222270,
			"isDeleted": false,
			"id": "fiKCFThfBMNq-ZCZgvAns",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 1.5707963267948957,
			"x": -96.01735990989664,
			"y": 216.13057883468554,
			"strokeColor": "#087f5b",
			"backgroundColor": "transparent",
			"width": 50.57247907260371,
			"height": 10.178760037658167,
			"seed": 1672456589,
			"groupIds": [
				"Ka_ZC03AKgTu5OZNeEAwL"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					1.332367676378171,
					4.05742385947015
				],
				[
					7.078318632616268,
					7.4615651903783
				],
				[
					14.724206326638113,
					9.523092596748189
				],
				[
					26.70244431044034,
					9.710950307853885
				],
				[
					40.68063699304561,
					8.398468833558885
				],
				[
					48.84405948536458,
					3.623690858023169
				],
				[
					50.57247907260371,
					-0.4678097298042818
				]
			]
		},
		{
			"type": "ellipse",
			"version": 5711,
			"versionNonce": 1401143842,
			"isDeleted": false,
			"id": "RYl93uNlDS12Y1kxYYOWQ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 1.5707963267948957,
			"x": -49.4125867777816,
			"y": 210.27738291379734,
			"strokeColor": "#087f5b",
			"backgroundColor": "#fff",
			"width": 51.27812853552538,
			"height": 22.797152568995934,
			"seed": 8187885,
			"groupIds": [
				"Ka_ZC03AKgTu5OZNeEAwL"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "arrow",
			"version": 123,
			"versionNonce": 1764387070,
			"isDeleted": false,
			"id": "EfnX17NGq9xdteZsXYegG",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 152.0957623002762,
			"y": 220.8090183041624,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 155.6797584070481,
			"height": 3.1120780406317863,
			"seed": 1875494851,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"type": "text",
					"id": "915ZA3ze"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": "arrow",
			"points": [
				[
					0,
					0
				],
				[
					-155.6797584070481,
					3.1120780406317863
				]
			]
		},
		{
			"type": "text",
			"version": 27,
			"versionNonce": 1674259938,
			"isDeleted": false,
			"id": "915ZA3ze",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 39.09589469343183,
			"y": 202.3650573244783,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 70.31997680664062,
			"height": 40,
			"seed": 995938573,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "post job\nto queue",
			"rawText": "post job\nto queue",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "EfnX17NGq9xdteZsXYegG",
			"originalText": "post job\nto queue",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"type": "arrow",
			"version": 140,
			"versionNonce": 1949342014,
			"isDeleted": false,
			"id": "LsGTDUQYx9QHNTg7GICxo",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -172.99741081608624,
			"y": 222.39954388035875,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 170.5854308288637,
			"height": 0.12241062163190009,
			"seed": 749643853,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"type": "text",
					"id": "VtF7QMcY"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": {
				"elementId": "FrMjTDi7KoWYGdzQANUEW",
				"focus": 0.03637525454352354,
				"gap": 14.886697922861998
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
					-170.5854308288637,
					0.12241062163190009
				]
			]
		},
		{
			"type": "text",
			"version": 12,
			"versionNonce": 397353378,
			"isDeleted": false,
			"id": "VtF7QMcY",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -271.49511640962567,
			"y": 212.39954388035875,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 72.62393188476562,
			"height": 20,
			"seed": 1578856269,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "grab jobs",
			"rawText": "grab jobs",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "LsGTDUQYx9QHNTg7GICxo",
			"originalText": "grab jobs",
			"lineHeight": 1.25,
			"baseline": 14
		},
		{
			"type": "arrow",
			"version": 120,
			"versionNonce": 1468449150,
			"isDeleted": false,
			"id": "Ue8j7jSbzHi5WGmdq2uwg",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -348.197342161905,
			"y": 277.9718592760052,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 159.16042954104194,
			"height": 103.05649409885234,
			"seed": 1160681123,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"type": "text",
					"id": "lxklzhpd"
				}
			],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "FrMjTDi7KoWYGdzQANUEW",
				"focus": 0.3607523986067837,
				"gap": 10.272197405906951
			},
			"endBinding": {
				"elementId": "pFA6fqXfridtVAk1-5h8N",
				"focus": 0.24961546028910025,
				"gap": 6.099675882999094
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
					159.16042954104194,
					103.05649409885234
				]
			]
		},
		{
			"type": "text",
			"version": 58,
			"versionNonce": 1516150114,
			"isDeleted": false,
			"id": "lxklzhpd",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -311.00909516482153,
			"y": 309.5001063254314,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"width": 84.783935546875,
			"height": 40,
			"seed": 1113301933,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "update job\nstatus?",
			"rawText": "update job\nstatus?",
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Ue8j7jSbzHi5WGmdq2uwg",
			"originalText": "update job\nstatus?",
			"lineHeight": 1.25,
			"baseline": 34
		},
		{
			"id": "qLXZtNfG",
			"type": "text",
			"x": -184.96347376506878,
			"y": 257.81321860627355,
			"width": 196.79986572265625,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 605345534,
			"version": 70,
			"versionNonce": 1986912702,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"text": "in-memory message broker",
			"rawText": "in-memory message broker",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 14,
			"containerId": null,
			"originalText": "in-memory message broker",
			"lineHeight": 1.25
		},
		{
			"type": "line",
			"version": 3993,
			"versionNonce": 1495834914,
			"isDeleted": false,
			"id": "ZiWBNiqMHNQlSvIeUsjSI",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -293.7502159788928,
			"y": 577.7919690296753,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#228be6",
			"width": 88.21658171083376,
			"height": 113.8575037534261,
			"seed": 463396706,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.29089298333313673,
					86.05288422061678
				],
				[
					0.013613108737802165,
					95.84963140781468
				],
				[
					4.543349062013738,
					100.08268472409586
				],
				[
					20.317928500125443,
					103.66521849306073
				],
				[
					46.98143617553956,
					104.78076599153316
				],
				[
					72.45665455006592,
					102.9996310009587
				],
				[
					85.99182564238487,
					98.74007888522631
				],
				[
					87.90077837148979,
					95.14923176741362
				],
				[
					88.16888387182134,
					87.26194204835767
				],
				[
					87.95845222911922,
					7.219356674957439
				],
				[
					87.48407176050935,
					-0.3431928547433216
				],
				[
					81.81967725989045,
					-4.569951534960701
				],
				[
					69.89167127292335,
					-7.017866506201685
				],
				[
					42.70935725136615,
					-9.076737761892943
				],
				[
					20.91603533578692,
					-7.849028196182914
				],
				[
					3.775735655469765,
					-3.684787148572539
				],
				[
					-0.047697839012426885,
					-0.0517060607782156
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "line",
			"version": 1727,
			"versionNonce": 604436990,
			"isDeleted": false,
			"id": "RzuVhKElZbxRGeLdtTs5-",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -293.06285438939545,
			"y": 643.082097060463,
			"strokeColor": "#0a11d3",
			"backgroundColor": "transparent",
			"width": 88.30808627974527,
			"height": 9.797916664247975,
			"seed": 1292935970,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					2.326538897826852,
					3.9056133261361587
				],
				[
					12.359939318521995,
					7.182387014695761
				],
				[
					25.710950037209347,
					9.166781347006062
				],
				[
					46.6269757640547,
					9.347610268342288
				],
				[
					71.03526003420632,
					8.084235941711592
				],
				[
					85.2899738827162,
					3.4881086608341767
				],
				[
					88.30808627974527,
					-0.45030639590568633
				]
			]
		},
		{
			"type": "line",
			"version": 1814,
			"versionNonce": 1065102562,
			"isDeleted": false,
			"id": "7vB4irofuWiFB0Pvhj4kG",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -294.1565959014569,
			"y": 610.0079424983912,
			"strokeColor": "#0a11d3",
			"backgroundColor": "transparent",
			"width": 88.30808627974527,
			"height": 9.797916664247975,
			"seed": 991162082,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					2.326538897826852,
					3.9056133261361587
				],
				[
					12.359939318521995,
					7.182387014695761
				],
				[
					25.710950037209347,
					9.166781347006062
				],
				[
					46.6269757640547,
					9.347610268342288
				],
				[
					71.03526003420632,
					8.084235941711592
				],
				[
					85.2899738827162,
					3.4881086608341767
				],
				[
					88.30808627974527,
					-0.45030639590568633
				]
			]
		},
		{
			"type": "ellipse",
			"version": 4833,
			"versionNonce": 659753534,
			"isDeleted": false,
			"id": "8_Pwq8eNgKr7oR40QRBFL",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -295.2774185876186,
			"y": 569.7672728025786,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 87.65074610854188,
			"height": 17.72670397681366,
			"seed": 1782039202,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 201,
			"versionNonce": 1927823522,
			"isDeleted": false,
			"id": "0uxAQ-9kEQb7SHy1lg3qz",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -223.76768628703803,
			"y": 594.3430756797122,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 12.846057046979809,
			"height": 13.941904362416096,
			"seed": 1965760098,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 250,
			"versionNonce": 1060311678,
			"isDeleted": false,
			"id": "HUcXYinutIfKraFslBD_7",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -223.76768628703803,
			"y": 624.9455295387727,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 12.846057046979809,
			"height": 13.941904362416096,
			"seed": 1220346402,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 304,
			"versionNonce": 1327225954,
			"isDeleted": false,
			"id": "mj83GVIZSevguIllZukRZ",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -223.76768628703803,
			"y": 658.2063307132694,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 12.846057046979809,
			"height": 13.941904362416096,
			"seed": 1608281570,
			"groupIds": [
				"LQ0KOHhEHtf9vGid2825l"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false
		},
		{
			"id": "NmxZ6ocz",
			"type": "text",
			"x": -318.74996217369653,
			"y": 689.6544900481892,
			"width": 143.2799072265625,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1030141218,
			"version": 96,
			"versionNonce": 644354750,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"text": "input object store",
			"rawText": "input object store",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 14,
			"containerId": null,
			"originalText": "input object store",
			"lineHeight": 1.25
		},
		{
			"id": "I03EtaCnZkkSpr4PSdjUP",
			"type": "arrow",
			"x": -172.63973268150903,
			"y": 498.9934527689773,
			"width": 58.25104967003077,
			"height": 62.61869386327811,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 121962402,
			"version": 104,
			"versionNonce": 1642463266,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077494,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-58.25104967003077,
					62.61869386327811
				]
			],
			"lastCommittedPoint": [
				-57.61134935461956,
				62.19928243885869
			],
			"startBinding": null,
			"endBinding": {
				"focus": 0.11324486010896852,
				"gap": 9.624374584297259,
				"elementId": "8_Pwq8eNgKr7oR40QRBFL"
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"type": "line",
			"version": 1875,
			"versionNonce": 657828834,
			"isDeleted": false,
			"id": "yAXmrgC1BZjHGUUAFJvIC",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -95.06686773999591,
			"y": -50.85892657935398,
			"strokeColor": "#881fa3",
			"backgroundColor": "#be4bdb",
			"width": 116.42036295658872,
			"height": 103.65107323746608,
			"seed": 944539582,
			"groupIds": [
				"rAD2wJKwYpNDEY78VLHHo"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					-62.44191743896485,
					19.19929080548739
				],
				[
					-63.17668831316513,
					79.43840749607878
				],
				[
					-7.618334228588694,
					103.65107323746608
				],
				[
					51.963117173367294,
					79.15871076413049
				],
				[
					53.24367464342358,
					21.28567723840068
				],
				[
					0,
					0
				]
			]
		},
		{
			"id": "Es6hPJ6F",
			"type": "text",
			"x": -141.91064943714105,
			"y": -17.277730976574105,
			"width": 89.8719482421875,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [
				"rAD2wJKwYpNDEY78VLHHo"
			],
			"frameId": null,
			"roundness": null,
			"seed": 1421018402,
			"version": 157,
			"versionNonce": 1362426686,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"text": "distributed\nlock service",
			"rawText": "distributed\nlock service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 34,
			"containerId": null,
			"originalText": "distributed\nlock service",
			"lineHeight": 1.25
		},
		{
			"id": "zwAPnbutGd4pO7-i_Tg8M",
			"type": "arrow",
			"x": -340.15189963876037,
			"y": 127.15271575851995,
			"width": 177.24699721638024,
			"height": 97.93620182891993,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1361030846,
			"version": 157,
			"versionNonce": 1159323554,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "fxFCoaaG"
				}
			],
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					177.24699721638024,
					-97.93620182891993
				]
			],
			"lastCommittedPoint": [
				177.24699721638024,
				-97.93620182891993
			],
			"startBinding": {
				"elementId": "Q1SmFqUk",
				"focus": 0.4416993768734469,
				"gap": 11.21344178203151
			},
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "fxFCoaaG",
			"type": "text",
			"x": -302.1763655081093,
			"y": 58.18461484405998,
			"width": 101.29592895507812,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1303717310,
			"version": 30,
			"versionNonce": 430891902,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"text": "request\nlock on jobId",
			"rawText": "request\nlock on jobId",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "zwAPnbutGd4pO7-i_Tg8M",
			"originalText": "request\nlock on jobId",
			"lineHeight": 1.25
		},
		{
			"id": "Lrq7MqRyGmQCRegKJe_fT",
			"type": "arrow",
			"x": -163.37424530555552,
			"y": 0.6849324391296818,
			"width": 214.9946409278058,
			"height": 124.80015504862808,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 814781730,
			"version": 214,
			"versionNonce": 1203870562,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WeKA25v5"
				}
			],
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-119.30036064581407,
					36.26223137626107
				],
				[
					-214.9946409278058,
					124.80015504862808
				]
			],
			"lastCommittedPoint": [
				-214.9946409278058,
				124.80015504862808
			],
			"startBinding": null,
			"endBinding": {
				"elementId": "Q1SmFqUk",
				"focus": 0.041695759904239724,
				"gap": 8.838620223647041
			},
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "WeKA25v5",
			"type": "text",
			"x": -322.5945812321313,
			"y": 26.947163815390752,
			"width": 79.83995056152344,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1263819774,
			"version": 21,
			"versionNonce": 1128383422,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"text": "heartbeat",
			"rawText": "heartbeat",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "Lrq7MqRyGmQCRegKJe_fT",
			"originalText": "heartbeat",
			"lineHeight": 1.25
		},
		{
			"id": "QIRn78nW1qYk5-xV1aOOo",
			"type": "arrow",
			"x": 351.1384993927528,
			"y": 619.0036973438582,
			"width": 545.2089034310787,
			"height": 9.641180229335987,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 4348286,
			"version": 134,
			"versionNonce": 892751038,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "aLiokkeq"
				}
			],
			"updated": 1710738142365,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-545.2089034310787,
					9.641180229335987
				]
			],
			"lastCommittedPoint": [
				-545.3635132783138,
				4.947593873540427
			],
			"startBinding": null,
			"endBinding": null,
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "aLiokkeq",
			"type": "text",
			"x": 31.182080819303266,
			"y": 603.8242874585262,
			"width": 94.70393371582031,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 122254306,
			"version": 54,
			"versionNonce": 1237355646,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738141191,
			"link": null,
			"locked": false,
			"text": "database\nlinks to this",
			"rawText": "database\nlinks to this",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "QIRn78nW1qYk5-xV1aOOo",
			"originalText": "database\nlinks to this",
			"lineHeight": 1.25
		},
		{
			"id": "GhuZxlqNaE6EyOiWBnEJb",
			"type": "arrow",
			"x": -301.26126147849413,
			"y": 642.9023786157184,
			"width": 450.2104856046759,
			"height": 437.64817954026574,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 959772862,
			"version": 413,
			"versionNonce": 482522238,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "CTb4yOfh"
				}
			],
			"updated": 1710738095340,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-450.2104856046759,
					-198.8707162734998
				],
				[
					-155.52391986976124,
					-437.64817954026574
				]
			],
			"lastCommittedPoint": [
				-155.23679292218355,
				-336.50380369071496
			],
			"startBinding": null,
			"endBinding": {
				"elementId": "9qNpybOUKHPQcIZZBTTFx",
				"focus": 0.8415919654897716,
				"gap": 12.104590519301752
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "CTb4yOfh",
			"type": "text",
			"x": -825.9196917242833,
			"y": 424.03166234221857,
			"width": 148.89588928222656,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 385875298,
			"version": 39,
			"versionNonce": 1153506146,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738092956,
			"link": null,
			"locked": false,
			"text": "read in data\nwhen processing job",
			"rawText": "read in data\nwhen processing job",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "GhuZxlqNaE6EyOiWBnEJb",
			"originalText": "read in data\nwhen processing job",
			"lineHeight": 1.25
		},
		{
			"type": "line",
			"version": 4168,
			"versionNonce": 1263641726,
			"isDeleted": false,
			"id": "vKAOnUoan601aLdfMZHSd",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -547.5526374208665,
			"y": 642.0943068853287,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#228be6",
			"width": 88.21658171083376,
			"height": 113.8575037534261,
			"seed": 68746814,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738080979,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					0.29089298333313673,
					86.05288422061678
				],
				[
					0.013613108737802165,
					95.84963140781468
				],
				[
					4.543349062013738,
					100.08268472409586
				],
				[
					20.317928500125443,
					103.66521849306073
				],
				[
					46.98143617553956,
					104.78076599153316
				],
				[
					72.45665455006592,
					102.9996310009587
				],
				[
					85.99182564238487,
					98.74007888522631
				],
				[
					87.90077837148979,
					95.14923176741362
				],
				[
					88.16888387182134,
					87.26194204835767
				],
				[
					87.95845222911922,
					7.219356674957439
				],
				[
					87.48407176050935,
					-0.3431928547433216
				],
				[
					81.81967725989045,
					-4.569951534960701
				],
				[
					69.89167127292335,
					-7.017866506201685
				],
				[
					42.70935725136615,
					-9.076737761892943
				],
				[
					20.91603533578692,
					-7.849028196182914
				],
				[
					3.775735655469765,
					-3.684787148572539
				],
				[
					-0.047697839012426885,
					-0.0517060607782156
				],
				[
					0,
					0
				]
			]
		},
		{
			"type": "line",
			"version": 1902,
			"versionNonce": 350512318,
			"isDeleted": false,
			"id": "kWwmPSCJILlQJYqq7Vjfe",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -546.8652758313692,
			"y": 707.3844349161163,
			"strokeColor": "#0a11d3",
			"backgroundColor": "transparent",
			"width": 88.30808627974527,
			"height": 9.797916664247975,
			"seed": 1998227070,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738080979,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					2.326538897826852,
					3.9056133261361587
				],
				[
					12.359939318521995,
					7.182387014695761
				],
				[
					25.710950037209347,
					9.166781347006062
				],
				[
					46.6269757640547,
					9.347610268342288
				],
				[
					71.03526003420632,
					8.084235941711592
				],
				[
					85.2899738827162,
					3.4881086608341767
				],
				[
					88.30808627974527,
					-0.45030639590568633
				]
			]
		},
		{
			"type": "line",
			"version": 1989,
			"versionNonce": 1454710014,
			"isDeleted": false,
			"id": "ws34AVZd2M1z2UMpLUaAt",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -547.9590173434306,
			"y": 674.3102803540446,
			"strokeColor": "#0a11d3",
			"backgroundColor": "transparent",
			"width": 88.30808627974527,
			"height": 9.797916664247975,
			"seed": 1497433790,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1710738080979,
			"link": null,
			"locked": false,
			"startBinding": null,
			"endBinding": null,
			"lastCommittedPoint": null,
			"startArrowhead": null,
			"endArrowhead": null,
			"points": [
				[
					0,
					0
				],
				[
					2.326538897826852,
					3.9056133261361587
				],
				[
					12.359939318521995,
					7.182387014695761
				],
				[
					25.710950037209347,
					9.166781347006062
				],
				[
					46.6269757640547,
					9.347610268342288
				],
				[
					71.03526003420632,
					8.084235941711592
				],
				[
					85.2899738827162,
					3.4881086608341767
				],
				[
					88.30808627974527,
					-0.45030639590568633
				]
			]
		},
		{
			"type": "ellipse",
			"version": 5008,
			"versionNonce": 1178914110,
			"isDeleted": false,
			"id": "xlUIjbKnC-XZDv1gUi5TS",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -549.0798400295923,
			"y": 634.069610658232,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 87.65074610854188,
			"height": 17.72670397681366,
			"seed": 1798143742,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [
				{
					"id": "I03EtaCnZkkSpr4PSdjUP",
					"type": "arrow"
				}
			],
			"updated": 1710738080979,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 376,
			"versionNonce": 1089762686,
			"isDeleted": false,
			"id": "VxUtTNuoWR0EZW2K9_HTp",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -477.57010772901174,
			"y": 658.6454135353656,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 12.846057046979809,
			"height": 13.941904362416096,
			"seed": 828436286,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738080979,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 425,
			"versionNonce": 1342510526,
			"isDeleted": false,
			"id": "hkZj_mNL9tfREc1R7Y1Lv",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -477.57010772901174,
			"y": 689.2478673944261,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 12.846057046979809,
			"height": 13.941904362416096,
			"seed": 2017220478,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738080979,
			"link": null,
			"locked": false
		},
		{
			"type": "ellipse",
			"version": 479,
			"versionNonce": 748137982,
			"isDeleted": false,
			"id": "ZUhiIGyYwqvokA49ztvwh",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -477.57010772901174,
			"y": 722.5086685689228,
			"strokeColor": "#0a11d3",
			"backgroundColor": "#fff",
			"width": 12.846057046979809,
			"height": 13.941904362416096,
			"seed": 1476442046,
			"groupIds": [
				"iOu_zPivX-vRaGLISDKCs"
			],
			"frameId": null,
			"roundness": null,
			"boundElements": [],
			"updated": 1710738080979,
			"link": null,
			"locked": false
		},
		{
			"id": "KJ1ySnWj",
			"type": "text",
			"x": -581.7463530897334,
			"y": 755.4753596688404,
			"width": 159.2958984375,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1205873534,
			"version": 248,
			"versionNonce": 796635810,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "VihqTQBgWdnFOBYkeF9fw",
					"type": "arrow"
				}
			],
			"updated": 1710738126868,
			"link": null,
			"locked": false,
			"text": "output object store",
			"rawText": "output object store",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 14,
			"containerId": null,
			"originalText": "output object store",
			"lineHeight": 1.25
		},
		{
			"id": "eVKV9HM-J-EfYfX6oI8s4",
			"type": "arrow",
			"x": -561.6789050647702,
			"y": 677.9499027230132,
			"width": 446.4444795702693,
			"height": 498.2895405165244,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 196213410,
			"version": 465,
			"versionNonce": 428660606,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "KIQQK9DV"
				}
			],
			"updated": 1710738115610,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-342.99198269513465,
					-280.24676999477197
				],
				[
					103.45249687513467,
					-498.2895405165244
				]
			],
			"lastCommittedPoint": [
				120.33844408267453,
				-525.9431223778291
			],
			"startBinding": null,
			"endBinding": {
				"elementId": "9qNpybOUKHPQcIZZBTTFx",
				"focus": 1.1298697285677748,
				"gap": 13.545817360681923
			},
			"startArrowhead": "arrow",
			"endArrowhead": null
		},
		{
			"id": "KIQQK9DV",
			"type": "text",
			"x": -986.6401228055886,
			"y": 401.07725894020064,
			"width": 124.19192504882812,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 435994110,
			"version": 34,
			"versionNonce": 219238498,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738105191,
			"link": null,
			"locked": false,
			"text": "write output\nto object store",
			"rawText": "write output\nto object store",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "eVKV9HM-J-EfYfX6oI8s4",
			"originalText": "write output\nto object store",
			"lineHeight": 1.25
		},
		{
			"id": "VihqTQBgWdnFOBYkeF9fw",
			"type": "arrow",
			"x": -410.125418054937,
			"y": 758.0393197596343,
			"width": 890.3489627251126,
			"height": 11.391666146196258,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 536842238,
			"version": 132,
			"versionNonce": 2061029922,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "53CZXVoz"
				}
			],
			"updated": 1710738158957,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					890.3489627251126,
					-11.391666146196258
				]
			],
			"lastCommittedPoint": [
				892.2871385380308,
				-22.89375664584304
			],
			"startBinding": {
				"elementId": "KJ1ySnWj",
				"focus": -0.5680411164558693,
				"gap": 12.32503659729639
			},
			"endBinding": {
				"elementId": "7j5FQDPTS3baFkwDabAEd",
				"focus": -1.1980412866412105,
				"gap": 29.708967322870166
			},
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "53CZXVoz",
			"type": "text",
			"x": -53.85487498583768,
			"y": 732.3434866865362,
			"width": 177.80787658691406,
			"height": 40,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 383380002,
			"version": 77,
			"versionNonce": 847310434,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738158413,
			"link": null,
			"locked": false,
			"text": "database links\nto this for job output",
			"rawText": "database links\nto this for job output",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "VihqTQBgWdnFOBYkeF9fw",
			"originalText": "database links\nto this for job output",
			"lineHeight": 1.25
		},
		{
			"id": "c7XGkYvbGILTwUkWGfVBx",
			"type": "arrow",
			"x": 76.86638002544078,
			"y": 36.008497739545305,
			"width": 133.16027100629958,
			"height": 149.34492117880114,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": {
				"type": 2
			},
			"seed": 376867134,
			"version": 79,
			"versionNonce": 354601278,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1710738192264,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-133.16027100629958,
					149.34492117880114
				]
			],
			"lastCommittedPoint": [
				-133.16027100629958,
				149.34492117880114
			],
			"startBinding": {
				"elementId": "przj2y1M",
				"focus": 0.8931278664085703,
				"gap": 12.115016547116284
			},
			"endBinding": null,
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "przj2y1M",
			"type": "text",
			"x": 88.98139657255706,
			"y": 1.2979175581148752,
			"width": 298.9598083496094,
			"height": 60,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1753295330,
			"version": 175,
			"versionNonce": 2058547582,
			"isDeleted": false,
			"boundElements": [
				{
					"id": "c7XGkYvbGILTwUkWGfVBx",
					"type": "arrow"
				}
			],
			"updated": 1710738192264,
			"link": null,
			"locked": false,
			"text": "in-memory because durability/retry\nlogic is handled by the task scheduler\nalong with the jobs database.",
			"rawText": "in-memory because durability/retry\nlogic is handled by the task scheduler\nalong with the jobs database.",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 54,
			"containerId": null,
			"originalText": "in-memory because durability/retry\nlogic is handled by the task scheduler\nalong with the jobs database.",
			"lineHeight": 1.25
		},
		{
			"id": "pOJvwWVQ",
			"type": "text",
			"x": -70.33377255934329,
			"y": -18.33621377687507,
			"width": 8,
			"height": 20,
			"angle": 0,
			"strokeColor": "#1e1e1e",
			"backgroundColor": "#eeeeee",
			"fillStyle": "solid",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"groupIds": [],
			"frameId": null,
			"roundness": null,
			"seed": 1960899902,
			"version": 3,
			"versionNonce": 395512574,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1710738077495,
			"link": null,
			"locked": false,
			"text": "",
			"rawText": "",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 14,
			"containerId": null,
			"originalText": "",
			"lineHeight": 1.25
		}
	],
	"appState": {
		"theme": "dark",
		"viewBackgroundColor": "#ffffff",
		"currentItemStrokeColor": "#1e1e1e",
		"currentItemBackgroundColor": "#eeeeee",
		"currentItemFillStyle": "solid",
		"currentItemStrokeWidth": 1,
		"currentItemStrokeStyle": "solid",
		"currentItemRoughness": 1,
		"currentItemOpacity": 100,
		"currentItemFontFamily": 1,
		"currentItemFontSize": 16,
		"currentItemTextAlign": "left",
		"currentItemStartArrowhead": null,
		"currentItemEndArrowhead": "arrow",
		"scrollX": 1421.7017404157384,
		"scrollY": 427.97354200592616,
		"zoom": {
			"value": 0.774931311694918
		},
		"currentItemRoundness": "round",
		"gridSize": null,
		"gridColor": {
			"Bold": "#C9C9C9FF",
			"Regular": "#EDEDEDFF"
		},
		"currentStrokeOptions": null,
		"previousGridSize": null,
		"frameRendering": {
			"enabled": true,
			"clip": true,
			"name": true,
			"outline": true
		}
	},
	"files": {}
}
```
%%