---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = WindowsPhone81CompliancePolicy(
	odata_type = "#microsoft.graph.windowsPhone81CompliancePolicy",
	description = "Description value",
	display_name = "Display Name value",
	version = 7,
	password_block_simple = True,
	password_expiration_days = 6,
	password_minimum_length = 5,
	password_minutes_of_inactivity_before_lock = 5,
	password_minimum_character_set_count = 0,
	password_required_type = RequiredPasswordType.Alphanumeric,
	password_previous_password_block_count = 2,
	password_required = True,
	os_minimum_version = "Os Minimum Version value",
	os_maximum_version = "Os Maximum Version value",
	storage_require_encryption = True,
)

result = await graph_client.device_management.device_compliance_policies.post(body = request_body)


```