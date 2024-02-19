---
title: "data encoding"
created_at: 2024-01-26
type: concept
aliases: 
parents: 
children: 
supports: 
enemies:
---

At its most basic, encoding is the act of moving in-memory data to the disk or to send on the network. Conversely, decoding is moving data in a disk or from a network to in-memory data.

Encoding formats can be split into two broad categories.

## human-readable formats

Human-readable formats of encoding tend to be popular as they can be understood without needing an decoding schema. The main formats in this format are:

1. **JSON**
	- No strict schema, so it’s flexible. Schema validation needs to be agreed upon outside of a strict schema.
	- Widely supported in the web browser space.
2. **XML**
	- Not very popular in newer technologies anymore.
	- Not binary encoded, but still hard to read due to verbosity.

## binary formats

Binary formats are not readable without an encoding schema, but are able to compress data more. As such, they are more useful for company-internal usecases.

Major technologies in this space include Thrift, Protocol Buffers, and Avro.

### protocol buffers (protobufs)

- developed by google
- TODO: ddia pdf page 142

### thrift

- developed by facebook
- binary encoding that requires an explicit schema to encode/decode
- TODO: ddia pdf page 139

### avro

- writer schema and reader schema
- TODO: ddia pdf page 144

## importance of evolvability

Business requirements and logic are always changing, and a change to business requirements typically requires schema changes.

Schema changes across a large distributed system without downtime requires **rolling changes**, meaning that machines may be running different versions of schemas/code at the same time.

Because of this, when considering encoding formats, we need to ensure that our encoding/decoding is evolvable, meaning that it’s backward and forward compatible in the face of schema changes.
