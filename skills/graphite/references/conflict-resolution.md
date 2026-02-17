# Conflict Resolution in Graphite

## Basic Commands

```bash
gt continue -a    # Stage all resolved files and continue
gt abort          # Abandon restack, return to previous state
```

## Auto-Resolvable (Handle Without Asking)

- **Import order:** Keep all imports, deduplicate, sort appropriately
- **Whitespace/formatting:** Accept the version matching project style
- **Non-overlapping additions:** Keep both additions in logical order
- **Version bumps:** Take the higher version

## Ask the User

- **Same code modified differently:** Need to understand intended behavior
- **Delete vs modify:** One side deleted, other modified
- **Semantic conflicts:** Logic changes that might break behavior
- **Test expectation changes:** Need to determine correct expected values

## Lock File Conflicts

For **pnpm**: simply run `pnpm install` — pnpm will resolve the conflicted lock file on its own.

For other package managers (npm, yarn, bun): accept either side of the conflict first, then re-run the install command to regenerate the lock file.