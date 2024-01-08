---
section: "Developer Guides"
sortOrder: 2
label: "Selecting Service Providers"
pageName: "selecting-service-providers"
---
# Selecting Service Providers

The Stateless protocol offers developers the unique ability to select and manage blockchain nodes that service their requests. This capability allows for tailoring services to specific needs, ensuring optimal performance and reliability.

## Provider Bucket Management

Provider buckets refer to a list of chosen blockchain nodes that application
can send requests to. Each bucket can contain multiple providers, the selection
of which can be based on supported blockchains, regions, latency, and other
factors.
<br/><br/>
When an application dispatches a request, it's not broadcasted arbitrarily.
Instead, Stateless routes the request to the nearest provider present in the
bucket. This proximity-based routing ensures minimal latency, enhancing the
speed and responsiveness of the application.
<br/><br/>
Application developers can construct these buckets via the Stateless CLI, using
the following commands: 
<br/><br/>
**Viewing and Adding New Providers**
<br/><br/>
To view and add providers to a bucket, use the `create bucket` command.  
<br/><br/>
```bash
stateless-cli buckets create
```
<br/><br/>
This command displays an interactive list of providers, allowing a fine-tuned
selection of blockchain nodes. The provider's ID, name, and supported
blockchains will be displayed to help developers make informed decisions when
selecting providers to service their requests.  
<br/><br/>
For additional details about a providers services, you can view all available
offerings: 
<br/><br/>
```bash
stateless-cli offerings list
```
<br/><br/> 
This command will return additional details such as a providers available
regions and average latency by chain. 
<br/><br/>
**Updating Existing Providers**  
<br/><br/>
Developers can view their current active providers in a specific bucket using
the following command
<br/><br/>
```bash
stateless-cli buckets list
```
<br/><br/>
To update the list of providers in a bucket, use the `bucket update` command.
<br/><br/>
```bash
stateless-cli buckets update
```
<br/><br/>
**Deleting Providers**
<br/><br/>
To remove a provider from the bucket, use the `bucket delete` command.&nbsp; 
<br/><br/>
```bash
stateless-cli buckets delete
```
<br/><br/>
For more information about managing providers via the API, please see the [**API reference**](https://app.stateless.solutions/api-reference)
