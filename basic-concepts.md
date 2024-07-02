---
section: "Get Started"
sortOrder: 2
label: "Basic Concepts"
pageName: "basic-concepts"
---
# Basic Concepts

## Verifiable APIs

Stateless's APIs are built to provide safe and reliable decentralized data
sources for developers. Operating across a distributed node network, the
Stateless protocol enables efficient client-side verification, whether
historically or in real-time.

<br/><br/>

## Data Provider Buckets

A provider bucket refers to a personalized selection of blockchain nodes chosen
by developers to service their requests.  Unlike conventional networks where
nodes are assigned randomly, provider buckets empower developers to customize
their service network. Each bucket can contain multiple providers, selected
based on factors like supported blockchains, regions, and latency performance.

<br/><br/>

When developers send requests, Stateless employs a routing system that directs
the request to the nearest provider within the chosen bucket. By creating
custom service networks, developers can receive data from 1-many providers for
reliable sources of truth that can be configured to their own requirements.

<br/><br/>

## Consumable Light Client

A consumable light client is an approach for allowing developers to deliver
proofs of the underlying RPC data directly to end users. This approach relies
on two key components, a Data Provider Bucket, and a Proof Provider.

The Proof Provider is any Ethereum resource that provides access to the
`eth_getProof` method. This can be a traditional node, or an indexer that
exposes the same data.

The Data Provider Bucket provides a verified state root hash. This state root
hash allows for verifying the underlying proof for a corresponding `eth_call`.
