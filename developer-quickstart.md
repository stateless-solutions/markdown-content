---
section: "Get Started"
sortOrder: 2
label: "Quickstart"
pageName: "quickstart"
---
**Alpha Access Disclaimer:** Thank you for your interest in Stateless! As we're
currently in our alpha phase, all new developer sign-ups are added to a
waitlist. Once your account is approved and you gain access, you'll be able to
utilize this guide. We appreciate your patience.

# Quickstart

This guide will walk you through the essentials of getting started with
Stateless, from account creation to sending an initial API request.

## Create an Account and API Key

Stateless offers a streamlined process for account creation. You can create an
account and log in using GitHub Single Sign-On (SSO). To create an account and generate an API key:

1. Visit [**app.stateless.solutions**](https://app.stateless.solutions)
2. Select "Sign Up" using GitHub SSO
3. Authorize Stateless to access your GitHub account
4. After successful authorization, you'll be logged into your Stateless account
5. Navigate to the ‘API Keys’ table on the ‘Account’ page
6. Click on 'Create API Key'
7. Label your key for easy identification
8. Save the generated key in a secure location

Having an account with Stateless is mandatory for sending requests. The account
allows you to manage billing, server resources, and more.

## Install Stateless

Stateless provides a full Python package for easy installation. To install the
Python package, run the following command in your terminal:
<br/><br/>

```bash
pip install stateless
```

## Configure a Provider Bucket

One of the key features of Stateless is the ability to select and manage the
blockchain nodes (providers) that service your requests. Here's how to set up
your bucket:
<br/><br/>
- List Providers: Check available providers using `offerings list`
- Build Bucket: Start adding providers to your bucket with `buckets create`

For a detailed guide on bucket management, read more [**here**](https://app.stateless.solutions/documentation/user-guides/developer-guides/selecting-service-providers).

## Send a Request

Now that you've set up your environment, you can use the Stateless API to make
your first request. Stateless provides the following supported blockchain
endpoints:
<br/><br/>
- Ethereum: [https://api.stateless.solutions/ethereum](https://app.stateless.solutions/ethereum)
- Optimism: [https://api.stateless.solutions/optimism](https://app.stateless.solutions/optimism)
- Arbitrum: [https://api.stateless.solutions/arbitrum](https://app.stateless.solutions/arbitrum)
- Polygon: [https://api.stateless.solutions/polygon](https://app.stateless.solutions/polygon)
- Binance: [https://api.stateless.solutions/binance](https://app.stateless.solutions/binance)

With any available endpoint, you can proceed to make a request. In this
example, you can quickly fetch the latest Ethereum block:
<br/><br/>
```bash
curl -X POST "https://api.stateless.solutions/eth/v1/<bucket_id>" -H "Content-Type: application/json" --data '{"jsonrpc":"2.0","method":"eth_blockNumber","id":1}'
```
<br/><br/>
After sending the request, you should receive a JSON response that contains the
latest Ethereum block number.
<br/><br/>
See the [**API Reference**](https://app.stateless.solutions/apireference) for more details.

## Next Steps

For a deeper dive into our offerings, tailored optimizations, provider bucket
management, and advanced use cases, please explore the Developer Guides for
comprehensive documentation designed to help you make the most of Stateless's
services.
