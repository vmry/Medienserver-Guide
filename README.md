# Medienserver-Guide

Ein deutschsprachiger Einstieg in den eigenen Medienserver für die Self-Hosting-Community. Der Guide erklärt Plex und Jellyfin, Homeserver und NAS, Dedicated Server sowie Speicherplanung, Ordnerstruktur und Videowiedergabe.

**[Website](https://vmry.github.io/Medienserver-Guide/)** · [Guide auf GitHub lesen](docs/README.md)

Die Website wird mit [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) erstellt. Die Markdown-Quellen liegen unter `docs/`, die Navigation und Website-Einstellungen in `mkdocs.yml`. Der ursprüngliche [Entwurf der Version 1.0](draft/Guide-v1.0.md) bleibt als Archiv erhalten.

## Lokal entwickeln

Voraussetzung: Python 3.13 mit pip. Im Repository-Hauptverzeichnis ausführen, vorzugsweise in einer virtuellen Python-Umgebung:

```powershell
python -m pip install -r requirements.txt
python -m mkdocs serve
```

Die Vorschau ist unter `http://127.0.0.1:8000/Medienserver-Guide/` erreichbar und aktualisiert sich bei Änderungen. Ein Produktions-Build prüft auch Navigation und interne Dokumentationslinks:

```powershell
python -m mkdocs build --strict
```

Die fertige Website liegt anschließend unter `site/`. Dieser Build-Ordner wird nicht versioniert. Neue Seiten unter `docs/` ergänzen und in `mkdocs.yml` unter `nav` eintragen.

## Veröffentlichung

Einmalig im GitHub-Repository unter **Settings → Pages → Build and deployment → Source** die Option **GitHub Actions** wählen. Falls für die Umgebung `github-pages` Branch-Regeln gesetzt sind, muss `main` zugelassen sein.

Bei jedem Push auf `main` installiert `.github/workflows/deploy.yml` die Dependencies, führt den strikten Build aus und veröffentlicht das Ergebnis über die offiziellen GitHub-Pages-Actions. Der Workflow lässt sich auch manuell für `main` starten. Ein zusätzlicher Veröffentlichungsbranch ist nicht nötig. Details zum Verfahren stehen in der [GitHub-Pages-Dokumentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages).

Die Website-Adresse funktioniert nach dem ersten erfolgreichen Deployment. `site_url` berücksichtigt den Project-Page-Pfad `/Medienserver-Guide/`.
