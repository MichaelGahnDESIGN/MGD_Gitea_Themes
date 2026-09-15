# MGD Gitea Themes

Eine Sammlung moderner Themes für selbst gehostete Gitea-Instanzen von Michael Gahn DESIGN.

## Themes

### MGD Black Red

Dunkles Developer-Theme mit tiefschwarzer Oberfläche, anthrazitfarbenen Panels und roten Akzenten. Entwickelt zunächst für Gitea 1.27.x.

Datei: `themes/mgd-black-red/theme-mgd-black-red.css`

## Installation

Die CSS-Datei des gewünschten Themes in den Gitea-Custom-Pfad unter `public/assets/css/` kopieren.

Beispiel für eine Synology-Paketinstallation:

```text
/var/packages/gitea/var/custom/public/assets/css/theme-mgd-black-red.css
```

Anschließend in der Gitea-Konfiguration den Theme-Namen `mgd-black-red` unter `[ui]` aktivieren. Je nach bestehender Konfiguration beispielsweise:

```ini
[ui]
THEMES = gitea-auto,gitea-light,gitea-dark,mgd-black-red
DEFAULT_THEME = mgd-black-red
```

Danach Gitea vollständig neu starten und gegebenenfalls den Browser-Cache leeren.

> Vor Änderungen an der Gitea-Konfiguration immer ein Backup der Konfigurationsdatei erstellen.

## Kompatibilität

Die Sammlung wird primär gegen aktuelle Gitea-Versionen entwickelt. `MGD Black Red` startet mit Gitea 1.27.x als Zielversion.
