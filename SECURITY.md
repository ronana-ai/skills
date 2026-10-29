# Security policy

## Reporting a vulnerability

Please report security problems privately, never in a public issue:

- **GitHub:** [report a vulnerability](https://github.com/ronana-ai/skills/security/advisories/new)
  (private to you and the Ronana team), or
- **Email:** security@ronana.ai

We acknowledge reports within 3 business days and keep you informed until it is
resolved.

## What these skills do

The skills are plain Markdown instructions for your AI agent. They contain no
code and run nothing by themselves. Your agent reads them and decides what to
run, and your agent app asks you before it runs a command, as usual.

The instructions tell your agent to:

- install the Ronana command line from npm (`@ronana/mcp`, open source at
  [github.com/ronana-ai/cli](https://github.com/ronana-ai/cli)),
- sign you in with `ronana auth login`, which opens Ronana in your browser,
- run `ronana` commands to check prices, generate, upload and organize media.

They never ask your agent to handle a password, an API key or payment details,
and never to use `sudo`. Generating spends your Ronana credits; the skill tells
your agent to check the price first. What the command line can access, and how
to disconnect it, is described in the
[CLI security policy](https://github.com/ronana-ai/cli/blob/main/SECURITY.md).
