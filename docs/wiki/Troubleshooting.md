# Troubleshooting

## The theme does not appear in the selector

Confirm that the CSS file is inside `<CustomPath>/public/assets/css/`, that its filename starts with `theme-`, and that the matching ID is present in the `[ui]` `THEMES` setting.

For `theme-mgd-black-red.css`, the ID is `mgd-black-red`.

Restart Gitea after changing its configuration.

## The theme appears but looks like the default theme

Check that Gitea can read the CSS file and that the file is not empty. Then hard-refresh the browser to bypass cached CSS.

## Only parts of the interface are styled

This usually indicates a compatibility gap rather than an installation failure. Gitea's markup can change between releases. Record your exact Gitea version and the affected screen before opening an issue.

## Text is difficult to read

Report the exact component and state, for example `repository file table / hover` or `pull request diff / deleted line`. Contrast issues are treated as bugs.

## Gitea fails to start after editing the configuration

Restore the configuration backup first. Then inspect the Gitea logs for an INI/configuration parsing error. CSS theme files themselves should not prevent the Gitea process from starting, but a malformed configuration can.

## I set the custom theme as default and now want to remove it

Change `DEFAULT_THEME` to an installed theme before removing `mgd-black-red` from `THEMES` and before deleting its CSS file. Restart Gitea afterwards.

## Reporting a useful issue

Include the theme name, Gitea version, browser and OS, affected URL/page type, expected appearance, actual appearance and a screenshot when the visual problem is difficult to describe.

Repository issues: https://github.com/MichaelGahnDESIGN/MGD_Gitea_Themes/issues

[Back to Wiki Home](Home.md)
