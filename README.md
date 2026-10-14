# FollowIncome for Gemini CLI

<p align="center">
  <img src="assets/followincome-mark.png" alt="FollowIncome" width="128" height="128">
</p>

Use FollowIncome from Gemini CLI to manage company operations, tasks, business context, analytics, pricing, memories, and runbooks.

## Install

```bash
gemini extensions install https://github.com/newcoolstudioteam/followincome-gemini-extension
```

Restart Gemini CLI after installation, then authenticate the connector:

```text
/mcp auth followincome
```

Verify that the server is connected:

```text
/mcp list
```

## Example prompts

- What companies can I manage in FollowIncome?
- Summarize my company profile, current priorities, and TODO tasks.
- Create a task for my company, set a due date, and add tags.

## Access and privacy

FollowIncome uses OAuth. Users can access only companies their signed-in account administers. The extension does not contain credentials, API keys, or client secrets.

- Website: https://followincome.com
- Support: https://followincome.com/contact
- Privacy policy: https://followincome.com/privacy
- Terms of service: https://followincome.com/terms

## MCP endpoint

`https://followincome.com/mcp/`
