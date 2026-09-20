# PnP PowerShell

> **Fork notice:** This repository is a personal fork of the official [pnp/powershell](https://github.com/pnp/powershell) project.
> For production use, issues, discussions, and pull requests, prefer the upstream repository:
> **https://github.com/pnp/powershell**
>
> Upstream maintains **PnP PowerShell 3.x** (.NET 8, PowerShell 7.4.0+).

---

**PnP PowerShell** is a .NET 8 based PowerShell module providing close to 900 cmdlets that work with Microsoft 365 environments such as SharePoint Online, Microsoft Teams, Microsoft Project, Security & Compliance, Entra ID, and more.

Starting with version 3.1.379-nightly, official releases (including nightlies) are fully digitally signed and work on machines restricted with the `AllSigned` PowerShell execution policy. Major thanks to the [.NET Foundation](https://dotnetfoundation.org) for providing the signing certificate.

Last version | Last nightly version
-------------|---------------------
[![PnP.PowerShell](https://img.shields.io/powershellgallery/v/pnp.powershell)](https://www.powershellgallery.com/packages/PnP.PowerShell/) | [![PnP.PowerShell](https://img.shields.io/powershellgallery/v/pnp.powershell?include_prereleases)](https://www.powershellgallery.com/packages/PnP.PowerShell/)

[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/pnp/powershell/badge)](https://scorecard.dev/viewer/?uri=github.com/pnp/powershell)

This module is a successor of the [PnP-PowerShell](https://github.com/pnp/pnp-powershell) module. The original cmdlets only work on Windows and Windows PowerShell and support SharePoint On-Premises (2013, 2016 and 2019) and SharePoint Online. This version is cross-platform (Windows, macOS, and Linux) and targets SharePoint Online / Microsoft 365. Only the cross-platform PnP PowerShell module is still being updated.

For installing or upgrading, see [the documentation](https://pnp.github.io/powershell/articles/index.html).

## IMPORTANT - New PnP PowerShell 3.x

PnP PowerShell 3.x requires **PowerShell 7.4.0 or newer** and is based on **.NET 8.0**.

Upgrade guide from 2.x: [MIGRATE-2.0-to-3.0.md](https://github.com/pnp/powershell/blob/dev/MIGRATE-2.0-to-3.0.md)

If you still use Windows PowerShell 5.1 or the ISE and need a Gallery install that works there, pin an older 1.x release, for example:

```powershell
Install-Module PnP.PowerShell -RequiredVersion 1.12.0 -Force
```

For current 3.x:

```powershell
Install-Module PnP.PowerShell -Force
# prerelease / nightly:
Install-Module PnP.PowerShell -AllowPrerelease -Force
```

## Documentation in this repository

| Location | Purpose |
|----------|---------|
| [`documentation/`](documentation/) | Per-cmdlet Markdown help (source for external help and the docs site) |
| [`pages/`](pages/) | DocFX articles and site content |
| [`CHANGELOG.md`](CHANGELOG.md) | Release history |
| [`MIGRATE-2.0-to-3.0.md`](MIGRATE-2.0-to-3.0.md) | Breaking-change migration notes |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to contribute |
| [`build/README.md`](build/README.md) | Local build and release scripts |

Public docs site: https://pnp.github.io/powershell/

## Building from source

1. Use **PowerShell 7** and the **.NET 8 SDK**.
2. Close any session that already imported `PnP.PowerShell` (file locks during copy).
3. From the `build` folder, run `Build-Debug.ps1` for a local debug build. See [`build/README.md`](build/README.md).

Contributor walkthrough: https://pnp.github.io/powershell/articles/gettingstartedcontributing.html

## Supportability and SLA

This library is open-source and community provided. It is **not** a Microsoft product and has **no Microsoft SLA**. For the PnP initiative, see [Microsoft 365 & Power Platform Community](https://pnp.github.io).

- Issues / bugs (upstream): https://github.com/pnp/powershell/issues
- Questions: https://github.com/pnp/powershell/discussions

## .NET Foundation

This project is supported by the [.NET Foundation](https://dotnetfoundation.org) and has adopted the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).

![.NET Foundation](dotnetfoundation_v4_small.png ".NET Foundation")

<img src="https://m365-visitor-stats.azurewebsites.net/pnp-powershell/readme" alt="" />
