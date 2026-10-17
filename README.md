# OpenSeason for Cursor

Connect [OpenSeason](https://openseason.life) to Cursor through the Model Context Protocol (MCP). Manage Focus, things, checklists and your life tree from your editor after a one-time OAuth sign-in.

Not on OpenSeason yet? Try the [Free renewals tool](https://openseason.life/for/renewals?utm_source=github&utm_medium=readme&utm_campaign=owned-links): list your subscriptions and see what renews in the next 30 and 90 days, plus your yearly total. No signup.

## What you get

- Remote MCP endpoint at `https://openseason.life/api/mcp`
- OAuth against OpenSeason (client id `cursor-mcp`)
- Tools to read and update your household data in OpenSeason

Your SaaS data stays on OpenSeason. This plugin only ships the Cursor manifest and MCP connection config.

## Install

### Cursor Marketplace (pending)

Once listed, install **OpenSeason** from the Cursor Marketplace. Cursor will prompt you to sign in to OpenSeason and grant access.

### Local install (smoke / pre-Marketplace)

1. Clone this repo (or copy its contents) into your local plugins folder:

   ```bash
   mkdir -p ~/.cursor/plugins/local
   git clone https://github.com/dbenzel/openseason-cursor.git ~/.cursor/plugins/local/openseason-cursor
   ```

2. Restart Cursor (or reload the window) so it picks up the local plugin.
3. When prompted, complete OAuth at [openseason.life](https://openseason.life).

## Permissions (OAuth scopes)

In plain language, the connection asks for:

| Scope | Meaning |
| --- | --- |
| `mcp:tools` | Use OpenSeason MCP tools from Cursor |
| `os:read` | Read your OpenSeason data (Focus, things, checklists and related) |
| `os:write` | Create and update that data on your behalf |

You can disconnect Cursor anytime in OpenSeason under [Settings, Connected apps](https://openseason.life/app/settings#connected-apps). Disconnecting revokes its access and refresh tokens immediately.

## Support

- Product and account help: [https://openseason.life](https://openseason.life)
- Issues with this plugin repo: open a GitHub issue on this repository

## License

MIT. See [LICENSE](./LICENSE).
