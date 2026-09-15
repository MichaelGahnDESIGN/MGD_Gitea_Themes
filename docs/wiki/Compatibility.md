# Compatibility

Custom Gitea themes depend on Gitea's HTML structure and CSS variables. Compatibility therefore needs to be tested against actual Gitea releases.

## Current target

| Theme | Target | Status |
| --- | --- | --- |
| MGD Black Red | Gitea 1.27.x | Active development |

The initial theme was created against a Gitea 1.27.2 installation.

## What compatibility means here

A compatible theme should keep all major Gitea functions visually usable. It does not mean that every future Gitea version is automatically supported because the CSS file still loads.

Minor visual regressions can occur when Gitea introduces new components. Major releases may require selector or variable changes.

## Before upgrading Gitea

Keep a copy of your working theme and Gitea configuration. After the Gitea update, inspect repository navigation, forms, Markdown, code, diffs, issues, pull requests, Actions, settings and administration.

If a regression appears, temporarily switch to an official Gitea theme while the custom theme is being updated.

## Reporting compatibility problems

Please include the exact Gitea version. `latest` is not enough because it changes over time. Also include the theme version or commit, browser and affected component.

[Back to Wiki Home](Home.md)
