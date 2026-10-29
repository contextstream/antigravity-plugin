# ContextStream for Antigravity

Persistent memory for your Antigravity sessions: decisions, lessons, plans and
indexed code search from [ContextStream](https://contextstream.io), through the
hosted MCP server at `https://mcp.contextstream.io/mcp`.

## Install

```sh
agy plugin install https://github.com/contextstream/antigravity-plugin
```

The plugin stays off until you give it your ContextStream API key. Open
`/plugin` in Antigravity, turn **contextstream** on and enter the key. Create
one at <https://contextstream.io/account/api-keys>.

## What it holds

| File | What it does |
| --- | --- |
| `rules/AGENTS.md` | Compact always-on rules: ground each request with `context`, search ContextStream before `grep_search` and `find_by_name`, and save decisions and lessons |
| `skills/contextstream/` | The full reference, loaded only when the agent asks for it |
| `mcp_config.json` | The hosted ContextStream server; your API key is asked for when you turn the plugin on |
| `hooks.json` | Reminders to call `init` and `context`, and to search ContextStream first |

## The hooks need `contextstream-mcp`

The hooks run the local `contextstream-mcp` binary. Everything else works
without it: with no binary on your `PATH` the hooks do nothing and print
nothing. To add it, run `npx -y @contextstream/mcp-server setup`, which also
signs the binary in. The hooks use a POSIX shell; on Windows run `setup`, which
writes hooks for Windows.

If you already ran `contextstream-mcp setup` for Antigravity, you have this
plugin and don't need to install it again.

## Privacy

What ContextStream collects, and how to turn each part off, is in
[docs/data-handling.md](https://github.com/contextstream/mcp-server/blob/main/docs/data-handling.md).
Hooks and indexing send nothing until `contextstream-mcp` is set up and signed in.

## Where this comes from

This repository is generated from
[contextstream/mcp-server](https://github.com/contextstream/mcp-server) by the
same code `setup` uses to write the plugin on your machine, so the two do not
drift. Please don't edit files here; open issues and pull requests on
`mcp-server`.
