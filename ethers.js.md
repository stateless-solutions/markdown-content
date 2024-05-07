---
section: "Developer Reference"
sortOrder: 3
label: "Ethers"
pageName: "ethers"
---

## Overview
Stateless enhances Ethereum-based application development by providing a specialized interface for Ethers.js library integrations. It enables direct interaction with Stateless HTTP API endpoints, facilitating efficient access to verified data and transaction execution. You can see the SDK code in full [**here**](https://github.com/stateless-solutions/ethers.js).

## Installation
To install the Stateless SDK for use with Ethers.js, follow these steps:

1. Open your terminal or command prompt.
2. Navigate to the root directory of your project.
3. Run the following command to install the Stateless version of the Ethers library:
   ```npm install ethers-stateless@6.8.1-stateless-2```

This command will add the necessary Stateless Ethers.js SDK files to your project.

## Initialization and Configuration

After installing the SDK, you need to initialize and configure it within your Ethers.js environment. Here's how:

1. Import the ethers object from the ethers-stateless package: ```const { ethers } = require("ethers-stateless");```
2. Initialize the StatelessProvider with your specific endpoint URL: ```const provider = new ethers.StatelessProvider("your_bucket_url");```
3. Replace "your_bucket_url" with the actual URL provided for your Stateless bucket.

You can then continue using Ethers as expected. For more information about usage, please refer to the [**Ethers documentation**](https://docs.ethers.org/v5/).  
