---
description: "Automatically generated file. DO NOT MODIFY"
---

```python

# THE PYTHON SDK IS IN PREVIEW. FOR NON-PRODUCTION USE ONLY

graph_client = GraphServiceClient(request_adapter)

request_body = CreateNewVersionPostRequestBody(
	workflow = Workflow(
		category = LifecycleWorkflowCategory.Joiner,
		description = "Configure new hire tasks for onboarding employees on their first day",
		display_name = "Global onboard new hire employee",
		is_enabled = True,
		is_scheduling_enabled = False,
		execution_conditions = TriggerAndScopeBasedConditions(
			odata_type = "#microsoft.graph.identityGovernance.triggerAndScopeBasedConditions",
			scope = RuleBasedSubjectSet(
				odata_type = "#microsoft.graph.identityGovernance.ruleBasedSubjectSet",
				rule = "(department eq 'Marketing')",
			),
			trigger = TimeBasedAttributeTrigger(
				odata_type = "#microsoft.graph.identityGovernance.timeBasedAttributeTrigger",
				time_based_attribute = WorkflowTriggerTimeBasedAttribute.EmployeeHireDate,
				offset_in_days = 1,
			),
		),
		tasks = [
			Task(
				continue_on_error = False,
				description = "Enable user account in the directory",
				display_name = "Enable User Account",
				is_enabled = True,
				task_definition_id = "6fc52c9d-398b-4305-9763-15f42c1676fc",
				arguments = [
				]
			),
			Task(
				continue_on_error = False,
				description = "Send welcome email to new hire",
				display_name = "Send Welcome Email",
				is_enabled = True,
				task_definition_id = "70b29d51-b59a-4773-9280-8841dfd3f2ea",
				arguments = [
				]
			),
		]
	),
)

result = await graph_client.identity_governance.lifecycle_workflows.workflows.by_workflow_id('workflow-id').microsoft_graph_identity_governance_create_new_version.post(body = request_body)


```