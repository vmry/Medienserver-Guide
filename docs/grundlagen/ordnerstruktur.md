# Ordnerstruktur

Saubere Ordner und Dateinamen erleichtern Plex und Jellyfin die automatische Erkennung. Trenne Filme und Serien und lege dafür später zwei Bibliotheken an.

Die folgenden Pfade sind Beispiele für ein Linux-System. Auf deinem Server können die Medien an einem anderen Ort liegen. Entscheidend ist, dass Plex oder Jellyfin auf die ausgewählten Ordner zugreifen und die Dateien lesen kann.

## Filme

Verwende pro Film einen Ordner mit Titel und Erscheinungsjahr. Das Jahr hilft, gleichnamige Filme auseinanderzuhalten.

```text
/media/
└── movies/
    ├── Dune (2021)/
    │   └── Dune (2021).mkv
    ├── Interstellar (2014)/
    │   └── Interstellar (2014).mkv
    └── Oppenheimer (2023)/
        └── Oppenheimer (2023).mkv
```

`.mkv` bezeichnet hier den **Container**, also die Dateihülle für Video, Audio und Untertitel. Die Endung allein sagt nicht, mit welchem Codec das Video komprimiert wurde.

## Serien

Lege für jede Serie einen Ordner und darunter eigene Staffelordner an:

```text
/media/
└── tv/
    └── Breaking Bad/
        ├── Season 01/
        │   ├── Breaking Bad - S01E01.mkv
        │   └── Breaking Bad - S01E02.mkv
        └── Season 02/
            ├── Breaking Bad - S02E01.mkv
            └── Breaking Bad - S02E02.mkv
```

`S01E02` bedeutet Staffel 1, Episode 2. Die eindeutige Nummerierung verhindert viele Zuordnungsprobleme.

## Ordner als Bibliotheken hinzufügen

| Bibliothek | Beispielpfad |
|---|---|
| Filme | `/media/movies` |
| Serien | `/media/tv` |

Wähle jeweils den übergeordneten Film- oder Serienordner aus. Nach dem Scan prüfst du, ob Titel und Episoden richtig erkannt wurden. Falsche Zuordnungen lassen sich oft schon durch eindeutigere Dateinamen beheben.

**Weiter:** [Direct Play](direct-play.md)
