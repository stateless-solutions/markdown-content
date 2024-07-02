---
section: "Developer Reference"
sortOrder: 3
label: "Viem"
pageName: "viem"
---

## Overview

The Stateless Viem SDK facilitates access to verifiable data from decentralized identities and blockchain networks. The custom library is designed to enhance decentralized application development by integrating a robust interface for interacting with various blockchain protocols through our specialized HTTP transport.

## Installation

To set up the Viem SDK in your project, follow these installation steps:

1. Open your terminal or command prompt
2. Navigate to the root directory of your project
3. Execute the following command to install the Viem SDK: `npm i viem-stateless`

## Initialization and Configuration

After installation, you must initialize and configure the SDK. First, import
the necessary components from the Viem SDK:

<br>

```
const { createPublicClient, http } = require('viem-stateless');
```

<br>

Define your HTTP transport configuration tailored to your security and data
integrity requirements:

<br>

```
const config = {
  minimumRequiredAttestations: 1,
  identities: ['https://api.stateless.solutions']
};
```

## Parameters

The `minimumRequiredAttestations` field represents how many matching responses
are needed to accept the result.

<br>

The `identities` field is the list of the known providers in your bucket. You
can see these corresponding identities of an existing bucket in the cli by
running either: `stateless-cli buckets list` or `stateless-cli buckets view`.

<br>

Next, initialize the client with the specific blockchain network and your HTTP
transport settings:

## Creating the Client

```
const client = createPublicClient({
  chain: 'mainnet',
  transport: http('your_bucket_url', config),
});
```

<br>

You can then continue using Viem as expected. For more information about usage,
please refer to the **[Viem documentation](https://viem.sh/docs/getting-started#2-consume-actions)**.



