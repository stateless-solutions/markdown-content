---
section: "Get Started"
sortOrder: 2
label: "Quickstart"
pageName: "quickstart"
---
**Beta Access Disclaimer:** Thank you for exploring our beta release! Should you experience any service disruptions or have insights to share, reach out at support@stateless.solutions.

# Quickstart

This guide will walk you through the essentials of getting started with
Stateless, from account creation to sending an initial API request.

For convenience, Stateless provides the following public endpoints:
<br/><br/>
**Active**
- Ethereum: [https://api.stateless.solutions/ethereum/v1/e9a59fdc-cae3-4682-a474-8afbd7d96bf5](https://api.stateless.solutions/ethereum/v1/e9a59fdc-cae3-4682-a474-8afbd7d96bf5)
- Polygon: [https://api.stateless.solutions/polygon/v1/cfa75b32-9418-42de-ae32-bb567b5522cc](https://api.stateless.solutions/polygon/v1/cfa75b32-9418-42de-ae32-bb567b5522cc)
- Optimism: [https://api.stateless.solutions/optimism/v1/f373feb1-c8e4-41c9-bb74-2c691988dd34](https://api.stateless.solutions/optimism/v1/f373feb1-c8e4-41c9-bb74-2c691988dd34)
- Arbitrum: [https://api.stateless.solutions/arbitrum-one/v1/2f299b0a-5e3e-4c22-bc6b-04b13e5b8c26](https://api.stateless.solutions/arbitrum-one/v1/2f299b0a-5e3e-4c22-bc6b-04b13e5b8c26)
<br>

## Create an Account and API Key

Stateless offers a streamlined process for account creation. You can create an
account and log in using GitHub Single Sign-On (SSO). To create an account and generate an API key:

1. Visit [**app.stateless.solutions**](https://app.stateless.solutions)
2. Select "Sign Up" using GitHub SSO
3. Authorize Stateless to access your GitHub account
4. After successful authorization, you'll be logged into your Stateless account
5. Navigate to the ‘API Keys’ table on the ‘Account’ page
6. Click on 'Create API Key'
7. Label your key for easy identification and set an expiration date
8. Save the generated key in a secure location as it will not be displayed after creation

Having an account with Stateless is mandatory for sending requests. The account
allows you to manage billing, server resources, and more.

## Install Stateless

Stateless provides a full Python package for easy installation. Please make sure you have Python 3.10 or later and pip before proceeding. To install the Python package, run the following command in your terminal:

<br/>
```bash
pip install stateless-sdk
```
<br/>
## Select Providers
One of the key features of Stateless is the ability to select and manage the blockchain nodes (Providers) that service your requests. Using the CLI, run the create bucket command:

<br/>
```bash
stateless-cli buckets create
```
<br/>

Follow the interactive prompts to enter a name for your bucket and select the blockchain and Provider Offerings to send your requests to. For a detailed guide on bucket management, see [**Selecting Service Providers**](https://app.stateless.solutions/documentation/selecting-service-providers).

## Send a Request

Now that you've set up your environment and built your Provider bucket, you can use the Stateless API to make
your first request. 

With any available endpoint, you can proceed to make a request. In this
example, you can quickly fetch the latest Ethereum block:
<br/><br/>
```bash
curl -X POST "https://api.stateless.solutions/eth/v1/<bucket_id>" -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"eth_blockNumber","id":1}'
```
<br/><br/>
After sending the request, you should receive a JSON response that contains the
latest Ethereum block number. See the [**API Reference**](https://app.stateless.solutions/apireference) for more details.

## Next Steps
Currently, public endpoints are assigned a bucket with 1-2 independent providers. For a detailed guide on bucket management, read more [**here**](https://app.stateless.solutions/documentation/user-guides/developer-guides/selecting-service-providers). For a deeper dive into our offerings, tailored optimizations, provider bucket
management, and advanced use cases, please explore the Developer Guides.
