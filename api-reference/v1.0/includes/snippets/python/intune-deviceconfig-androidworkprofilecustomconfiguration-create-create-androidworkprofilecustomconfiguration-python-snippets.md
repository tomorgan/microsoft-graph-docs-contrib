---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = AndroidWorkProfileCustomConfiguration(
	odata_type = "#microsoft.graph.androidWorkProfileCustomConfiguration",
	description = "Description value",
	display_name = "Display Name value",
	version = 7,
	oma_settings = [
		OmaSetting(
			odata_type = "microsoft.graph.omaSetting",
			display_name = "Display Name value",
			description = "Description value",
			oma_uri = "Oma Uri value",
		),
	]
)

result = await graph_client.device_management.device_configurations.post(body = request_body)


```