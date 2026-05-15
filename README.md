# Theo's Demo Copilot Skills

A demo-friendly collection of [Agent Skills](https://agentskills.io/specification) for GitHub Copilot, packaged so they are easy to install during demos.

Most skills here are copied or lightly adapted from other public skill packages, with attribution in each `SKILL.md` and in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md). The goal is convenience and repeatable demos, not claiming original authorship.

## Requirements

- GitHub CLI v2.90.0+
- A Copilot environment that supports Agent Skills

## Install

```bash
gh skill install theomonfort/skills <skill-name>
```

Preview before installing:

```bash
gh skill preview theomonfort/skills <skill-name>
```

Update installed skills:

```bash
gh skill update --all
```

## Skills

| Name | Description |
| ---- | ----------- |
| [grill-me](skills/grill-me/) | Matt Pocock's famous grilling skill: interview the user one question at a time until the plan is sharp. |
| [hands-on-helper](skills/hands-on-helper/) | Help participants complete Theo Monfort's GitHub Copilot hands-on workshop with the right repo, guide links, playbook references, and troubleshooting steps. |
| [github-issues](skills/github-issues/) | Create well-structured GitHub Issues with templates, labels, priorities and dependencies. Mirrored from [`github/awesome-copilot`](https://github.com/github/awesome-copilot/tree/main/skills/github-issues). |
| [github-support](skills/github-support/) | Answer GitHub support questions from public sources only, with exact URLs, quoted evidence, and mandatory double-checking. |
| [md-slides-creator](skills/md-slides-creator/) | Author a single Markdown file that doubles as a long-form doc AND a slide deck (one slide per `## H2`). Captures the conventions used by the [theomonfort playbook](https://theomonfort.github.io/theomonfort/playbook/) — frontmatter schema, hero-quote variants, comparison tables, callout patterns, link groups. |
| [research-codebase](skills/research-codebase/) | Research and document how an existing codebase works by coordinating parallel exploration and synthesizing findings. |
| [write-a-skill](skills/write-a-skill/) | Create new agent skills with a concise `SKILL.md`, progressive disclosure, references, and optional scripts. |

## Validate

Run the GitHub CLI skill validator before publishing changes:

```bash
gh skill publish --dry-run
```

This checks skill discovery, required frontmatter, naming rules, and publish readiness without creating a release.

## Authoring a new skill

Each skill is a folder containing a `SKILL.md` file (see [agentskills.io](https://agentskills.io/specification)). Optional bundled assets (scripts, reference docs, templates) sit next to it.

```
skills/
  my-skill/
    SKILL.md
    references/
      foo.md
```

Before opening a PR or publishing:

1. Keep the folder name and `name:` frontmatter identical.
2. Include `description:` and `license:` in `SKILL.md`.
3. Put long examples, templates, or API notes in `references/` so the main skill stays scannable.
4. Run `gh skill publish --dry-run`.

## License

This repository is MIT licensed. Some bundled demo skills are copied from third-party projects under their original licenses; see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
