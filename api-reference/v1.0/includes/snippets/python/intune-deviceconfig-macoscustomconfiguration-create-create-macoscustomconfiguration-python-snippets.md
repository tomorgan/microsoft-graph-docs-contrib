---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = MacOSCustomConfiguration(
	odata_type = "#microsoft.graph.macOSCustomConfiguration",
	description = "Description value",
	display_name = "Display Name value",
	version = 7,
	payload_name = "Payload Name value",
	payload_file_name = "Payload File Name value",
	payload = base64.urlsafe_b64decode("cGF5bG9hZA=="),
)

result = await graph_client.device_management.device_configurations.post(body = request_body)


```