# Theme Development

MGD Gitea Themes is intended to become a collection, so every theme should be maintainable independently.

## Directory convention

Use one directory per theme:

```text
themes/<theme-id>/theme-<theme-id>.css
```

Example:

```text
themes/mgd-black-red/theme-mgd-black-red.css
```

Keep IDs lowercase and predictable.

## Design priorities

A theme must preserve usability before adding visual personality. Test navigation, repository lists, file browsers, Markdown, code views, diffs, issues, pull requests, forms, dialogs, labels, status colors, Actions and administration.

Semantic colors deserve special care. Error, warning, success, destructive actions and diff additions/deletions should remain immediately distinguishable.

## Prefer variables

Where Gitea exposes suitable CSS variables, override those before writing highly specific selectors. This reduces duplication and usually improves coverage across the interface.

Theme-specific design tokens can live near the top of the stylesheet:

```css
:root {
  --mgd-red: #e21b2d;
  --mgd-bg: #090a0c;
  --mgd-panel: #111318;
}
```

## Avoid core modifications

Do not edit Gitea's bundled CSS, templates or application source just to make a theme work. The collection should use Gitea's supported custom-file mechanism whenever possible.

## Test matrix

Before considering a theme stable, inspect at minimum:

1. Dashboard and Explore
2. Repository overview and file browser
3. Source code and Markdown rendering
4. Issues and labels
5. Pull requests and diff views
6. Releases and packages where available
7. Actions
8. User settings
9. Site administration
10. Narrow/mobile layouts

Test hover, focus, active, disabled, selected and error states, not only static screenshots.

## New Gitea releases

Gitea can change markup, class names and variables. When upgrading the target Gitea version, verify the complete interface rather than assuming visual compatibility from the login page or dashboard alone.

## Adding a new theme

Create its directory and CSS file, document its ID and target version in the root README and update the Wiki Home page. A screenshot or preview image can be added when it provides useful visual information.

[Back to Wiki Home](Home.md)
