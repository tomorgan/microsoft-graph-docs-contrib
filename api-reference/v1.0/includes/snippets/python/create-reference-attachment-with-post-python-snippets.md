---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = ReplyPostRequestBody(
	post = Post(
		body = ItemBody(
			content_type = BodyType.Text,
			content = "I attached a reference to a file on OneDrive.",
		),
		attachments = [
			ReferenceAttachment(
				odata_type = "#microsoft.graph.referenceAttachment",
				name = "Personal pictures",
				additional_data = {
						"source_url" : "https://contoso.com/personal/mario_contoso_net/Documents/Pics",
						"provider_type" : "oneDriveConsumer",
						"permission" : "Edit",
						"is_folder" : "True",
				}
			),
		]
	),
)

await graph_client.groups.by_group_id('group-id').threads.by_thread_id('conversationThread-id').reply.post(body = request_body)


```