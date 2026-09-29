# Hardware-Transcoding

Beim Hardware-Transcoding übernehmen spezialisierte Videoeinheiten die unterstützten Teile der Videoumwandlung. Dadurch muss die **CPU**, also der Hauptprozessor, diese Arbeit nicht vollständig mit ihren allgemeinen Rechenkernen erledigen.

Solche Einheiten können in einem Prozessor oder einer **GPU**, dem Grafikprozessor, stecken. Bei vielen geeigneten Intel-Prozessoren heißt die Technik **Intel Quick Sync Video**.

```text
Videodatei
    │
    ▼
Spezialisierte Videoeinheit
    │
    ▼
Angepasster Stream
```

## Warum ist das relevant?

Wenn mehrere Benutzer gleichzeitig streamen oder häufig Video-Transcoding nötig ist, kann Hardwarebeschleunigung den Prozessor entlasten. Sie sollte deshalb bei der Hardwarewahl berücksichtigt werden. Bei Direct Play ist keine Videoumwandlung nötig, die davon profitieren würde.

Nicht jede CPU oder GPU unterstützt jedes Videoformat. Hardware, Treiber und die Einstellungen des Medienservers müssen zusammenpassen. Die [Jellyfin-Dokumentation zur Hardwarebeschleunigung](https://jellyfin.org/docs/general/post-install/transcoding/hardware-acceleration/) erläutert die Voraussetzungen für unterstützte Geräte.

## Plex und Jellyfin

Beide Programme unterstützen Hardwarebeschleunigung auf geeigneten Systemen. Die Einrichtung hängt vom Betriebssystem und der verfügbaren Hardware ab. Bei Plex gelten zudem Funktions- und gegebenenfalls Abovoraussetzungen; prüfe dafür die [offiziellen Angaben zu Hardware-Accelerated Streaming](https://support.plex.tv/articles/115002178853-using-hardware-accelerated-streaming/).

Damit kennst du die wichtigsten Grundlagen für deine erste Bibliothek. Die nächsten Kapitel beschreiben die Einrichtung der beiden Programme.

**Weiter:** [Plex](../plex/README.md)
