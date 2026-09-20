# PnP PowerShell

PnP PowerShell is a cross-platform PowerShell module providing **close to 900 cmdlets** for Microsoft 365 products such as SharePoint Online, Microsoft Teams, Microsoft Planner, Microsoft Power Platform, Microsoft Entra, Microsoft Purview, Microsoft Search, and more. It runs on Windows, Linux, and macOS.

> [!NOTE]
> This documentation tree is published from a **personal fork** of [pnp/powershell](https://github.com/pnp/powershell).
> Issues, discussions, and pull requests should normally target the **upstream** repository so the community and Gallery builds benefit.

> [!NOTE]
> As of September 9<sup>th</sup>, 2024, as part of a focus on improving the security posture, the multi-tenant PnP Management Shell Entra ID app (with Client/ApplicationID: `31359c7f-bd7e-475c-86db-fdb8c937548e`) has been deleted. It impacts credentials (username + password), Interactive auth flow, and Device login flow if they depended on that multi-tenant app.
>
> It has always been a recommended practice to register your own Entra ID application with the minimal permissions required for your scripts. [This has become a mandatory step](https://github.com/pnp/powershell/discussions/4249). The linked post has more details and will guide you through restoring scripts with minimal code changes.

## Getting up and running

Starting to use PnP PowerShell consists of 3 steps:

1. [Installing the PnP.PowerShell module](./articles/installation.md)

2. [Registering your own Entra ID application](./articles/registerapplication.md)

3. [Connecting and authenticating](./articles/authentication.md)

**Requirements for 3.x:** PowerShell **7.4.0+** and .NET 8–based builds. See the [2.x → 3.x migration guide](https://github.com/pnp/powershell/blob/dev/MIGRATE-2.0-to-3.0.md).

Once you're set up, check the [cmdlets](/powershell/cmdlets) section for what you can do. The [articles](/powershell/articles) section covers authentication, batching, Azure Functions, and more.

Official docs site: https://pnp.github.io/powershell/

## I've found a bug, where do I log an issue or create a PR?

Use the **upstream** repository:

- Issues: https://github.com/pnp/powershell/issues
- Discussions (questions): https://github.com/pnp/powershell/discussions

Please prefer Discussions for how-to questions so Issues can stay focused on bugs and concrete product work.

Some behaviour lives in related PnP libraries (for example PnP Framework / PnP Core). Issues may be moved; you will be notified if that happens.

Before a large code change, start a discussion first—someone may already be working on the same feature, and maintainers can advise on approach.

## Contributing to PnP PowerShell

Follow the [getting started contributing](/powershell/articles/gettingstartedcontributing.html) guidelines. Sharing is caring!

If you are working in this fork first, see also [`CONTRIBUTING.md`](https://github.com/sachchinannam404/powershell/blob/dev/CONTRIBUTING.md) for local build notes and how to sync with upstream.

## Supportability and SLA

This library is open-source and community provided. It is **not** a Microsoft product and has **no Microsoft SLA**. Report issues on the [upstream issues list](https://github.com/pnp/powershell/issues).

## .NET Foundation

This project is supported by the [.NET Foundation](https://dotnetfoundation.org) and has adopted the [.NET Foundation Code of Conduct](https://dotnetfoundation.org/code-of-conduct).

![.NET Foundation](images/dotnetfoundation_v4_small.png ".NET Foundation")

<img src="https://m365-visitor-stats.azurewebsites.net/pnp-powershell/readme" alt="" />
