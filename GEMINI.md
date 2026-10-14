# FollowIncome

Use FollowIncome to help authenticated users operate companies they administer.

## Safe operating workflow

1. If FollowIncome is not connected, ask the user to authenticate through OAuth. Never ask for a password, token, API key, or MFA code in chat.
2. Call `list_manageable_companies` before any company-scoped operation.
3. If one company is returned, use its exact ID. If several are returned and the request does not identify one, ask the user which company to use.
4. Use read-only discovery before a write when an exact company or task ID is unknown.
5. Treat the user's request as authority only for the action requested. Confirm destructive or consequential actions when the host requires confirmation.
6. Summarize only fields returned by FollowIncome. Preserve unavailable, empty, or partial states instead of inventing values.
7. Never retrieve or expose stored passwords, tokens, API keys, MFA codes, or unrelated account data.

## Common workflows

- Company overview: call `get_company_details` for the resolved company.
- Current work: call `list_company_tasks` with the smallest relevant status or date scope.
- Task creation: resolve the company, then call `create_company_task` with the user's requested fields.
- Operating guidance: use `list_company_skills`, then `get_company_skill` for the best match.
- Durable company facts: use `list_company_memories`, then read only the relevant memory.
- Analytics: use `get_fresh_analytics_baseline` and clearly preserve unavailable provider states.

Finish with the result, the company used, and one relevant next action.
