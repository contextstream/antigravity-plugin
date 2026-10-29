---
name: contextstream
description: >-
  Full ContextStream reference: every tool and action, the notices
  context() returns, plans, tasks, lessons, decisions, docs, handoffs,
  past sessions and code search. Use it when a ContextStream call or
  notice needs more detail than the plugin rules give.
---
<!-- contextstream-managed: antigravity skill -->

# ContextStream reference

In Antigravity, make each ContextStream call with `call_mcp_tool`: `ServerName` "contextstream", `ToolName` the tool, `Arguments` its parameters. For example, `search(mode="auto", query="...")` is `call_mcp_tool(ServerName="contextstream", ToolName="search", Arguments={"mode": "auto", "query": "..."})`.

The complete reference is [references/reference.md](references/reference.md) in this skill's folder. Open it with `view_file` and read the section you need:
- Core ContextStream Workflow (harness_teaching_v4)
- Canonical Agent Handoffs
- Why These Rules?
- Finding Information — Search ContextStream Knowledge, Not Just Code
- Past Sessions Are Queryable — USE THEM
- Project Scope Discipline
- Code Health and Dependency Recommendations
- Response to Notices
- System Reminders
- Search Protocol
- Plans and Tasks
- Memory, Docs & Todos
- Skills (IMPORTANT — Do Not Ignore Matched Skills)
- Code Search
- Context Pressure
