---
section: "Developer Guides"
sortOrder: 2
label: "Selecting Service Providers"
pageName: "selecting-service-providers"
---
# Selecting Service Providers

One of the unique attributes of the Stateless protocol is the ability for
developers to select and manage the blockchain nodes that service their
requests. With Stateless, developers can tailor the services they receive to
their specific needs, ensuring optimal performance and reliability.&nbsp;   

This guide provides detailed instructions on how developers can view provider offerings,
build and manage "provider buckets," assign weights to providers, and configure
multi-signature thresholds within their buckets.

## Provider Bucket Management

Provider buckets refer to a list of chosen blockchain nodes that application
can send requests to. Each bucket can contain multiple providers, the selection
of which can be based on supported blockchains, regions, latency, and other
factors.&nbsp;  

When an application dispatches a request, it's not broadcasted arbitrarily.
Instead, Stateless routes the request to the nearest provider present in the
bucket. This proximity-based routing ensures minimal latency, enhancing the
speed and responsiveness of the application.&nbsp;  

Application developers can construct these buckets via the Stateless CLI, using
the following commands:&nbsp;  

### Viewing and Adding New Providers
&nbsp; 
To view and add providers to a bucket, use the `create bucket` command.&nbsp;  

```bash
buckets create
```
&nbsp;  
This command displays an interactive list of providers, allowing a fine-tuned
selection of blockchain nodes. The provider's ID, name, and supported
blockchains will be displayed to help developers make informed decisions when
selecting providers to service their requests.&nbsp;  

For additional details about a providers services, you can view all available
offerings:&nbsp; 

```bash
offerings list
```
&nbsp; 
This command will return additional details such as a providers available
regions and average latency by chain.&nbsp; 

### Updating Existing Providers
&nbsp; 
Developers can view their current active providers in a specific bucket using
the following command:&nbsp; 

```bash
buckets list
```
&nbsp; 
To update the list of providers in a bucket, use the `bucket update` command.&nbsp; 

```bash
buckets update
```
&nbsp; 
### Deleting Providers
&nbsp; 
To remove a provider from the bucket, use the `bucket delete` command.&nbsp; 

```bash
buckets delete
```
&nbsp; 
For more information about managing providers via the API, please see the [API reference](https://app.stateless.solutions/api-reference)
