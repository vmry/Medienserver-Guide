# Speicherbedarf

Eine Medienbibliothek wächst schnell. Plex und Jellyfin verwalten deine Dateien, verkleinern aber nicht automatisch deine Sammlung. Plane deshalb den Platz für die vorhandenen Medien und künftige Ergänzungen ein.

## Ein einfaches Rechenbeispiel

```text
500 Filme × durchschnittlich 15 GB
= 7.500 GB
= ungefähr 7,5 TB
```

**GB** steht für Gigabyte, **TB** für Terabyte. In dieser dezimalen Rechnung entsprechen 1.000 GB einem TB. Programme können Kapazitäten anders anzeigen, wenn sie binäre Einheiten verwenden.

Dazu kommen Serien: Viele Staffeln können zusammen mehrere hundert Gigabyte belegen. Auch Bibliotheksdaten, Bilder und gegebenenfalls temporäre Dateien beim [Transcoding](transcoding.md) brauchen Platz. Plane den Speicher deshalb nicht bis zum letzten Gigabyte voll.

## Warum Dateigrößen so unterschiedlich sind

| Begriff | Bedeutung |
|---|---|
| Laufzeit | Je länger ein Video bei gleicher Bitrate ist, desto größer wird es. |
| Auflösung | Anzahl der Bildpunkte, etwa 1080p oder 4K. Mehr Bildpunkte können mehr Daten benötigen. |
| Codec | Verfahren zum Kodieren und Dekodieren, also zum Komprimieren und Wiedergeben von Bild oder Ton. |
| Bitrate | Datenmenge pro Sekunde. Bei gleicher Laufzeit bedeutet eine höhere Gesamtbitrate eine größere Datei. |
| HDR | High Dynamic Range: ein größerer Helligkeitsumfang. HDR kann mit anderen Formaten und Kodierungseinstellungen einhergehen. |
| Bildrate | Anzahl der Bilder pro Sekunde. |
| Audiospuren | Zusätzliche Sprachen oder Tonformate belegen weiteren Speicher. |
| Untertitel | Zusätzliche Text- oder Bildspuren; ihr Platzbedarf ist meist klein im Vergleich zum Video. |

Derselbe Film kann beispielsweise als kleinere Fassung 8 GB und als hochwertige 4K-Fassung 60 GB groß sein. Das sind Beispiele, keine festen Größen pro Auflösung. Entscheidend sind Laufzeit und die tatsächliche Bitrate aller enthaltenen Spuren.

**Weiter:** [Ordnerstruktur](ordnerstruktur.md)
