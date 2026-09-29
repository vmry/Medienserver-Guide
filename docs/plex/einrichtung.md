# Plex einrichten

Die genaue Installation hängt vom Betriebssystem und der Hardware ab. Dieser Ablauf beschreibt den Weg von der Serverinstallation zur ersten Bibliothek; er ersetzt keine systemspezifische Installationsanleitung.

## Vorbereitung

Dein Server muss erreichbar sein, und die Medien sollten bereits in getrennten [Film- und Serienordnern](../grundlagen/ordnerstruktur.md) liegen. Plex benötigt Leserechte für diese Ordner.

## Einrichtung Schritt für Schritt

1. Installiere **Plex Media Server** in der zu deinem System passenden Version.
2. Öffne die Plex-Weboberfläche und richte den Server mit deinem Plex-Konto ein.
3. Lege eine Bibliothek namens **Filme** mit dem passenden Filmtyp an.
4. Wähle deinen Filmordner aus, im Beispiel `/media/movies`.
5. Lege eine zweite Bibliothek namens **Serien** mit dem passenden Serientyp an und wähle `/media/tv`.
6. Lass Plex die Bibliotheken scannen und die Medien zuordnen.
7. Installiere die Plex-App auf deinem Wiedergabegerät und verbinde dich mit deiner Bibliothek.

```text
Filme  → /media/movies
Serien → /media/tv
```

Verwende die tatsächlichen Pfade deines Servers. Plex durchsucht diese Verzeichnisse und versucht, die Dateien den passenden Filmen und Serien zuzuordnen.

## Die erste Wiedergabe prüfen

Kontrolliere zunächst die erkannten Titel, Cover und Episoden. Starte dann einen Film und eine Serienepisode auf deinem vorgesehenen Client. Prüfe auch die gewünschte Tonspur und Untertitel.

Bei Rucklern lohnt sich ein Blick darauf, ob der Client [Direct Play](../grundlagen/direct-play.md) nutzt oder der Server [transcodiert](../grundlagen/transcoding.md). So kannst du zwischen einem Netzwerkengpass und fehlender Rechenleistung unterscheiden.

Der Remote-Zugriff ist ein eigener Einrichtungsschritt und mit einer funktionierenden lokalen Bibliothek noch nicht automatisch erledigt.

**Weiter:** [Jellyfin](../jellyfin/README.md)
