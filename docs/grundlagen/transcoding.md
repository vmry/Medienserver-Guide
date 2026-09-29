# Transcoding

**Transcoding** bedeutet, dass der Server Bild oder Ton während des Streamings umwandelt. Plex oder Jellyfin kann dadurch Medien an einen Client oder an die verfügbare Verbindung anpassen.

## Warum wird umgewandelt?

Typische Gründe sind ein nicht unterstütztes Video- oder Audioformat, eine niedrigere gewählte Wiedergabequalität oder Untertitel, die in das Bild eingebrannt werden müssen. Dabei werden die Untertitel zu einem festen Teil der Videobilder.

Ein Beispiel für Video-Transcoding:

```text
4K HEVC
   │
   ▼
Server: Video umwandeln
   │
   ▼
1080p H.264
   │
   ▼
Client
```

**HEVC**, auch H.265 genannt, und **H.264** sind Videocodecs. **4K** und **1080p** bezeichnen unterschiedliche Bildauflösungen. Im Beispiel ändert der Server sowohl die Auflösung als auch den Codec.

## Was bedeutet das für die Leistung?

Video-Transcoding benötigt deutlich mehr Rechenleistung als Direct Play. Die Umwandlung muss schnell genug erfolgen, damit die Wiedergabe nicht auf neue Bilder warten muss. Besonders mehrere gleichzeitige 4K-Umwandlungen können schwache Server überfordern.

Nicht immer wird alles umgewandelt: Es kann etwa nur die Tonspur betroffen sein. Der Aufwand hängt von der konkreten Datei, den Einstellungen und dem Client ab. Weitere technische Details findest du in der [Jellyfin-Dokumentation zu Transcoding](https://jellyfin.org/docs/general/post-install/transcoding/).

Für deine Hardwareplanung zählt deshalb nicht nur die Anzahl der Zuschauer, sondern auch, was ihre Geräte direkt wiedergeben können.

**Weiter:** [Hardware-Transcoding](hardware-transcoding.md)
