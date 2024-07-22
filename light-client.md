---
section: "Get Started"
sortOrder: 3
label: "Consumable Light Client"
pageName: "light-client"
---
# Consumable Light Client

## Overview

Traditionally, light clients have been inaccessible to consumers. While
[**EIP-1186**](https://eips.ethereum.org/EIPS/eip-1186) allows end users to
receive Merkle Proofs from an Ethereum node, it requires reliance on a trusted
state root hash. Stateless APIs, however, provide a method to deliver a
verified state root hash to the end user, eliminating the need for trust.

By combining a verified state root hash with an independent proof provider,
developers can continue using their existing frameworks to consume data from
the Ethereum blockchain without the current trust assumptions.

<br>

This combination of a verified state root hash and an independent proof provider
allows for developers wishing to consume data from the Ethereum blockchain to
continue doing so via their existing frameworks, while eliminating the trust
assumptions that currently come with it.

## Usage

Regardless if you want to bring your own proofs or use the Stateless network
you'll need to create a verified API bucket.

<br>

Using the light client approach is nearly identical to consuming the current
verified APIs via a bucket as described in the Quickstart section. The same
initial steps of creating a bucket still apply.

<br>

What needs to be considered when consuming proofs directly through the
Stateless API, is that the providers in the bucket should be different from the
provider acting as your proof provider.

<br>

If you haven't created a bucket, the first step is following the
**[Quickstart](https://app.stateless.solutions/documentation/quickstart)** to
create your initial bucket, which can have between 1 and 3 providers, take note
of which ones.

<br>

If you already have created a bucket, simply run `stateless-cli buckets list`
to take note of which providers are already in your bucket.


## Using Stateless as your Proof Provider

Once you've done that, you'll want to create a second bucket with a single
provider that isn't in already in your existing bucket, this is your Proof
Provider.

<br>

This bucket URL is your `proverUrl`.

## Bring your Own Proof Provider

Otherwise, you're free to bring any RPC resource that offers `eth_getProof`.
Some examples of this include:

<br>

1. A node from another commercial node provider, **[Infura](https://www.infura.io/)**, **[Alchemy](https://www.alchemy.com)**, etc.
2. An RPC resource from an indexer layer, **[Laconic's ipld-eth-server](https://github.com/cerc-io/ipld-eth-server)**, **[Subsquid's RPC Proxy](https://docs.subsquid.io/cloud/resources/rpc-proxy/)**, etc.

This RPC URL is your `proverUrl`

## Connecting it to Ethers

Once you have this `proverUrl` either from Stateless or your own source,
using Ethers works identical to the proof source, just with this additional
`proverUrl` parameter in the initialization:

<br>

```js
const { ethers } = require("ethers-stateless");

const provider = new ethers.StatelessProvider(
    "your_bucket_url",
    ['https://api.stateless.solutions'],
    1,
    "your_proverUrl"']);
```

<br>

See the **[Ethers guide](https://app.stateless.solutions/documentation/ethers)** for more information about the other parameters.
