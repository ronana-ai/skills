# Ronana skills

Agent skills for [Ronana](https://ronana.ai): make and edit images and videos, upscale video, and keep the results organized, from Claude Code, Codex and other agents.

## Install

Any agent:

```bash
npx skills add ronana-ai/skills
```

Claude Code, as a plugin:

```text
/plugin marketplace add ronana-ai/skills
/plugin install ronana@ronana
```

Then ask your agent for an image or a video. It installs the [Ronana command line](https://github.com/ronana-ai/cli) and signs you in through your browser on first use. Generating spends your Ronana credits.

## Security

The skills are Markdown instructions with no code of their own. They never ask your agent for a password, an API key or payment details. See [SECURITY.md](SECURITY.md) for what they do and how to report a problem.

## Contributing

This repository is published from Ronana's internal source, so pull requests are closed automatically. Issues are welcome: see [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE)
