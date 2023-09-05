# Basic Concepts

## Secure API Services

API services in Stateless are specifically built to provide a safe and reliable data source for dApps. These services operate on a decentralized node network, adhering to our custom RPC modifications and offering signed attestations for every request they service.

Applications on Stateless build their custom buckets of providers to service their needs. This approach differs from conventional networks, where you have little to no control over what nodes are servicing your requests. By receiving data from multiple providers, applications on Stateless have a reliable source of truth that they control and can configure to their own tolerance thresholds.

## Blockchain Provider Buckets

In the Stateless middleware, a provider bucket refers to a personalized selection of blockchain nodes chosen by applications to service their requests. Unlike conventional networks where nodes are assigned randomly, provider buckets empower applications to customize their service network. Each bucket can contain multiple providers, selected based on factors like supported blockchains, regions, and latency performance.

When applications send requests, Stateless employs a smart routing system that directs the request to the nearest provider within the chosen bucket. This proximity-based routing minimizes latency, ensuring rapid response times and enhanced application performance.

By harnessing the potential of provider buckets, Stateless empowers applications to construct a custom network of service providers. This approach guarantees an optimized, reliable, and highly responsive environment for decentralized applications.
