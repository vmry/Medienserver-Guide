# Direct Play

**Direct Play** bedeutet, dass der Client die vorhandene Mediendatei unverändert wiedergeben kann. Plex oder Jellyfin liefert die Daten aus, ohne das Video neu zu berechnen.

```text
Filmdatei → Server → unveränderte Mediendaten → Client
```

Das ist der günstigste Fall für die Serverleistung: Der Client übernimmt die Wiedergabe, und der Server benötigt vergleichsweise wenig Rechenleistung.

## Wann funktioniert das?

Der Client muss mit Container, Video- und Audioformat sowie den ausgewählten Untertiteln umgehen können. Außerdem muss die Verbindung genügend **Bandbreite**, also Übertragungskapazität, für die Datei bieten. Das Zusammenspiel dieser Faktoren beschreibt auch die [Plex-Übersicht zur Wiedergabe](https://support.plex.tv/articles/200430303-streaming-overview/).

Eine kompatible App kann deshalb für die Wiedergabe genauso wichtig sein wie der Server. Direct Play spart Rechenarbeit, reduziert aber nicht die zu übertragende Datenmenge. Ein schwaches WLAN oder ein zu geringer Upload kann weiterhin zu Unterbrechungen führen.

## Wenn Direct Play nicht möglich ist

Nicht jede Anpassung bedeutet, dass das Video vollständig neu berechnet werden muss. Manchmal genügt es, die vorhandenen Spuren anders zu verpacken. Muss dagegen Bild oder Ton neu kodiert werden, handelt es sich um Transcoding.

**Weiter:** [Transcoding](transcoding.md)
