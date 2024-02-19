---

excalidraw-plugin: parsed
tags: [excalidraw]

---
==⚠  Switch to EXCALIDRAW VIEW in the MORE OPTIONS menu of this document. ⚠==


# Text Elements
Requirements: ^0p5X1HJh

- 1 on 1 messaging in real-time
- sent, delivered, read receipts
- group messaging?
- online status
- sending images/videos ^KNrWHTed

client 2 ^po8EeNiu

client 1 ^VoDF9yGB

websocket ^LcwV0cYG

message1 ^bt2Ul79e

message1 ^aYhYsZmG

sent ^Hll8Pqbn

received ^Ezihux2C

delivered ^bBGGjabG

read ^pVyBHQnb

read ^YRuJfpvg

session db ^OtFXbzlH

on login: load
balance and save
session machine id ^FbhBH5oe

on open chat:
connect to friend's
machine ^YEbRwpsH

image service ^M4JQVncu

upload image ^EXvkSOiu

object storage ^T6UUgbx8

enqueue save image ^L9jhGl1o

session service ^04DHC73a

message service ^SCkd44vf

save message ^UcNYCB5l

message db ^l5qHPp1p

save ^4Oo2aP4c

sender_id, recipient_id,
content, timestamp ^MIwVhJDn

cache ^FwXVFXVC

retrieve ^FspXMycz

save picture link as
message ^PrVmGRbn

message queue ^lqnmYCMC

save image ^RtYOPTc1

user_id, connected_machine, last_action ^TpNUCUfk

* everytime user makes action,
update timestamp for last_action ^GmYXY71w

* images/videos could
be distributed geographically
with CDNs ^gxQzNkNR

NoSQL - no relationships, just storing data ^IQ5K9Z4q

NoSQL - just storing rows of data ^QjILbeEW

* multiple of these, sessions service will
store which machine each user is connected to ^Ok77EtHh

group service ^FwRo7zIY

find who belongs
to a group ^hP5ZxXeM

groups db ^AkgOjT2T

many to many, SQL
group_id, user_id ^4LFmiLUD

cache ^WD3DsWST

on login:
retrieve all messages
missed since last active ^yttReUFY

cache ^9HDKXcNO

WhatsApp System Design ^nkopXWt9

notification service ^TJzPhGfn

SMS notification service ^uodoWpVo

iOS notification service ^xDKvxxNj

