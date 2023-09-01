# Selecting Service Providers

One of the unique attributes of the Stateless network protocol is the ability for applications to select and manage the blockchain nodes that service their requests. With Stateless, applications can tailor the services they receive to their specific needs, ensuring optimal performance and reliability. This guide provides detailed instructions on how applications can view provider offerings, build and manage "provider buckets," assign weights to providers, and configure multi-signature thresholds within their buckets.

## Provider Bucket Management

Provider buckets refer to a list of chosen blockchain nodes that applications can send requests to. Each bucket can contain multiple providers, the selection of which can be based on supported blockchains, regions, latency, and other factors.

When an application dispatches a request, it's not broadcasted arbitrarily. Instead, Stateless routes the request to the nearest provider present in the bucket. This proximity-based routing ensures minimal latency, enhancing the speed and responsiveness of the application.

Applications can construct these buckets via the Stateless CLI, using the following commands:

### Viewing and Adding New Providers

To view and add providers to a bucket, use the `create bucket` command. 

```bash
buckets create
```
This command displays an interactive list of providers, allowing a fine-tuned selection of blockchain nodes. The provider's ID, name, and supported blockchains will be displayed to help applications make informed decisions when selecting providers to service their requests.

For additional details about a providers services, you can view all availale offerings:

```bash
offerings list
```
This command will return additional details such as a providers available regions and average latency by chain.

### Updating Existing Providers

Applications can view their current active providers in a specific bucket using the following command:

```bash
buckets list
```
To update the list of providers in a bucket, use the `bucket update` command.

```bash
buckets update
```

### Deleting Providers

To remove a provider from the bucket, use the `bucket delete` command.

```bash
buckets delete
```

For more information about managing providers via the API, please see the [API reference](https://app.stateless.solutions/api-reference)
