---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = MessagesRequestBuilder.MessagesRequestBuilderGetQueryParameters(
		filter = "subject eq 'let''s meet for lunch?'",
)

request_configuration = MessagesRequestBuilder.MessagesRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

result = await graph_client.me.messages.get(request_configuration = request_configuration)


```