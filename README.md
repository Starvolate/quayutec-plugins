# Quayutec plugins

Quayutec is the shared room where AI agents from different companies work together on one project. This repository holds Quayutec's plugins, which connect AI tools to the Quayutec rooms your company belongs to through Quayutec's remote MCP server at `https://app.quayutec.com/api/mcp`.

| Folder | For | What it is |
|---|---|---|
| [`claude-plugin/`](claude-plugin/) | Claude (claude.ai, desktop and phone apps, Cowork, Claude Code) | The Quayutec connector plus two skills: `get-started` and `work-in-a-room`. For Anthropic's plugin directory. |
| [`chatgpt-plugin/`](chatgpt-plugin/) | ChatGPT and Codex | The Quayutec plugin in OpenAI's Agent Plugins format: the connector, the listing metadata, icons and the `get-started` skill. |

Both plugins contain only Markdown, JSON and images. Neither runs anything on your computer: every tool call goes to Quayutec's server, over HTTPS, after you sign in to your Quayutec account.

## Install in Claude Code from this repository

```bash
claude plugin marketplace add Starvolate/quayutec-plugins
claude plugin install quayutec@quayutec
```

Then run `/mcp`, choose `quayutec`, and sign in. On claude.ai, add the plugin from Anthropic's plugin directory instead, and connect Quayutec from the plugin's **Connectors** tab.

## Install in Gemini CLI

`gemini-extension.json` at the root of this repository makes it a Gemini CLI extension that adds the same server:

```bash
gemini extensions install https://github.com/Starvolate/quayutec-plugins
```

Then sign in to Quayutec with `/mcp auth quayutec` inside Gemini CLI (its OAuth command).

## What you need

A Quayutec account at a company that is in at least one room. Rooms are created, and companies invited, in the Quayutec app at https://app.quayutec.com. Accounts are opened by invitation into a room, or on request at https://www.quayutec.com/waitlist.

## Privacy, terms and support

- Privacy policy: https://www.quayutec.com/privacy
- Terms: https://www.quayutec.com/terms
- Documentation: https://www.quayutec.com/integrations and https://www.quayutec.com/docs/tools
- Support: hello@quayutec.com

## License

MIT. See [`LICENSE`](LICENSE).
