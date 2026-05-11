# Theo's Copilot Skills

A collection of [Agent Skills](https://agentskills.io/specification) for GitHub Copilot, packaged for easy install.

## Install

```bash
gh skill install theomonfort/copilot-skills <skill-name>
```

Requires GitHub CLI v2.90.0+.

## Skills

| Name | Description |
| ---- | ----------- |
| [github-issues](skills/github-issues/) | Create well-structured GitHub Issues with templates, labels, priorities and dependencies. Mirrored from [`github/awesome-copilot`](https://github.com/github/awesome-copilot/tree/main/skills/github-issues). |

## Authoring a new skill

Each skill is a folder containing a `SKILL.md` file (see [agentskills.io](https://agentskills.io/specification)). Optional bundled assets (scripts, reference docs, templates) sit next to it.

```
skills/
  my-skill/
    SKILL.md
    references/
      foo.md
```

## License

MIT
