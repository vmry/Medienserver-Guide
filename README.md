# Medienserver-Guide

Ein deutschsprachiger Einstieg in den eigenen Medienserver für die Self-Hosting-Community. Der Guide erklärt Plex und Jellyfin, Homeserver und NAS, Dedicated Server sowie Speicherplanung, Ordnerstruktur und Videowiedergabe.

**[Zum Guide](docs/README.md)** · [Inhaltsverzeichnis](SUMMARY.md)

Die Dokumentation liegt unter `docs/`. Der ursprüngliche [Entwurf der Version 1.0](draft/Guide-v1.0.md) bleibt als Archiv erhalten.

Das Repository ist für **GitBook Git Sync** vorbereitet. `gitbook-docs.yaml` beschreibt die Site mit einem deutschsprachigen Standard-Space. Die weiterhin benötigte `.gitbook.yaml` legt `docs/README.md` als Startseite und `SUMMARY.md` als Navigation fest. Beide Konfigurationsdateien liegen im Repository-Hauptverzeichnis; siehe die [GitBook-Konfigurationsreferenz](https://gitbook.com/docs/docs-as-code/git-sync/content-configuration).

Beim [Verbinden mit GitHub](https://gitbook.com/docs/docs-as-code/git-sync/enabling-github-sync) diese Einstellungen verwenden:

- **Source repository:** `vmry/Medienserver-Guide`, **Branch:** `main`.
- **Project directory:** leer lassen (Repository-Hauptverzeichnis).
- **Initial sync direction:** GitHub → GitBook; gegebenenfalls **Swap direction** wählen.
- **Content mapping:** den Guide-Space auf `./` abbilden. So bleiben `.gitbook.yaml` und die Navigation im Hauptverzeichnis erreichbar, während die Guide-Seiten unter `docs/` liegen.

Die Konfiguration muss vor dem Verbinden auf dem ausgewählten GitHub-Branch vorhanden sein; lokale Änderungen werden nicht synchronisiert. Den Space-Schlüssel `medienserver-guide` nach der ersten Verbindung beibehalten, damit GitBook den Space bei späteren Änderungen wiedererkennt.

Neue Kapitel unter `docs/` ergänzen und in `SUMMARY.md` verlinken. Inhaltsdateien verwenden Kleinbuchstaben und Bindestriche; `README.md` und `SUMMARY.md` bleiben die konventionellen Ausnahmen.
