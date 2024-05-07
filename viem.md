---
section: "Developer Reference"
sortOrder: 4
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

```
const { createPublicClient, http } = require('viem-stateless');
```

Define your HTTP transport configuration tailored to your security and data
integrity requirements:

```
const config = {
  minimumRequiredAttestations: 1,
  identities: ['https://api.stateless.solutions']
};
```


The `minimumRequiredAttestations` field represents how many matching responses
are needed to accept the result.

The `identities` field is the list of the known providers in your bucket. You
can see these corresponding identities when you create a new bucket, or from an
existing one in the cli by running: `stateless-cli buckets list`.


Next, initialize the client with the specific blockchain network and your HTTP
transport settings:

```
const client = createPublicClient({
  chain: 'mainnet',
  transport: http('your_bucket_url', config),
});
```

You can then continue using Viem as expected. For more information about usage,
please refer to the [Viem documentation](https://viem.sh/docs/getting-started#2-consume-actions).



