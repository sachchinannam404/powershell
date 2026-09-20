# Contribution guidance

This repository is a **personal fork** of [pnp/powershell](https://github.com/pnp/powershell).

**Prefer contributing upstream** so changes reach Gallery users and the maintained docs site:

- Official repo: https://github.com/pnp/powershell
- Full setup, build, and PR guide: https://pnp.github.io/powershell/articles/gettingstartedcontributing.html

---

## Upstream contributions (recommended)

1. Fork **https://github.com/pnp/powershell** (or keep this fork synced with `pnp/dev`).
2. Create a **feature branch** off `dev` for each change.
3. Build and test using the official [getting started contributing](https://pnp.github.io/powershell/articles/gettingstartedcontributing.html) steps (PowerShell 7, .NET 8 SDK).
4. Open a pull request against **pnp/powershell** `dev`.
5. Use [Discussions](https://github.com/pnp/powershell/discussions) for design questions before large features.

## Working in this fork

Useful when experimenting locally before (or without) an upstream PR:

### Build

```powershell
# Close any pwsh session that already loaded PnP.PowerShell
./build/Build-Debug.ps1
```

Other scripts are listed in [`build/README.md`](build/README.md).

### Documentation

| Path | Content |
|------|---------|
| `documentation/` | One Markdown file per cmdlet; keep existing YAML/schema headers |
| `pages/articles/` | Conceptual articles for the DocFX site |
| `pages/index.md` | Docs site home |

### Code conventions

- Most cmdlets extend `PnPCmdlet` or `PnPWebCmdlet`. Prefer `ClientContext` / connection helpers so multi-connection scenarios stay correct.
- Use approved PowerShell verbs.
- One logical change per pull request when contributing upstream.

## Keeping the fork current

```powershell
git remote add upstream https://github.com/pnp/powershell.git   # once
git fetch upstream
git checkout dev
git merge upstream/dev   # or: git reset --hard upstream/dev if you intend a hard sync
git push origin dev
```

GitHub’s **Sync fork** UI works well when you are not rewriting history.

## Questions

- Bugs: https://github.com/pnp/powershell/issues
- How-to: https://github.com/pnp/powershell/discussions
