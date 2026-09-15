# Installation

This guide explains the generic Gitea installation process. Paths vary depending on Docker, packages, NAS distributions and manual installations.

## 1. Find the CustomPath

Open **Site Administration → Configuration** in Gitea and locate the custom-file root path. Do not assume a path from another installation is correct for yours.

Gitea custom theme CSS belongs in:

```text
<CustomPath>/public/assets/css/
```

## 2. Copy the theme

For MGD Black Red, copy:

```text
themes/mgd-black-red/theme-mgd-black-red.css
```

as:

```text
<CustomPath>/public/assets/css/theme-mgd-black-red.css
```

The filename matters. Gitea derives the theme ID from the `theme-*.css` naming convention.

## 3. Back up the configuration

Before editing your Gitea configuration, create a copy of it. Package and Docker installations can store the configuration in different places.

## 4. Enable the theme

Add `mgd-black-red` to the configured theme list:

```ini
[ui]
THEMES = gitea-auto,gitea-light,gitea-dark,mgd-black-red
```

To use it as the default:

```ini
DEFAULT_THEME = mgd-black-red
```

If you want users to choose it manually, keep your existing default theme.

## 5. Restart Gitea

Restart the Gitea service. A browser reload alone is not enough after configuration changes.

If old styles are cached, use a hard refresh.

## Synology package example

The development installation currently uses this custom path:

```text
/var/packages/gitea/var/custom
```

which results in:

```text
/var/packages/gitea/var/custom/public/assets/css/theme-mgd-black-red.css
```

Treat this only as an example. Verify the path shown by your own Gitea installation.

## Updating a theme

Replace the existing CSS file with the newer version, restart Gitea when necessary and hard-refresh the browser. Always review release notes when a future theme version introduces compatibility changes.

## Uninstalling

Remove the theme ID from `THEMES`, change `DEFAULT_THEME` first if it points to the theme, restart Gitea and then remove the CSS file.

[Back to Wiki Home](Home.md)
