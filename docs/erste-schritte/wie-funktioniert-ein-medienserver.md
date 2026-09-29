# Wie funktioniert ein Medienserver?

Die eigentlichen Videodateien liegen auf dem Speicher des Servers. Plex oder Jellyfin durchsucht die ausgewählten Ordner und baut daraus eine **Medienbibliothek**: eine übersichtliche Sammlung mit Zusatzinformationen zu jedem Film und jeder Serie.

```text
Server
├── Speicher mit Filmen und Serien
└── Plex oder Jellyfin
         │
         ▼
   Netzwerk / Internet
         │
         ├── Fernseher
         ├── Smartphone
         ├── Tablet
         └── PC
```

Plex oder Jellyfin vermittelt zwischen deinen gespeicherten Dateien und den Clients. Die Programme bringen dabei keine eigene Film- und Seriensammlung für deine persönliche Bibliothek mit: Du fügst die vorhandenen Medienordner hinzu.

## Von der Datei zum Bibliothekseintrag

Aus dieser Datei:

```text
/media/movies/Dune (2021)/Dune (2021).mkv
```

wird beispielsweise ein Eintrag mit Poster, Beschreibung, Erscheinungsjahr, Laufzeit und Besetzung. Solche Zusatzinformationen heißen **Metadaten**. Saubere Dateinamen helfen der Software, den richtigen Titel zu erkennen.

Wenn du einen Film startest, sendet der Server die Mediendaten an den Client. Kann der Client das Format abspielen, ist kaum zusätzliche Rechenarbeit nötig. Andernfalls muss der Server Bild oder Ton möglicherweise umwandeln. Das erklären später die Kapitel zu [Direct Play](../grundlagen/direct-play.md) und [Transcoding](../grundlagen/transcoding.md).

## Zu Hause und unterwegs

Beim lokalen Streaming von einem Homeserver bleiben die Mediendaten im Heimnetz. **Remote-Streaming** bedeutet, dass du von außerhalb auf deinen Server zugreifst, etwa unterwegs mit dem Smartphone. Dann werden die Mediendaten über das Internet übertragen.

Ein Server im Rechenzentrum liefert dir die Medien ebenfalls über das Internet, auch wenn du zu Hause auf dem Sofa schaust.

**Weiter:** [Plex oder Jellyfin?](plex-oder-jellyfin.md)
