---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

query_params = GetM365AppPlatformUserCountsWithPeriodRequestBuilder.GetM365AppPlatformUserCountsWithPeriodRequestBuilderGetQueryParameters(
		format = "text/csv",
)

request_configuration = GetM365AppPlatformUserCountsWithPeriodRequestBuilder.GetM365AppPlatformUserCountsWithPeriodRequestBuilderGetRequestConfiguration(
query_parameters = query_params,
)

await graph_client.reports.get_m365_app_platform_user_counts(period='{period}'.get(request_configuration = request_configuration)


```