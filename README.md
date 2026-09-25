<!-- MGD-HEADER -->
<p align="center"><a href="https://Michael-Gahn.de"><img src="assets/mgd-logo.png" alt="Michael Gahn DESIGN" width="48"></a></p>

<p align="center"><img src="assets/banner.svg" alt="MGD Gitea Themes" width="100%"></p>

<p align="center">
  <img alt="Lizenz" src="https://img.shields.io/github/license/MichaelGahnDESIGN/MGD_Gitea_Themes?label=Lizenz">
  <img alt="Sprache" src="https://img.shields.io/badge/Sprache-CSS-2f6fed">
  <a href="https://Michael-Gahn.de"><img alt="by Michael Gahn DESIGN" src="https://img.shields.io/badge/by-Michael%20Gahn%20DESIGN-cd1616"></a>
</p>
<!-- /MGD-HEADER -->

<div align="center">

# MGD Gitea Themes

### Modern themes for a Gitea that deserves to look as good as the code it hosts.

A growing collection of carefully designed themes for self-hosted Gitea instances, created and maintained by **Michael Gahn DESIGN**.

[![Gitea](https://img.shields.io/badge/Gitea-1.27.x-609926?logo=gitea&logoColor=white)](https://about.gitea.com/)
[![CSS](https://img.shields.io/badge/CSS-Custom%20Themes-663399?logo=css&logoColor=white)](https://github.com/MichaelGahnDESIGN/MGD_Gitea_Themes)
[![Status](https://img.shields.io/badge/status-active-success)](https://github.com/MichaelGahnDESIGN/MGD_Gitea_Themes)
[![GitHub stars](https://img.shields.io/github/stars/MichaelGahnDESIGN/MGD_Gitea_Themes?style=flat)](https://github.com/MichaelGahnDESIGN/MGD_Gitea_Themes/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/MichaelGahnDESIGN/MGD_Gitea_Themes?style=flat)](https://github.com/MichaelGahnDESIGN/MGD_Gitea_Themes/forks)

[Themes](#themes) · [Quick Start](#quick-start) · [Documentation](docs/wiki/Home.md) · [Contributing](#contributing) · [More MGD Open Source](#more-open-source-by-michael-gahn-design)

</div>

---

## Why MGD Gitea Themes?

Gitea is fast, lightweight and excellent for self-hosting. Its interface is functional, but a private Git server can also be part of a visual identity.

**MGD Gitea Themes** turns Gitea's built-in custom-theme support into a curated design collection. The goal is not to replace Gitea's interface, but to refine it: better visual hierarchy, carefully chosen contrast, polished states and a coherent appearance across repositories, issues, pull requests, code views and administration.

The themes remain CSS-based and keep Gitea itself untouched. No fork of Gitea is required.

## Themes

### MGD Black Red

> Deep black. Anthracite surfaces. Precise red accents.

`MGD Black Red` is the first theme in the collection. It is designed as a modern developer interface rather than a simple recolor.

| | |
| --- | --- |
| Theme ID | `mgd-black-red` |
| File | `themes/mgd-black-red/theme-mgd-black-red.css` |
| Target | Gitea 1.27.x |
| Base | Dark |
| Accent | Red |
| Status | Active development |

It includes custom styling for navigation, repository surfaces, cards, forms, buttons, tables, Markdown, code and diff views, labels, progress elements, selection states and scrollbars.

More themes will be added to this repository over time.

## Quick Start

### 1. Get the theme

Clone the repository:

```bash
git clone https://github.com/MichaelGahnDESIGN/MGD_Gitea_Themes.git
```

Or download the CSS file for the theme you want to use.

### 2. Copy it into Gitea

Gitea loads custom themes from its custom directory:

```text
<CustomPath>/public/assets/css/
```

Copy:

```text
themes/mgd-black-red/theme-mgd-black-red.css
```

to:

```text
<CustomPath>/public/assets/css/theme-mgd-black-red.css
```

For the Synology package installation used during development, the resulting path is:

```text
/var/packages/gitea/var/custom/public/assets/css/theme-mgd-black-red.css
```

Your installation can use a different `CustomPath`. Check **Site Administration → Configuration** before copying files.

### 3. Enable the theme

Back up your Gitea configuration first. Then add the theme ID to the `[ui]` configuration.

```ini
[ui]
THEMES = gitea-auto,gitea-light,gitea-dark,mgd-black-red
DEFAULT_THEME = mgd-black-red
```

You do not have to make it the default. Leaving `DEFAULT_THEME` unchanged makes the theme available as a selectable option instead.

### 4. Restart Gitea

Restart the Gitea service completely. If the previous styles remain visible, perform a hard refresh or clear the browser cache.

That's it. Your Gitea now has a new skin.

## Repository Structure

```text
MGD_Gitea_Themes/
├── themes/
│   └── mgd-black-red/
│       └── theme-mgd-black-red.css
├── docs/
│   └── wiki/
│       ├── Home.md
│       ├── Installation.md
│       ├── Theme-Development.md
│       ├── Troubleshooting.md
│       └── Compatibility.md
└── README.md
```

Each theme lives in its own directory so the collection can grow without turning into a pile of unrelated CSS files.

## Documentation

The full documentation is maintained in the repository under [`docs/wiki`](docs/wiki/Home.md). It covers installation, configuration, theme development, compatibility and troubleshooting.

Useful upstream documentation:

* [Gitea: Customizing Gitea](https://docs.gitea.com/administration/customizing-gitea)
* [Gitea Documentation](https://docs.gitea.com/)

## Compatibility

The first development target is **Gitea 1.27.x**. Gitea's markup and CSS variables can change between releases, so a theme that works perfectly on one release may need adjustments on another.

The project therefore treats compatibility as an explicit part of theme development rather than assuming every CSS file works forever. See the [compatibility documentation](docs/wiki/Compatibility.md) before reporting a visual regression.

## Design Principles

The collection follows a few simple rules: Gitea must remain recognizable and usable, contrast must stay readable, destructive and semantic states must remain understandable, code and diff readability take priority over decoration, and themes should use Gitea's supported customization mechanism instead of patching core files.

A theme should feel intentional on the dashboard, inside a repository and deep inside a pull request, not just on the first screen.

## Contributing

Ideas, compatibility fixes and improvements are welcome. If you find a visual problem, include your Gitea version, the affected page, browser and ideally a screenshot with the report.

For larger design changes, opening an issue before investing significant work helps keep the collection visually coherent.

## Roadmap

The collection starts with `MGD Black Red`. Planned work includes broader Gitea 1.27.x coverage, dedicated states for Actions and administration, visual regression cleanup, additional dark themes and eventually carefully designed light variants.

## More Open Source by Michael Gahn DESIGN

If this project is useful to you, there is more public work in the same GitHub account:

| Project | What it does |
| --- | --- |
| [MGD WordPress MCP](https://github.com/MichaelGahnDESIGN/MGD_WordPress-MCP) | MCP tooling around WordPress workflows |
| [MGD Claude Codex MCP](https://github.com/MichaelGahnDESIGN/MGD_Claude-Codex_MCP) | Local MCP system for tasks and handoffs between AI coding agents |
| [MGD DEV Skill](https://github.com/MichaelGahnDESIGN/MGD_DEV_SKILL) | Reusable development workflow for AI coding agents |
| [MGD Autopilot Skill](https://github.com/MichaelGahnDESIGN/MGD_Autopilot_SKILL) | Guardrailed autonomous project workflow |
| [MGD Divi 5 Dev Skill](https://github.com/MichaelGahnDESIGN/MGD_Divi5-Dev_SKILL) | Development workflow for WordPress and Divi 5 |
| [MGD AI Kennzeichnung for WordPress](https://github.com/MichaelGahnDESIGN/MGD-AI-Kennzeichnung-WordPress) | AI-content labeling for WordPress |
| [MGD AI Kennzeichnung for Shopware 6](https://github.com/MichaelGahnDESIGN/MGD-AI-Kennzeichnung-Shopware-6) | AI-content labeling for Shopware 6 |
| [MGD AI Kennzeichnung for JTL-Shop 5](https://github.com/MichaelGahnDESIGN/MGD-AI-Kennzeichnung-JTL-Shop-5) | AI-content labeling for JTL-Shop 5 |
| [MGD JTL SEO Plugin](https://github.com/MichaelGahnDESIGN/MGD_JTL-SEO-Plugin) | SEO tooling for JTL-Shop |
| [All public repositories](https://github.com/MichaelGahnDESIGN?tab=repositories&type=public) | The complete public project collection |

A curated overview is also available at [michael-gahn.de/eigene-projekte](https://michael-gahn.de/eigene-projekte/).

## Credits

Designed and maintained by **Michael Gahn DESIGN**.

This project is independent and is not an official Gitea project. Gitea and its trademarks belong to their respective owners.

---

<div align="center">

**Michael Gahn DESIGN** · Webdesign · eCommerce · Development · AI

[Website](https://michael-gahn.de/) · [GitHub](https://github.com/MichaelGahnDESIGN) · [Projects](https://michael-gahn.de/eigene-projekte/) · [Impressum](https://michael-gahn.de/impressum/)

</div>
