# Selecting Service Providers

One of the unique attributes of the Stateless network protocol is the ability for applications to select and manage the blockchain nodes that service their requests. With Stateless, applications can tailor the services they receive to their specific needs, ensuring optimal performance and reliability. This guide provides detailed instructions on how applications can view provider offerings, build and manage "provider buckets," assign weights to providers, and configure multi-signature thresholds within their buckets.

## Provider Bucket Management

Provider buckets refer to a list of chosen blockchain nodes that applications can send requests to. Each bucket can contain multiple providers, the selection of which can be based on supported blockchains, regions, latency, and other factors.

When an application dispatches a request, it's not broadcasted arbitrarily. Instead, Stateless routes the request to the nearest provider present in the bucket. This proximity-based routing ensures minimal latency, enhancing the speed and responsiveness of the application.

Applications can construct these buckets via the Stateless CLI, using the following commands:

### Listing Providers

Applications can view a provider's offering name, supported blockchains, regions, and latency using the `provider list` command. This feature provides applications with the visibility they need to make informed decisions when selecting providers for their buckets. To display all providers on the Stateless network, use the following command:

```bash
stateless-cli provider list
```
This command displays the provider's offering name, supported blockchains, regions, and latency, helping applications make informed decisions when selecting providers for their buckets.

To display all providers in a specific bucket, use the following command:

```bash
stateless-cli bucket list
```
This command provides applications with a clear view of their current selection of service providers. It is especially useful when updating or modifying the list of providers in a bucket.

### Adding Providers

To add providers to a bucket, use the `add bucket` command. This command displays an interactive list of providers, allowing a fine-tuned selection of blockchain nodes.

```bash
stateless-cli add bucket
```
### Updating Providers

To update the list of providers in a bucket, use the `bucket update` command.

```bash
stateless-cli bucket update
```

### Deleting Providers

To remove a provider from the bucket, use the `bucket delete` command.

```bash
stateless-cli bucket delete
```

For more information about managing provider buckets via the API, please see the [API reference](https://app.stateless.solutions/api-reference)

