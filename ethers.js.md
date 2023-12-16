---
section: "Developer Reference"
sortOrder: 3
label: "JavaScript SDK"
pageName: "javascript-sdk"
---

# Stateless Ethers.js SDK Reference

## Overview
The Stateless SDK enhances Ethereum-based application development by providing a specialized interface for Ethers.js library integration. It enables direct interaction with Stateless HTTP API endpoints, facilitating efficient blockchain data access and transaction execution.

## Installation
To install the Stateless SDK for use with Ethers.js, follow these steps:

1. Open your terminal or command prompt.
2. Navigate to the root directory of your project.
3. Run the following command to install the Stateless version of the Ethers library:
   ```bash npm install ethers-stateless@6.8.1-stateless```

This command will add the necessary Stateless Ethers.js SDK files to your project.

## Initialization and Configuration

After installing the SDK, you need to initialize and configure it within your Ethers.js environment. Here's how:

1. Import the ethers object from the ethers-stateless package: ```bash const { ethers } = require("ethers-stateless");```
2. Initialize the StatelessProvider with your specific endpoint URL: ```bash const provider = new ethers.StatelessProvider("your_bucket_url");```
3. Replace "your_bucket_url" with the actual URL provided for your Stateless bucket.

## Basic Usage Examples

With the Stateless SDK set up, you can start using it for typical Ethereum operations. Here are a few basic examples:
<br>
**Retrieving the Current Block Number**

To get the current block number from the Ethereum blockchain:
<br>
```bash
provider.getBlockNumber()
  .then(blockNumber => console.log(`Current block number: ${blockNumber}`))
  .catch(error => console.error(error));
```
<br>
**Getting an Account's Balance**

To check the balance of a specific Ethereum account:
<br>
```bash
const address = '0xYourEthereumAddress'; // Replace with the actual Ethereum address
provider.getBalance(address)
  .then(balance => console.log(`Balance for ${address}: ${balance}`))
  .catch(error => console.error(error));
```
<br>
Remember to replace '0xYourEthereumAddress' with the Ethereum address whose balance you wish to check.
<br>
