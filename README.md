# agent-skills

[Agent Skills](https://agentskills.io) for devorgpl tools. Each skill is a folder in `skills/` with a `SKILL.md` that AI coding agents (Claude Code, GitHub Copilot, Codex, Cursor and others) load when a task needs it.

| Skill | What it does |
|---|---|
| [`compost`](skills/compost/SKILL.md) | Deploys docker-compose apps to Linux servers with the [compost](https://github.com/devorgpl/compost) CLI. Covers its config files, shared apps, secrets, backups, and moving existing Docker servers to compost. |

## Install

With the [GitHub CLI](https://cli.github.com) (`gh skill`):

```sh
gh skill install devorgpl/agent-skills compost                                   # asks which agent and scope
gh skill install devorgpl/agent-skills compost --agent claude-code --scope user  # Claude Code, all your projects
```

Without a version, you get the skill of the latest stable compost release. To install a given release, or keep it from changing with `gh skill update`:

```sh
gh skill install devorgpl/agent-skills compost@compost-vX.Y.Z
gh skill install devorgpl/agent-skills compost --pin compost-vX.Y.Z
```

Update installed skills with `gh skill update`.

## Where the files come from

Don't edit the skills here. Each one is published from its tool's repository when that tool is released, and the next release overwrites changes made here. The `compost` skill comes from [`docs/agents/skills/compost`](https://github.com/devorgpl/compost/tree/master/docs/agents/skills/compost), and every stable compost release `vX.Y.Z` commits it here and tags `compost-vX.Y.Z`.

## License

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE) or [MIT license](LICENSE-MIT) at your option.
