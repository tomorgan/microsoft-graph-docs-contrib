---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = RetentionEvent(
	odata_type = "#microsoft.graph.security.retentionEvent",
	display_name = "String",
	description = "String",
	event_trigger_date_time = "String (timestamp)",
	additional_data = {
			"event_query" : [
				(
					odata_type = "microsoft.graph.security.eventQuery",
				),
			]
			"retention_event_type@odata_bind" : "https://graph.microsoft.com/v1.0/security/triggerTypes/retentionEventType/9eecef97-fb3c-4c68-825b-4dd74530863a",
	}
)

result = await graph_client.security.triggers.retention_events.post(body = request_body)


```