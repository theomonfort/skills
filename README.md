# Theo's Copilot Skills

A collection of [Agent Skills](https://agentskills.io/specification) for GitHub Copilot, packaged for easy install.

## Install

```bash
gh skill install theomonfort/skills <skill-name>
```

Requires GitHub CLI v2.90.0+.

## Skills

| Name | Description |
| ---- | ----------- |
| [github-issues](skills/github-issues/) | Create well-structured GitHub Issues with templates, labels, priorities and dependencies. Mirrored from [`github/awesome-copilot`](https://github.com/github/awesome-copilot/tree/main/skills/github-issues). |
| [md-slides-creator](skills/md-slides-creator/) | Author a single Markdown file that doubles as a long-form doc AND a slide deck (one slide per `## H2`). Captures the conventions used by the [theomonfort playbook](https://theomonfort.github.io/theomonfort/playbook/) — frontmatter schema, hero-quote variants, comparison tables, callout patterns, link groups. |

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
