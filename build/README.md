# Build scripts and tools

Scripts used to build, test, and package PnP PowerShell in this repository.

| Script | Function |
| ------ | -------- |
| `Build-Debug.ps1` | Builds a debug version for local testing |
| `Build-HelpFile.ps1` | Builds `PnP.PowerShell.dll-Help.xml` from Markdown under `documentation/` |
| `Build-Nightly.ps1` | Builds a nightly-style package (used by GitHub Actions) |
| `Build-Release.ps1` | Builds a release package |
| `Run-Tests.ps1` | Runs unit / integration tests |
| `Unlist-Nightly.ps1` | Limits how many nightly releases remain listed on the Gallery |
| `Generate-PredictorCommands.ps1` | Generates the predictor file from samples |
| `postCreateCommand.sh` | Dev container post-create hook |

## Usage notes

- **PowerShell 7** and the **.NET 8 SDK** are required for current 3.x builds.
- Close any session that has already imported `PnP.PowerShell` before running a build; otherwise copy steps into the modules folder can fail because files are locked.
- Cmdlet help is generated from Markdown in `documentation/`. Keep the existing front-matter / schema when editing those files.
- For the full contributor setup (fork, branch, debug attach), see:
  https://pnp.github.io/powershell/articles/gettingstartedcontributing.html
- This repo is a personal fork of [pnp/powershell](https://github.com/pnp/powershell); prefer upstream PRs for changes meant for the Gallery.