* these send notifications back
to the client ^ceGBvfOU

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
			"versionNonce": 220910995,
			"isDeleted": false,
			"id": "0p5X1HJh",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -407.5486838821787,
			"y": -382.5772746511027,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 132,
			"height": 25,
			"seed": 930547453,
			"groupIds": [
				"0PS8jw4rSzqGxgbuWsKe1"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
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
			"version": 382,
			"versionNonce": 1338327325,
			"isDeleted": false,
			"id": "KNrWHTed",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -406.56142108338554,
			"y": -349.1201654328969,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 245,
			"height": 100,
			"seed": 670202365,
			"groupIds": [
				"0PS8jw4rSzqGxgbuWsKe1"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "- 1 on 1 messaging in real-time\n- sent, delivered, read receipts\n- group messaging?\n- online status\n- sending images/videos",
			"rawText": "- 1 on 1 messaging in real-time\n- sent, delivered, read receipts\n- group messaging?\n- online status\n- sending images/videos",
			"baseline": 94,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "- 1 on 1 messaging in real-time\n- sent, delivered, read receipts\n- group messaging?\n- online status\n- sending images/videos"
		},
		{
			"type": "rectangle",
			"version": 168,
			"versionNonce": 1795205939,
			"isDeleted": false,
			"id": "TA12zevvlTfkwhE5j0In0",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -433.84382202849093,
			"y": -80.05385101991513,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 115,
			"height": 42,
			"seed": 882611613,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "VoDF9yGB"
				},
				{
					"id": "kVW44VuCq5WwG563_bbUZ",
					"type": "arrow"
				},
				{
					"id": "rILLr9yyS3wDyV7E81OrJ",
					"type": "arrow"
				},
				{
					"id": "dbimb5GS_fwn3-t8FGeCq",
					"type": "arrow"
				},
				{
					"id": "f5FoFJVL_jy9XeUN-RxAa",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 41,
			"versionNonce": 1125717373,
			"isDeleted": false,
			"id": "VoDF9yGB",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -403.34382202849093,
			"y": -69.05385101991513,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 54,
			"height": 20,
			"seed": 1395710461,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client 1",
			"rawText": "client 1",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "TA12zevvlTfkwhE5j0In0",
			"originalText": "client 1"
		},
		{
			"type": "rectangle",
			"version": 338,
			"versionNonce": 2078503261,
			"isDeleted": false,
			"id": "dDXWqQCdh0gjOQcZQ4-xk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -433.1527155108709,
			"y": 31.994992716436144,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 115,
			"height": 42,
			"seed": 605913971,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "po8EeNiu"
				},
				{
					"id": "-7KMYCvktGtbon5VJzc34",
					"type": "arrow"
				},
				{
					"id": "4lcyQ-lGX46_3kkNumcIp",
					"type": "arrow"
				},
				{
					"id": "ECuCyrsr7JshBMeiNDoBK",
					"type": "arrow"
				},
				{
					"id": "2JTKjO3hbh-br6echjWUC",
					"type": "arrow"
				},
				{
					"id": "-IfIgyQnRAUIpVRjO6bek",
					"type": "arrow"
				}
			],
			"updated": 1674849263265,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 209,
			"versionNonce": 1504927197,
			"isDeleted": false,
			"id": "po8EeNiu",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -406.1527155108709,
			"y": 42.994992716436144,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 61,
			"height": 20,
			"seed": 575212733,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "client 2",
			"rawText": "client 2",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dDXWqQCdh0gjOQcZQ4-xk",
			"originalText": "client 2"
		},
		{
			"type": "rectangle",
			"version": 339,
			"versionNonce": 1411365491,
			"isDeleted": false,
			"id": "GTAPFCdYWjwseby8gFsgi",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -58.80302527098928,
			"y": -44.72957989791445,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 138,
			"height": 55,
			"seed": 1947532125,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "LcwV0cYG"
				},
				{
					"id": "kVW44VuCq5WwG563_bbUZ",
					"type": "arrow"
				},
				{
					"id": "-7KMYCvktGtbon5VJzc34",
					"type": "arrow"
				},
				{
					"id": "rILLr9yyS3wDyV7E81OrJ",
					"type": "arrow"
				},
				{
					"id": "4lcyQ-lGX46_3kkNumcIp",
					"type": "arrow"
				},
				{
					"id": "dbimb5GS_fwn3-t8FGeCq",
					"type": "arrow"
				},
				{
					"id": "ECuCyrsr7JshBMeiNDoBK",
					"type": "arrow"
				},
				{
					"id": "f5FoFJVL_jy9XeUN-RxAa",
					"type": "arrow"
				},
				{
					"id": "rv7R1wWFBY5BqqnJ9m5m5",
					"type": "arrow"
				},
				{
					"id": "A-e8Ub1lPNF9Dry9sgPSn",
					"type": "arrow"
				},
				{
					"id": "exWNPq3GVTcb2G_k8vs4r",
					"type": "arrow"
				},
				{
					"id": "7v7ofv_de8l7jeWDATTFq",
					"type": "arrow"
				},
				{
					"id": "KQLFT-dDEpK912tTdPFtg",
					"type": "arrow"
				},
				{
					"id": "-IfIgyQnRAUIpVRjO6bek",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 314,
			"versionNonce": 1252366909,
			"isDeleted": false,
			"id": "LcwV0cYG",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -33.30302527098928,
			"y": -28.229579897914448,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 87,
			"height": 22,
			"seed": 181688925,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 17.684919915743386,
			"fontFamily": 1,
			"text": "websocket",
			"rawText": "websocket",
			"baseline": 15,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "GTAPFCdYWjwseby8gFsgi",
			"originalText": "websocket"
		},
		{
			"type": "arrow",
			"version": 434,
			"versionNonce": 1338373139,
			"isDeleted": false,
			"id": "kVW44VuCq5WwG563_bbUZ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -311.0477966488277,
			"y": -65.01401385260978,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"width": 243.7572165934859,
			"height": 52.24289694173043,
			"seed": 1245519869,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "bt2Ul79e"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "TA12zevvlTfkwhE5j0In0",
				"gap": 7.79602537966322,
				"focus": -0.5988091858868558
			},
			"endBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 8.487554784352547,
				"focus": -0.4981485592286701
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
					243.7572165934859,
					52.24289694173043
				]
			]
		},
		{
			"type": "text",
			"version": 17,
			"versionNonce": 1859209885,
			"isDeleted": false,
			"id": "bt2Ul79e",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -225.91735395056367,
			"y": -46.64285673898229,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"width": 69,
			"height": 20,
			"seed": 86422973,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "message1",
			"rawText": "message1",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kVW44VuCq5WwG563_bbUZ",
			"originalText": "message1"
		},
		{
			"type": "arrow",
			"version": 541,
			"versionNonce": 431225267,
			"isDeleted": false,
			"id": "-7KMYCvktGtbon5VJzc34",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -68.57330938388162,
			"y": -0.8505160058683394,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"width": 240.43358060422213,
			"height": 50.972937079134326,
			"seed": 1089099549,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "aYhYsZmG"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 9.770284112892346,
				"focus": 0.007609431660573079
			},
			"endBinding": {
				"elementId": "dDXWqQCdh0gjOQcZQ4-xk",
				"gap": 9.145825522767163,
				"focus": 0.33915465430116715
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
					-240.43358060422213,
					50.972937079134326
				]
			]
		},
		{
			"type": "text",
			"version": 16,
			"versionNonce": 115863293,
			"isDeleted": false,
			"id": "aYhYsZmG",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -224.28557467284983,
			"y": 22.959029526695232,
			"strokeColor": "#5c940d",
			"backgroundColor": "transparent",
			"width": 69,
			"height": 20,
			"seed": 283306845,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "message1",
			"rawText": "message1",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "-7KMYCvktGtbon5VJzc34",
			"originalText": "message1"
		},
		{
			"type": "arrow",
			"version": 172,
			"versionNonce": 789597011,
			"isDeleted": false,
			"id": "rILLr9yyS3wDyV7E81OrJ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -68.12058138557339,
			"y": -22.935070787846094,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 242.94938777876692,
			"height": 63.74929594253152,
			"seed": 1287673203,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Hll8Pqbn"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 9.317556114584116,
				"focus": -0.5805278791040168
			},
			"endBinding": {
				"elementId": "TA12zevvlTfkwhE5j0In0",
				"gap": 7.773852864150626,
				"focus": -0.5213350477265332
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
					-112.55742522058526,
					-63.74929594253152
				],
				[
					-242.94938777876692,
					-54.10899993517497
				]
			]
		},
		{
			"type": "text",
			"version": 12,
			"versionNonce": 1097533277,
			"isDeleted": false,
			"id": "Hll8Pqbn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -198.17800660615865,
			"y": -96.68436673037769,
			"strokeColor": "#343a40",
			"backgroundColor": "transparent",
			"width": 35,
			"height": 20,
			"seed": 180396317,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "sent",
			"rawText": "sent",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rILLr9yyS3wDyV7E81OrJ",
			"originalText": "sent"
		},
		{
			"type": "arrow",
			"version": 144,
			"versionNonce": 607217907,
			"isDeleted": false,
			"id": "4lcyQ-lGX46_3kkNumcIp",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -309.6813569946779,
			"y": 66.94605248277594,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 268.757494329938,
			"height": 51.35265471260956,
			"seed": 894888787,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "Ezihux2C"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dDXWqQCdh0gjOQcZQ4-xk",
				"gap": 8.471358516192993,
				"focus": 0.5413612473168945
			},
			"endBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 8.925690347896113,
				"focus": -0.30937106069599773
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
					135.4600770207282,
					3.6027126798152835
				],
				[
					268.757494329938,
					-47.74994203279427
				]
			]
		},
		{
			"type": "text",
			"version": 16,
			"versionNonce": 11277245,
			"isDeleted": false,
			"id": "Ezihux2C",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -205.72127997394972,
			"y": 60.54876516259122,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 63,
			"height": 20,
			"seed": 923825149,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "received",
			"rawText": "received",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "4lcyQ-lGX46_3kkNumcIp",
			"originalText": "received"
		},
		{
			"type": "arrow",
			"version": 187,
			"versionNonce": 1050530451,
			"isDeleted": false,
			"id": "dbimb5GS_fwn3-t8FGeCq",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -39.13458068921145,
			"y": -54.9914145262326,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 306.89385982473993,
			"height": 67.04497032073407,
			"seed": 453607859,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "bBGGjabG"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 10.26183462831815,
				"focus": 0.22243769606012465
			},
			"endBinding": {
				"elementId": "TA12zevvlTfkwhE5j0In0",
				"gap": 10.35161237709238,
				"focus": -0.8107302390150383
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
					-137.0352357163613,
					-67.04497032073407
				],
				[
					-306.89385982473993,
					-35.414048870774906
				]
			]
		},
		{
			"type": "text",
			"version": 19,
			"versionNonce": 1624019997,
			"isDeleted": false,
			"id": "bBGGjabG",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -210.66981640557276,
			"y": -132.0363848469666,
			"strokeColor": "#364fc7",
			"backgroundColor": "transparent",
			"width": 68,
			"height": 20,
			"seed": 2094142429,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "delivered",
			"rawText": "delivered",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "dbimb5GS_fwn3-t8FGeCq",
			"originalText": "delivered"
		},
		{
			"type": "arrow",
			"version": 175,
			"versionNonce": 1326188595,
			"isDeleted": false,
			"id": "ECuCyrsr7JshBMeiNDoBK",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -342.1505650539724,
			"y": 84.3484985445125,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 368.764517412283,
			"height": 87.04598568124766,
			"seed": 245726845,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "pVyBHQnb"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dDXWqQCdh0gjOQcZQ4-xk",
				"gap": 10.35350582807635,
				"focus": 0.9953079563820474
			},
			"endBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 8.344409955006654,
				"focus": -0.7247780902723936
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
					185.00857485342766,
					21.31231719382737
				],
				[
					368.764517412283,
					-65.73366848742029
				]
			]
		},
		{
			"type": "text",
			"version": 17,
			"versionNonce": 2109606013,
			"isDeleted": false,
			"id": "pVyBHQnb",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -175.64199020054474,
			"y": 95.66081573833986,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 36,
			"height": 20,
			"seed": 1629467933,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "read",
			"rawText": "read",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ECuCyrsr7JshBMeiNDoBK",
			"originalText": "read"
		},
		{
			"type": "arrow",
			"version": 164,
			"versionNonce": 1264749011,
			"isDeleted": false,
			"id": "f5FoFJVL_jy9XeUN-RxAa",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 0.5319162851173758,
			"y": -55.29323319177137,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 391.81183586712154,
			"height": 102.94625464996437,
			"seed": 1500710941,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "YRuJfpvg"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 10.563653293856937,
				"focus": 0.4670577508426219
			},
			"endBinding": {
				"elementId": "TA12zevvlTfkwhE5j0In0",
				"gap": 10.591579917932648,
				"focus": -0.9368396849590622
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
					-171.0033034875365,
					-102.94625464996437
				],
				[
					-391.81183586712154,
					-35.352197746076406
				]
			]
		},
		{
			"type": "text",
			"version": 12,
			"versionNonce": 2034364637,
			"isDeleted": false,
			"id": "YRuJfpvg",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -187.7363542588945,
			"y": -173.72994517616115,
			"strokeColor": "#e67700",
			"backgroundColor": "transparent",
			"width": 36,
			"height": 20,
			"seed": 750387411,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "read",
			"rawText": "read",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "f5FoFJVL_jy9XeUN-RxAa",
			"originalText": "read"
		},
		{
			"type": "arrow",
			"version": 855,
			"versionNonce": 683136883,
			"isDeleted": false,
			"id": "rv7R1wWFBY5BqqnJ9m5m5",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 63.74735489975018,
			"y": -227.8240007123723,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 10.783584961350812,
			"height": 167.76583285628874,
			"seed": 1776590131,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FbhBH5oe"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "wk0OG2eXShtaQMI7xGgaz",
				"focus": 0.08631384722323514,
				"gap": 14.349478572943951
			},
			"endBinding": {
				"elementId": "WJLn027li1oCD6GbzopC5",
				"focus": -0.014943616964340404,
				"gap": 9.921752829605076
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
					-10.783584961350812,
					-167.76583285628874
				]
			]
		},
		{
			"type": "text",
			"version": 175,
			"versionNonce": 1089064253,
			"isDeleted": false,
			"id": "FbhBH5oe",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -2.481980119479431,
			"y": -269.9477173240938,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 141,
			"height": 60,
			"seed": 2008539453,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "on login: load\nbalance and save\nsession machine id",
			"rawText": "on login: load\nbalance and save\nsession machine id",
			"baseline": 54,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "rv7R1wWFBY5BqqnJ9m5m5",
			"originalText": "on login: load\nbalance and save\nsession machine id"
		},
		{
			"type": "arrow",
			"version": 762,
			"versionNonce": 1968337171,
			"isDeleted": false,
			"id": "A-e8Ub1lPNF9Dry9sgPSn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 135.96678507871252,
			"y": -195.00039485177354,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 128.23773020547824,
			"height": 213.90995602967865,
			"seed": 372723997,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "YEbRwpsH"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "wk0OG2eXShtaQMI7xGgaz",
				"focus": 0.6419596553587327,
				"gap": 10.292417527729754
			},
			"endBinding": {
				"elementId": "WJLn027li1oCD6GbzopC5",
				"focus": -0.137082373724932,
				"gap": 5.764060358515664
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
					73.63360251552228,
					-58.5289660123849
				],
				[
					-54.60412768995596,
					-213.90995602967865
				]
			]
		},
		{
			"type": "text",
			"version": 114,
			"versionNonce": 337059229,
			"isDeleted": false,
			"id": "YEbRwpsH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 136.12909553338238,
			"y": -165.6031858808301,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 149,
			"height": 60,
			"seed": 773447731,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "on open chat:\nconnect to friend's\nmachine",
			"rawText": "on open chat:\nconnect to friend's\nmachine",
			"baseline": 54,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "A-e8Ub1lPNF9Dry9sgPSn",
			"originalText": "on open chat:\nconnect to friend's\nmachine"
		},
		{
			"type": "rectangle",
			"version": 231,
			"versionNonce": 849925811,
			"isDeleted": false,
			"id": "8ogjjt1K-TUh9Y7in_-em",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -541.9482590014958,
			"y": 223.5701375031707,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 133,
			"height": 58,
			"seed": 89238973,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "M4JQVncu"
				},
				{
					"id": "2JTKjO3hbh-br6echjWUC",
					"type": "arrow"
				},
				{
					"id": "Od4OIOLnVt9hwko2kBl_1",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 156,
			"versionNonce": 1241211389,
			"isDeleted": false,
			"id": "M4JQVncu",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -526.9482590014958,
			"y": 242.5701375031707,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103,
			"height": 20,
			"seed": 261073373,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "image service",
			"rawText": "image service",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "8ogjjt1K-TUh9Y7in_-em",
			"originalText": "image service"
		},
		{
			"type": "arrow",
			"version": 348,
			"versionNonce": 1868662867,
			"isDeleted": false,
			"id": "2JTKjO3hbh-br6echjWUC",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -380.4961545907526,
			"y": 84.01734245551881,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 95.01175739493891,
			"height": 127.49911173125204,
			"seed": 1359897875,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "EXvkSOiu"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "dDXWqQCdh0gjOQcZQ4-xk",
				"gap": 10.02234973908267,
				"focus": -0.024310546560194525
			},
			"endBinding": {
				"elementId": "8ogjjt1K-TUh9Y7in_-em",
				"gap": 12.053683316399855,
				"focus": -0.5031523804883026
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
					-12.748416300468364,
					62.32319689423991
				],
				[
					-95.01175739493891,
					127.49911173125204
				]
			]
		},
		{
			"type": "text",
			"version": 19,
			"versionNonce": 1469586013,
			"isDeleted": false,
			"id": "EXvkSOiu",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -402.81480298721533,
			"y": 142.26271616490578,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 100,
			"height": 20,
			"seed": 270445107,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "upload image",
			"rawText": "upload image",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "2JTKjO3hbh-br6echjWUC",
			"originalText": "upload image"
		},
		{
			"type": "ellipse",
			"version": 712,
			"versionNonce": 559089139,
			"isDeleted": false,
			"id": "i1wfVMiW_-Q53ClsQ4IRq",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -237.64042063978184,
			"y": 486.6546123729029,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 138,
			"height": 136,
			"seed": 1263550941,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "T6UUgbx8"
				},
				{
					"id": "Od4OIOLnVt9hwko2kBl_1",
					"type": "arrow"
				},
				{
					"id": "kq12wgI1DhSYq2kjoW5cD",
					"type": "arrow"
				},
				{
					"id": "umR_zKGQBv3TCoGIUczOf",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 670,
			"versionNonce": 364824253,
			"isDeleted": false,
			"id": "T6UUgbx8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -227.64042063978184,
			"y": 544.6546123729029,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 118,
			"height": 20,
			"seed": 1527260253,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "object storage",
			"rawText": "object storage",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "i1wfVMiW_-Q53ClsQ4IRq",
			"originalText": "object storage"
		},
		{
			"type": "arrow",
			"version": 1936,
			"versionNonce": 1065602963,
			"isDeleted": false,
			"id": "Od4OIOLnVt9hwko2kBl_1",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -470.9772086620924,
			"y": 293.12373066168567,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 48.00056972740481,
			"height": 100.15750675961033,
			"seed": 1293151059,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "L9jhGl1o"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "8ogjjt1K-TUh9Y7in_-em",
				"gap": 11.553593158514957,
				"focus": 0.18612704731080965
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
					48.00056972740481,
					100.15750675961033
				]
			]
		},
		{
			"type": "text",
			"version": 234,
			"versionNonce": 1192290077,
			"isDeleted": false,
			"id": "L9jhGl1o",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -524.47692379839,
			"y": 333.20248404149083,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 155,
			"height": 20,
			"seed": 1423786365,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "enqueue save image",
			"rawText": "enqueue save image",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "Od4OIOLnVt9hwko2kBl_1",
			"originalText": "enqueue save image"
		},
		{
			"type": "rectangle",
			"version": 189,
			"versionNonce": 472540467,
			"isDeleted": false,
			"id": "wk0OG2eXShtaQMI7xGgaz",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -4.325632449017235,
			"y": -213.47452213942836,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 130,
			"height": 55,
			"seed": 2045792659,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "04DHC73a"
				},
				{
					"id": "rv7R1wWFBY5BqqnJ9m5m5",
					"type": "arrow"
				},
				{
					"id": "A-e8Ub1lPNF9Dry9sgPSn",
					"type": "arrow"
				},
				{
					"id": "exWNPq3GVTcb2G_k8vs4r",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 140,
			"versionNonce": 1577057149,
			"isDeleted": false,
			"id": "04DHC73a",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 2.1743675509827654,
			"y": -195.97452213942836,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 117,
			"height": 20,
			"seed": 490374237,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "session service",
			"rawText": "session service",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "wk0OG2eXShtaQMI7xGgaz",
			"originalText": "session service"
		},
		{
			"type": "arrow",
			"version": 231,
			"versionNonce": 2125285075,
			"isDeleted": false,
			"id": "exWNPq3GVTcb2G_k8vs4r",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 15.722012488902113,
			"y": -54.199966582790225,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 41.071392677903944,
			"height": 95.89307082196201,
			"seed": 1886062963,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 9.470386684875766,
				"focus": -0.12763066963999153
			},
			"endBinding": {
				"elementId": "wk0OG2eXShtaQMI7xGgaz",
				"gap": 8.381484734676132,
				"focus": -0.14961537769681651
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
					41.071392677903944,
					-95.89307082196201
				]
			]
		},
		{
			"type": "rectangle",
			"version": 100,
			"versionNonce": 47023069,
			"isDeleted": false,
			"id": "BAlKrNNBGe7yWzqZDxfvL",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 23.784860453885585,
			"y": 167.67911958678928,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 143,
			"height": 55,
			"seed": 1159023805,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "SCkd44vf"
				},
				{
					"id": "7v7ofv_de8l7jeWDATTFq",
					"type": "arrow"
				},
				{
					"id": "XsfaV8EYypFVkKlksV-Hb",
					"type": "arrow"
				},
				{
					"id": "byPiKktsYe2szZieGqoKH",
					"type": "arrow"
				},
				{
					"id": "agTtPjO94sMarRh-yfHb8",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 37,
			"versionNonce": 2107831411,
			"isDeleted": false,
			"id": "SCkd44vf",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 32.284860453885585,
			"y": 185.17911958678928,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 126,
			"height": 20,
			"seed": 43696563,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "message service",
			"rawText": "message service",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "BAlKrNNBGe7yWzqZDxfvL",
			"originalText": "message service"
		},
		{
			"type": "arrow",
			"version": 85,
			"versionNonce": 1502281789,
			"isDeleted": false,
			"id": "7v7ofv_de8l7jeWDATTFq",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 52.849956508533104,
			"y": 18.128519569097733,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 30.34138499371877,
			"height": 137.45234347421652,
			"seed": 825414237,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "UcNYCB5l"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 7.858099467012191,
				"focus": -0.46421449659191943
			},
			"endBinding": {
				"elementId": "BAlKrNNBGe7yWzqZDxfvL",
				"gap": 12.098256543475028,
				"focus": -0.04321952780778302
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
					30.34138499371877,
					137.45234347421652
				]
			]
		},
		{
			"type": "text",
			"version": 17,
			"versionNonce": 416411155,
			"isDeleted": false,
			"id": "UcNYCB5l",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 12.992499815994961,
			"y": 104.81635115692114,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 109,
			"height": 20,
			"seed": 314586547,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "save message",
			"rawText": "save message",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "7v7ofv_de8l7jeWDATTFq",
			"originalText": "save message"
		},
		{
			"type": "ellipse",
			"version": 130,
			"versionNonce": 135917725,
			"isDeleted": false,
			"id": "1-Zb5vpQJ-hUy2MeYUyv8",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 118.22612817559059,
			"y": 354.9531874487626,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 122,
			"height": 122,
			"seed": 1213431699,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "l5qHPp1p"
				},
				{
					"id": "XsfaV8EYypFVkKlksV-Hb",
					"type": "arrow"
				},
				{
					"id": "8NESEB27JBVlSpRaIPt6y",
					"type": "arrow"
				},
				{
					"id": "kq12wgI1DhSYq2kjoW5cD",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 101,
			"versionNonce": 321958835,
			"isDeleted": false,
			"id": "l5qHPp1p",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 134.2261281755906,
			"y": 405.9531874487626,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 90,
			"height": 20,
			"seed": 65731037,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "message db",
			"rawText": "message db",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "1-Zb5vpQJ-hUy2MeYUyv8",
			"originalText": "message db"
		},
		{
			"type": "arrow",
			"version": 252,
			"versionNonce": 2083247357,
			"isDeleted": false,
			"id": "XsfaV8EYypFVkKlksV-Hb",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 111.22952611931339,
			"y": 236.10210653052252,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 49.73401375614458,
			"height": 107.42407161379685,
			"seed": 220393597,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "4Oo2aP4c"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "BAlKrNNBGe7yWzqZDxfvL",
				"gap": 13.422986943733235,
				"focus": 0.03563278529425893
			},
			"endBinding": {
				"elementId": "1-Zb5vpQJ-hUy2MeYUyv8",
				"gap": 13.694001152743496,
				"focus": 0.22714693841961822
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
					49.73401375614458,
					107.42407161379685
				]
			]
		},
		{
			"type": "text",
			"version": 12,
			"versionNonce": 216384851,
			"isDeleted": false,
			"id": "4Oo2aP4c",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 183.04517680787012,
			"y": 263.61159191873065,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 37,
			"height": 20,
			"seed": 1492602429,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "save",
			"rawText": "save",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "XsfaV8EYypFVkKlksV-Hb",
			"originalText": "save"
		},
		{
			"type": "text",
			"version": 244,
			"versionNonce": 1900162397,
			"isDeleted": false,
			"id": "MIwVhJDn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 112.6519639811927,
			"y": 485.76789150570335,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 181,
			"height": 40,
			"seed": 312290195,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "sender_id, recipient_id,\ncontent, timestamp",
			"rawText": "sender_id, recipient_id,\ncontent, timestamp",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "sender_id, recipient_id,\ncontent, timestamp"
		},
		{
			"type": "ellipse",
			"version": 100,
			"versionNonce": 1564975859,
			"isDeleted": false,
			"id": "HorK1Ku7_eDSKasQy2ogh",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 296.76904573708043,
			"y": 240.08604666043243,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 92,
			"height": 76,
			"seed": 412407069,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FwXVFXVC"
				},
				{
					"id": "8NESEB27JBVlSpRaIPt6y",
					"type": "arrow"
				},
				{
					"id": "byPiKktsYe2szZieGqoKH",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 47,
			"versionNonce": 917404093,
			"isDeleted": false,
			"id": "FwXVFXVC",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 320.76904573708043,
			"y": 268.08604666043243,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 44,
			"height": 20,
			"seed": 661994675,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "cache",
			"rawText": "cache",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "HorK1Ku7_eDSKasQy2ogh",
			"originalText": "cache"
		},
		{
			"type": "arrow",
			"version": 116,
			"versionNonce": 752667795,
			"isDeleted": false,
			"id": "8NESEB27JBVlSpRaIPt6y",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 236.9727373115265,
			"y": 370.8933436670106,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 65.4910489336255,
			"height": 63.345657065109776,
			"seed": 687467731,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "1-Zb5vpQJ-hUy2MeYUyv8",
				"gap": 12.246572536429653,
				"focus": 0.12716137880551237
			},
			"endBinding": {
				"elementId": "HorK1Ku7_eDSKasQy2ogh",
				"gap": 7.17119295840515,
				"focus": 0.16275810320970632
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
					65.4910489336255,
					-63.345657065109776
				]
			]
		},
		{
			"type": "arrow",
			"version": 171,
			"versionNonce": 898775581,
			"isDeleted": false,
			"id": "byPiKktsYe2szZieGqoKH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 307.4063211786402,
			"y": 235.88743027492592,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 129.91887882655016,
			"height": 39.1552080196505,
			"seed": 1984028733,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FspXMycz"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "HorK1Ku7_eDSKasQy2ogh",
				"gap": 14.161081203696845,
				"focus": 0.7797519490182929
			},
			"endBinding": {
				"elementId": "BAlKrNNBGe7yWzqZDxfvL",
				"gap": 10.702581898204471,
				"focus": -0.47343193727316696
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
					-129.91887882655016,
					-39.1552080196505
				]
			]
		},
		{
			"type": "text",
			"version": 18,
			"versionNonce": 1331413555,
			"isDeleted": false,
			"id": "FspXMycz",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 209.95131997728333,
			"y": 200.89415692398524,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 62,
			"height": 20,
			"seed": 811741011,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "retrieve",
			"rawText": "retrieve",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "byPiKktsYe2szZieGqoKH",
			"originalText": "retrieve"
		},
		{
			"type": "arrow",
			"version": 718,
			"versionNonce": 920579709,
			"isDeleted": false,
			"id": "kq12wgI1DhSYq2kjoW5cD",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -89.28054998832395,
			"y": 523.3657622394376,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 198.83794583672355,
			"height": 77.02800198198236,
			"seed": 709074013,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "PrVmGRbn"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "i1wfVMiW_-Q53ClsQ4IRq",
				"gap": 16.441827491011665,
				"focus": -0.007465372399993953
			},
			"endBinding": {
				"elementId": "1-Zb5vpQJ-hUy2MeYUyv8",
				"gap": 15.00627953560501,
				"focus": -0.05190592596882844
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
					198.83794583672355,
					-77.02800198198236
				]
			]
		},
		{
			"type": "text",
			"version": 43,
			"versionNonce": 1571488723,
			"isDeleted": false,
			"id": "PrVmGRbn",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -257.0350925477168,
			"y": 435.22797119858575,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 157,
			"height": 40,
			"seed": 774198355,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "save picture link as\nmessage",
			"rawText": "save picture link as\nmessage",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "kq12wgI1DhSYq2kjoW5cD",
			"originalText": "save picture link as\nmessage"
		},
		{
			"type": "diamond",
			"version": 346,
			"versionNonce": 1767249629,
			"isDeleted": false,
			"id": "ksDJJaWhONgRU99KzE-d3",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -485.95581051834915,
			"y": 404.45005687657016,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 156,
			"height": 66,
			"seed": 34037629,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "lqnmYCMC"
				},
				{
					"id": "umR_zKGQBv3TCoGIUczOf",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 319,
			"versionNonce": 266408307,
			"isDeleted": false,
			"id": "lqnmYCMC",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -466.45581051834915,
			"y": 427.45005687657016,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 117,
			"height": 20,
			"seed": 1293974173,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "message queue",
			"rawText": "message queue",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "ksDJJaWhONgRU99KzE-d3",
			"originalText": "message queue"
		},
		{
			"type": "arrow",
			"version": 260,
			"versionNonce": 1425627155,
			"isDeleted": false,
			"id": "umR_zKGQBv3TCoGIUczOf",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -368.735969502001,
			"y": 465.3021499370948,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 118.03109690039196,
			"height": 67.4674407453208,
			"seed": 115110099,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "RtYOPTc1"
				}
			],
			"updated": 1674849322431,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "ksDJJaWhONgRU99KzE-d3",
				"focus": 0.16465891692095225,
				"gap": 10.54056479142125
			},
			"endBinding": {
				"elementId": "i1wfVMiW_-Q53ClsQ4IRq",
				"focus": -0.31832481534057233,
				"gap": 15.999911757998447
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
					118.03109690039196,
					67.4674407453208
				]
			]
		},
		{
			"type": "text",
			"version": 15,
			"versionNonce": 1464101651,
			"isDeleted": false,
			"id": "RtYOPTc1",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -361.5281592212398,
			"y": 507.94728598338725,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 87,
			"height": 20,
			"seed": 1628144189,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "save image",
			"rawText": "save image",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "umR_zKGQBv3TCoGIUczOf",
			"originalText": "save image"
		},
		{
			"type": "text",
			"version": 106,
			"versionNonce": 2111423389,
			"isDeleted": false,
			"id": "GmYXY71w",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 131.35081846616595,
			"y": -163.63221317354777,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 274,
			"height": 40,
			"seed": 159695315,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "* everytime user makes action,\nupdate timestamp for last_action",
			"rawText": "* everytime user makes action,\nupdate timestamp for last_action",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "* everytime user makes action,\nupdate timestamp for last_action"
		},
		{
			"type": "text",
			"version": 90,
			"versionNonce": 944476339,
			"isDeleted": false,
			"id": "gxQzNkNR",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": -263.42214183695114,
			"y": 628.8018076065123,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 223,
			"height": 60,
			"seed": 448735901,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "* images/videos could\nbe distributed geographically\nwith CDNs",
			"rawText": "* images/videos could\nbe distributed geographically\nwith CDNs",
			"baseline": 54,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "* images/videos could\nbe distributed geographically\nwith CDNs"
		},
		{
			"type": "ellipse",
			"version": 548,
			"versionNonce": 1886996477,
			"isDeleted": false,
			"id": "RmZPM0tC44kJKMfc-CVFT",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 243.36881751666874,
			"y": -460.52902947933967,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 108,
			"height": 62,
			"seed": 195242899,
			"groupIds": [
				"xlUTIcJjxjiWDR5KQcsFT",
				"AXV0SN30M6g6FJcpBpZ9k"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "OtFXbzlH"
				},
				{
					"id": "rv7R1wWFBY5BqqnJ9m5m5",
					"type": "arrow"
				},
				{
					"id": "A-e8Ub1lPNF9Dry9sgPSn",
					"type": "arrow"
				},
				{
					"id": "QmQQjLRYqPVAkoeMz9GTU",
					"type": "arrow"
				}
			],
			"updated": 1674849247698,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 486,
			"versionNonce": 1688011347,
			"isDeleted": false,
			"id": "OtFXbzlH",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 256.86881751666874,
			"y": -439.52902947933967,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 81,
			"height": 20,
			"seed": 329925747,
			"groupIds": [
				"xlUTIcJjxjiWDR5KQcsFT",
				"AXV0SN30M6g6FJcpBpZ9k"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "session db",
			"rawText": "session db",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "RmZPM0tC44kJKMfc-CVFT",
			"originalText": "session db"
		},
		{
			"type": "text",
			"version": 261,
			"versionNonce": 23674973,
			"isDeleted": false,
			"id": "TpNUCUfk",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 367.42865373008635,
			"y": -440.9714828431673,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 323,
			"height": 20,
			"seed": 1250323197,
			"groupIds": [
				"xlUTIcJjxjiWDR5KQcsFT",
				"AXV0SN30M6g6FJcpBpZ9k"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "user_id, connected_machine, last_action",
			"rawText": "user_id, connected_machine, last_action",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "user_id, connected_machine, last_action"
		},
		{
			"type": "text",
			"version": 130,
			"versionNonce": 353320947,
			"isDeleted": false,
			"id": "IQ5K9Z4q",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 364.13942767348635,
			"y": -419.5353008560842,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 346,
			"height": 20,
			"seed": 699762803,
			"groupIds": [
				"AXV0SN30M6g6FJcpBpZ9k"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247698,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "NoSQL - no relationships, just storing data",
			"rawText": "NoSQL - no relationships, just storing data",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "NoSQL - no relationships, just storing data"
		},
		{
			"type": "text",
			"version": 66,
			"versionNonce": 1987783869,
			"isDeleted": false,
			"id": "QjILbeEW",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 112.35883040492376,
			"y": 534.7204017577599,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 280,
			"height": 20,
			"seed": 326884925,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "NoSQL - just storing rows of data",
			"rawText": "NoSQL - just storing rows of data",
			"baseline": 14,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "NoSQL - just storing rows of data"
		},
		{
			"type": "text",
			"version": 171,
			"versionNonce": 598264211,
			"isDeleted": false,
			"id": "Ok77EtHh",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 98.82285836966821,
			"y": -36.95506413271892,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 367,
			"height": 40,
			"seed": 1131193555,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "* multiple of these, sessions service will\nstore which machine each user is connected to",
			"rawText": "* multiple of these, sessions service will\nstore which machine each user is connected to",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "* multiple of these, sessions service will\nstore which machine each user is connected to"
		},
		{
			"type": "rectangle",
			"version": 230,
			"versionNonce": 1599114525,
			"isDeleted": false,
			"id": "VNldjvRW0ZioF80N8jCSa",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 397.8039386084562,
			"y": 92.15099763885456,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 145,
			"height": 53,
			"seed": 1011605299,
			"groupIds": [],
			"roundness": {
				"type": 3
			},
			"boundElements": [
				{
					"type": "text",
					"id": "FwRo7zIY"
				},
				{
					"id": "KQLFT-dDEpK912tTdPFtg",
					"type": "arrow"
				},
				{
					"id": "dIAoPsPSQCQCue3kCx9IW",
					"type": "arrow"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 204,
			"versionNonce": 1704992563,
			"isDeleted": false,
			"id": "FwRo7zIY",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 418.8039386084562,
			"y": 108.65099763885456,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103,
			"height": 20,
			"seed": 1636546131,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "group service",
			"rawText": "group service",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "VNldjvRW0ZioF80N8jCSa",
			"originalText": "group service"
		},
		{
			"type": "arrow",
			"version": 340,
			"versionNonce": 1532682621,
			"isDeleted": false,
			"id": "KQLFT-dDEpK912tTdPFtg",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 80.99635261545217,
			"y": 12.66791893327433,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 305.7321161139037,
			"height": 98.56706318103502,
			"seed": 362142995,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "hP5ZxXeM"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"startBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"gap": 2.9976259646203403,
				"focus": -0.09518157358407603
			},
			"endBinding": {
				"elementId": "VNldjvRW0ZioF80N8jCSa",
				"gap": 11.075469879100297,
				"focus": -0.14771001787282317
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
					145.4939776814486,
					73.65093153137525
				],
				[
					305.7321161139037,
					98.56706318103502
				]
			]
		},
		{
			"type": "text",
			"version": 37,
			"versionNonce": 1163641043,
			"isDeleted": false,
			"id": "hP5ZxXeM",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 144.53822699765237,
			"y": 57.25511588597635,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 125,
			"height": 40,
			"seed": 1893423741,
			"groupIds": [],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "find who belongs\nto a group",
			"rawText": "find who belongs\nto a group",
			"baseline": 34,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "KQLFT-dDEpK912tTdPFtg",
			"originalText": "find who belongs\nto a group"
		},
		{
			"type": "ellipse",
			"version": 231,
			"versionNonce": 534489565,
			"isDeleted": false,
			"id": "YumMmuH3a-yWYF9jVaUbJ",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 553.9660309597456,
			"y": 221.4642118948916,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 117,
			"height": 88,
			"seed": 602688819,
			"groupIds": [
				"7E6xlXYcXZCVLhBVKHuW8"
			],
			"roundness": {
				"type": 2
			},
			"boundElements": [
				{
					"type": "text",
					"id": "AkgOjT2T"
				},
				{
					"id": "WMjhkWSe_mYPutrlwO7FS",
					"type": "arrow"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"type": "text",
			"version": 214,
			"versionNonce": 477245043,
			"isDeleted": false,
			"id": "AkgOjT2T",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 574.4660309597456,
			"y": 255.4642118948916,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 76,
			"height": 20,
			"seed": 50716669,
			"groupIds": [
				"7E6xlXYcXZCVLhBVKHuW8"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "groups db",
			"rawText": "groups db",
			"baseline": 14,
			"textAlign": "center",
			"verticalAlign": "middle",
			"containerId": "YumMmuH3a-yWYF9jVaUbJ",
			"originalText": "groups db"
		},
		{
			"type": "text",
			"version": 206,
			"versionNonce": 1038378557,
			"isDeleted": false,
			"id": "4LFmiLUD",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 689.7846276733994,
			"y": 242.20373674114273,
			"strokeColor": "#495057",
			"backgroundColor": "transparent",
			"width": 148,
			"height": 40,
			"seed": 1342413203,
			"groupIds": [
				"7E6xlXYcXZCVLhBVKHuW8"
			],
			"roundness": null,
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"fontSize": 16,
			"fontFamily": 1,
			"text": "many to many, SQL\ngroup_id, user_id",
			"rawText": "many to many, SQL\ngroup_id, user_id",
			"baseline": 34,
			"textAlign": "left",
			"verticalAlign": "top",
			"containerId": null,
			"originalText": "many to many, SQL\ngroup_id, user_id"
		},
		{
			"type": "arrow",
			"version": 157,
			"versionNonce": 1302980627,
			"isDeleted": false,
			"id": "dIAoPsPSQCQCue3kCx9IW",
			"fillStyle": "hachure",
			"strokeWidth": 1,
			"strokeStyle": "solid",
			"roughness": 1,
			"opacity": 100,
			"angle": 0,
			"x": 550.727263001992,
			"y": 119.82854538719644,
			"strokeColor": "#000000",
			"backgroundColor": "transparent",
			"width": 103.8716003170839,
			"height": 0.8545900069033223,
			"seed": 277883069,
			"groupIds": [],
			"roundness": {
				"type": 2
			},
			"boundElements": [],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"startBinding": {
				"focus": -0.04125645141047466,
				"gap": 7.923324393535836,
				"elementId": "VNldjvRW0ZioF80N8jCSa"
			},
			"endBinding": {
				"focus": -0.0353203821219262,
				"gap": 10.064214974575705,
				"elementId": "KFIveaN30iNJc-7N5p035"
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
					103.8716003170839,
					0.8545900069033223
				]
			]
		},
		{
			"id": "KFIveaN30iNJc-7N5p035",
			"type": "ellipse",
			"x": 672.4909342838953,
			"y": 89.99111841976423,
			"width": 87,
			"height": 67,
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
			"seed": 331782525,
			"version": 103,
			"versionNonce": 676763293,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "9HDKXcNO"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"id": "9HDKXcNO",
			"type": "text",
			"x": 693.9909342838953,
			"y": 113.49111841976423,
			"width": 44,
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
			"seed": 1108369885,
			"version": 60,
			"versionNonce": 519663027,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "cache",
			"rawText": "cache",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "KFIveaN30iNJc-7N5p035",
			"originalText": "cache"
		},
		{
			"id": "WMjhkWSe_mYPutrlwO7FS",
			"type": "arrow",
			"x": 694.9809177471457,
			"y": 161.938820574507,
			"width": 52.71795532404553,
			"height": 52.32611333357974,
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
			"seed": 1174462205,
			"version": 43,
			"versionNonce": 2044967677,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-52.71795532404553,
					52.32611333357974
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"focus": -0.49379024761745904,
				"gap": 9.841079303991627,
				"elementId": "KFIveaN30iNJc-7N5p035"
			},
			"endBinding": {
				"focus": -0.2968142644116592,
				"gap": 12.420608432513674,
				"elementId": "YumMmuH3a-yWYF9jVaUbJ"
			},
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "-IfIgyQnRAUIpVRjO6bek",
			"type": "arrow",
			"x": -364.55539217324315,
			"y": 80.50926215895015,
			"width": 406.99015764180615,
			"height": 238.65323724387372,
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
			"seed": 966972061,
			"version": 225,
			"versionNonce": 2064470877,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "yttReUFY"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					183.47831444254882,
					178.2003140384595
				],
				[
					406.99015764180615,
					-60.45292320541421
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "dDXWqQCdh0gjOQcZQ4-xk",
				"focus": 0.21778868966486328,
				"gap": 6.514269442514006
			},
			"endBinding": {
				"elementId": "GTAPFCdYWjwseby8gFsgi",
				"focus": -0.7087532635038042,
				"gap": 9.78591885145039
			},
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "yttReUFY",
			"type": "text",
			"x": -276.5770777306943,
			"y": 228.70957619740966,
			"width": 191,
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
			"seed": 1727043933,
			"version": 76,
			"versionNonce": 95018227,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "on login:\nretrieve all messages\nmissed since last active",
			"rawText": "on login:\nretrieve all messages\nmissed since last active",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 54,
			"containerId": "-IfIgyQnRAUIpVRjO6bek",
			"originalText": "on login:\nretrieve all messages\nmissed since last active"
		},
		{
			"id": "WJLn027li1oCD6GbzopC5",
			"type": "ellipse",
			"x": 6.0276010453258095,
			"y": -472.4225910423803,
			"width": 87,
			"height": 67,
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
			"seed": 951763187,
			"version": 136,
			"versionNonce": 1747247037,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "WD3DsWST"
				},
				{
					"id": "dIAoPsPSQCQCue3kCx9IW",
					"type": "arrow"
				},
				{
					"id": "WMjhkWSe_mYPutrlwO7FS",
					"type": "arrow"
				},
				{
					"id": "rv7R1wWFBY5BqqnJ9m5m5",
					"type": "arrow"
				},
				{
					"id": "A-e8Ub1lPNF9Dry9sgPSn",
					"type": "arrow"
				},
				{
					"id": "QmQQjLRYqPVAkoeMz9GTU",
					"type": "arrow"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"id": "WD3DsWST",
			"type": "text",
			"x": 27.52760104532581,
			"y": -448.9225910423803,
			"width": 44,
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
			"seed": 1917022205,
			"version": 91,
			"versionNonce": 1088931475,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "cache",
			"rawText": "cache",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 14,
			"containerId": "WJLn027li1oCD6GbzopC5",
			"originalText": "cache"
		},
		{
			"id": "QmQQjLRYqPVAkoeMz9GTU",
			"type": "arrow",
			"x": 103.4116964653287,
			"y": -432.5351716251507,
			"width": 132.74766067394268,
			"height": 3.5677383833570957,
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
			"seed": 376855091,
			"version": 422,
			"versionNonce": 2001461277,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					132.74766067394268,
					-3.5677383833570957
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "WJLn027li1oCD6GbzopC5",
				"focus": 0.23111694379726977,
				"gap": 10.949219579289938
			},
			"endBinding": {
				"elementId": "RmZPM0tC44kJKMfc-CVFT",
				"focus": 0.26483739875003215,
				"gap": 8.093662142183675
			},
			"startArrowhead": "arrow",
			"endArrowhead": "arrow"
		},
		{
			"id": "nkopXWt9",
			"type": "text",
			"x": -479.23611873988114,
			"y": -451.3265687531707,
			"width": 339,
			"height": 35,
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
			"seed": 260469309,
			"version": 71,
			"versionNonce": 1542945843,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "WhatsApp System Design",
			"rawText": "WhatsApp System Design",
			"fontSize": 28,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 25,
			"containerId": null,
			"originalText": "WhatsApp System Design"
		},
		{
			"id": "hp7H5tZlKUmBNccUizwOC",
			"type": "rectangle",
			"x": 497.77027070233567,
			"y": 422.1271591937062,
			"width": 145,
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
			"seed": 1098034301,
			"version": 64,
			"versionNonce": 510907517,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "TJzPhGfn"
				},
				{
					"id": "agTtPjO94sMarRh-yfHb8",
					"type": "arrow"
				},
				{
					"id": "fwUOxu145714LxFOLTUP5",
					"type": "arrow"
				},
				{
					"id": "3WQTa9umTT6m-enZkT3cs",
					"type": "arrow"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"id": "TJzPhGfn",
			"type": "text",
			"x": 521.7702707023357,
			"y": 429.6271591937062,
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
			"seed": 1549960125,
			"version": 27,
			"versionNonce": 314539475,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "notification \nservice",
			"rawText": "notification service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 34,
			"containerId": "hp7H5tZlKUmBNccUizwOC",
			"originalText": "notification service"
		},
		{
			"id": "agTtPjO94sMarRh-yfHb8",
			"type": "arrow",
			"x": 175.63230293903212,
			"y": 175.81784969302942,
			"width": 387.5470889595488,
			"height": 234.53097289664822,
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
			"seed": 528804285,
			"version": 156,
			"versionNonce": 425606365,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					263.87498621045074,
					44.69819630751613
				],
				[
					387.5470889595488,
					234.53097289664822
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "BAlKrNNBGe7yWzqZDxfvL",
				"focus": -0.8323706867302146,
				"gap": 8.84744248514653
			},
			"endBinding": {
				"elementId": "hp7H5tZlKUmBNccUizwOC",
				"focus": 0.20458996093372014,
				"gap": 11.778336604028539
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "qTah6ztpW2pBd6ELy3ieH",
			"type": "rectangle",
			"x": 532.2743785072495,
			"y": 534.9388384525301,
			"width": 125,
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
				"type": 3
			},
			"seed": 1556494653,
			"version": 55,
			"versionNonce": 994877171,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "xDKvxxNj"
				},
				{
					"id": "fwUOxu145714LxFOLTUP5",
					"type": "arrow"
				}
			],
			"updated": 1674849263265,
			"link": null,
			"locked": false
		},
		{
			"id": "xDKvxxNj",
			"type": "text",
			"x": 546.2743785072495,
			"y": 539.9388384525301,
			"width": 97,
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
			"seed": 1367738781,
			"version": 56,
			"versionNonce": 798791997,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "iOS \nnotification \nservice",
			"rawText": "iOS notification service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 54,
			"containerId": "qTah6ztpW2pBd6ELy3ieH",
			"originalText": "iOS notification service"
		},
		{
			"id": "dASPNvn1lDDqEE8Tc6EJ9",
			"type": "rectangle",
			"x": 678.6356244954283,
			"y": 534.9388384525301,
			"width": 125,
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
				"type": 3
			},
			"seed": 546174419,
			"version": 91,
			"versionNonce": 982542749,
			"isDeleted": false,
			"boundElements": [
				{
					"type": "text",
					"id": "uodoWpVo"
				},
				{
					"id": "3WQTa9umTT6m-enZkT3cs",
					"type": "arrow"
				}
			],
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"id": "uodoWpVo",
			"type": "text",
			"x": 692.6356244954283,
			"y": 539.9388384525301,
			"width": 97,
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
			"seed": 92311069,
			"version": 132,
			"versionNonce": 1144670899,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"text": "SMS \nnotification \nservice",
			"rawText": "SMS notification service",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "center",
			"verticalAlign": "middle",
			"baseline": 54,
			"containerId": "dASPNvn1lDDqEE8Tc6EJ9",
			"originalText": "SMS notification service"
		},
		{
			"id": "fwUOxu145714LxFOLTUP5",
			"type": "arrow",
			"x": 574.8243714462592,
			"y": 484.9918480672717,
			"width": 10.906476724339427,
			"height": 37.62609299927021,
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
			"seed": 1454550291,
			"version": 29,
			"versionNonce": 1802186237,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					10.906476724339427,
					37.62609299927021
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "hp7H5tZlKUmBNccUizwOC",
				"focus": 0.07079388748198061,
				"gap": 7.8646888735655125
			},
			"endBinding": {
				"elementId": "qTah6ztpW2pBd6ELy3ieH",
				"focus": 0.06432804803898025,
				"gap": 12.320897385988246
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "3WQTa9umTT6m-enZkT3cs",
			"type": "arrow",
			"x": 651.0695725405888,
			"y": 459.39458919052265,
			"width": 93.35593600118318,
			"height": 67.45409686396101,
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
			"seed": 246626109,
			"version": 38,
			"versionNonce": 916749395,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					93.35593600118318,
					67.45409686396101
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "hp7H5tZlKUmBNccUizwOC",
				"focus": -0.6085509094898061,
				"gap": 8.299301838253086
			},
			"endBinding": {
				"elementId": "dASPNvn1lDDqEE8Tc6EJ9",
				"focus": 0.5672117449397657,
				"gap": 8.090152398046484
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "ceGBvfOU",
			"type": "text",
			"x": 541.8212226744442,
			"y": 617.422850046603,
			"width": 248,
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
			"seed": 1686584765,
			"version": 49,
			"versionNonce": 1886934717,
			"isDeleted": false,
			"boundElements": null,
			"updated": 1674849272575,
			"link": null,
			"locked": false,
			"text": "* these send notifications back\nto the client",
			"rawText": "* these send notifications back\nto the client",
			"fontSize": 16,
			"fontFamily": 1,
			"textAlign": "left",
			"verticalAlign": "top",
			"baseline": 34,
			"containerId": null,
			"originalText": "* these send notifications back\nto the client"
		},
		{
			"id": "VVgYNW5ZVZDfo3nacHEmA",
			"type": "arrow",
			"x": 709.3186872600859,
			"y": 174.6815946102405,
			"width": 54.680059523809405,
			"height": 50.438988095238074,
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
			"seed": 251201245,
			"version": 40,
			"versionNonce": 1401372499,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-54.680059523809405,
					50.438988095238074
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"focus": -0.49379024761745904,
				"gap": 9.841079303991627,
				"elementId": "WJLn027li1oCD6GbzopC5"
			},
			"endBinding": {
				"focus": -0.2968142644116592,
				"gap": 12.420608432513674,
				"elementId": "YumMmuH3a-yWYF9jVaUbJ"
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
		},
		{
			"id": "KevuDaBRjYW_k6fyU3m6u",
			"type": "rectangle",
			"x": 710.9008182280509,
			"y": 548.4029548983771,
			"width": 117.27174494682708,
			"height": 56.08031891807377,
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
			"seed": 1350918739,
			"version": 25,
			"versionNonce": 419587347,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674849247699,
			"link": null,
			"locked": false
		},
		{
			"id": "doIztjXdmwLOJ6M_dCzl3",
			"type": "arrow",
			"x": 598.890384355972,
			"y": 617.9515625946327,
			"width": 1041.8939690965565,
			"height": 563.8990597734929,
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
			"seed": 455906611,
			"version": 871,
			"versionNonce": 651837779,
			"isDeleted": true,
			"boundElements": null,
			"updated": 1674849263265,
			"link": null,
			"locked": false,
			"points": [
				[
					0,
					0
				],
				[
					-555.1079555431243,
					-27.29539813719498
				],
				[
					-1041.8939690965565,
					-563.8990597734929
				]
			],
			"lastCommittedPoint": null,
			"startBinding": {
				"elementId": "qTah6ztpW2pBd6ELy3ieH",
				"focus": -1.255747460388257,
				"gap": 13.01272414210257
			},
			"endBinding": {
				"elementId": "dDXWqQCdh0gjOQcZQ4-xk",
				"focus": 0.892356079625973,
				"gap": 9.85086922971368
			},
			"startArrowhead": null,
			"endArrowhead": "arrow"
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
		"scrollX": 1402.9280588315637,
		"scrollY": 731.0235551868285,
		"zoom": {
			"value": 0.78622695560454
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