# Cursor Skills

A collection of agent skills for [Cursor](https://cursor.com).

## Installation

Install skills using the [skills CLI](https://skills.sh/):

```bash
npx skills add AllySummers/skills
```

Or clone the repo directly and reference the skills you need:

```bash
git clone https://github.com/AllySummers/skills.git .cursor/skills
```

## Skills

| Skill | Description |
|-------|-------------|
| [graphite](skills/graphite/) | Graphite CLI stacked PR workflows |

### graphite

Skill for [Graphite](https://graphite.dev) CLI (`gt`) stacked PR workflows.

| Feature | Description |
|---------|-------------|
| Detection | Auto-detects Graphite repos via `.git/.graphite_repo_config` |
| Commands | Uses `gt` commands instead of `git` for commits/branches |
| Stack planning | Break features into atomic, reviewable PRs |
| Conflict resolution | Guidance for handling restack conflicts |

**Prerequisites:** Graphite CLI — `brew install withgraphite/tap/graphite` or `npm install -g @withgraphite/graphite-cli@stable`

> Adapted from [georgeguimaraes/claude-code-graphite](https://github.com/georgeguimaraes/claude-code-graphite) (Apache-2.0). See [NOTICE](NOTICE) for details.

## License

Licensed under the Apache License, Version 2.0. See [LICENSE](LICENSE) for the full text.

Some skills in this collection are derivative works. See [NOTICE](NOTICE) for attribution details.
