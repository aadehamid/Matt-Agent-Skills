# Contributing / Maintenance

This repository is a **fork of [`mattpocock/skills`](https://github.com/mattpocock/skills)**. We customize upstream skills (e.g. the `teach` skill) while staying able to pull updates from the source.

## Branch model

```
upstream/main ─── main          (a CLEAN mirror of mattpocock/skills — nothing of ours)
                    └── experiment   (all our customizations = main + our commits)
```

- **`main`** — kept identical to `upstream/main`. Do **not** commit to it directly.
- **`experiment`** — where all our work lives. This is the working branch.

Keeping `main` pristine means upstream updates always fast-forward, so source changes fold into our work with minimal conflict.

## Remotes

| Remote | URL | Role |
|--------|-----|------|
| `origin` | `https://github.com/aadehamid/Matt-Agent-Skills.git` | Our fork |
| `upstream` | `https://github.com/mattpocock/skills.git` | The source |

First-time setup (if `upstream` is missing):

```bash
git remote add upstream https://github.com/mattpocock/skills.git
git fetch upstream
```

## Pulling updates from the source

```bash
# 1. Refresh main as a clean mirror of the source
git fetch upstream
git switch main
git merge --ff-only upstream/main     # fast-forward only — keeps main pristine
git push origin main                  # keep the fork's main in sync (optional)

# 2. Apply the updates to our customizations
git switch experiment
git merge main                        # resolve any conflicts in customized files here
git push
```

## Rules

- **Never commit directly to `main`.** Always work on `experiment`. This guarantees the `--ff-only` step always succeeds.
- **Merge, don't rebase, into `experiment`.** `experiment` is already pushed/shared, so merging avoids rewriting public history. (Rebase gives cleaner history but requires a force-push.)
- Customizations currently live under `skills/productivity/teach/` — expect merge conflicts there when upstream changes the same files.
