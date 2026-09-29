# Homeserver und NAS

Ein Homeserver ist ein eigener Server zu Hause. Das kann ein Mini-PC, ein alter Desktop-PC, ein selbstgebauter Rechner oder ein NAS sein. Hardware und Datenträger gehören dir; du kümmerst dich um Einrichtung und Wartung.

## Was ist ein NAS?

**NAS** steht für **Network Attached Storage**, also Speicher, der über das Netzwerk erreichbar ist. Vereinfacht ist ein NAS ein kleiner Server, dessen Hauptaufgabe das Speichern und Bereitstellen von Dateien ist.

Auf vielen NAS-Systemen kann zusätzlich Plex oder Jellyfin laufen. Das Gerät übernimmt dann Speicher und Medienserver zugleich. Ob die gewünschte Software unterstützt wird und genug Leistung bekommt, hängt vom konkreten Gerät ab.

## Speicher und Erweiterbarkeit

Eine **HDD** ist eine mechanische Festplatte. Eine **SSD** speichert Daten auf Speicherchips und arbeitet ohne bewegliche Teile. Beide können Mediendateien speichern.

Ein NAS kann beispielsweise so bestückt sein:

```text
NAS
├── HDD 1: 12 TB
├── HDD 2: 12 TB
├── HDD 3: 12 TB
└── HDD 4: 12 TB
```

Das ergibt 48 Terabyte (TB) an nomineller Rohkapazität. Der tatsächlich nutzbare Speicher hängt unter anderem davon ab, wie die Datenträger eingerichtet sind.

Zusätzliche oder größere Festplatten ermöglichen mehr Speicher, sofern Gehäuse, Anschlüsse und System das unterstützen. Ein Mini-PC ist dabei oft weniger flexibel als ein Gehäuse mit mehreren Laufwerksschächten.

## Netzwerk: lokal und remote

Im Heimnetz sieht der Weg der Mediendaten so aus:

```text
Homeserver / NAS                    Wiedergabegeräte
├── Betriebssystem                       ▲
├── Plex oder Jellyfin                   │
└── Filme und Serien ──► Router/Switch ───┘
```

Ein **Switch** verbindet Geräte innerhalb eines Netzwerks. Ein **Router** verbindet unterschiedliche Netzwerke, etwa dein Heimnetz und das Internet; Heimrouter enthalten häufig auch einen Switch und WLAN.

Beim lokalen Streaming muss der Film nicht erst durch das Internet. Wie flüssig die Wiedergabe läuft, hängt trotzdem von der Netzwerkverbindung ab, etwa von der WLAN-Qualität.

Beim Remote-Streaming kommt der **Upload** deines Internetanschlusses hinzu: die Geschwindigkeit, mit der dein Zuhause Daten ins Internet senden kann. Sie muss für die übertragenen Streams ausreichen. Außerdem muss der externe Zugriff passend eingerichtet sein.

## Strom und Wartung

Auch ohne Servermiete entstehen laufende Kosten. Der Stromverbrauch hängt von Hardware, Anzahl der Laufwerke, Auslastung und Betriebsdauer ab. Ein Gerät, das rund um die Uhr läuft, verbraucht über das Jahr mehr Energie als dasselbe Gerät bei gelegentlicher Nutzung.

Du kümmerst dich um Updates, defekte Datenträger und andere Hardwareprobleme selbst. Bei der Planung zählen deshalb neben dem Kaufpreis auch Betrieb und spätere Ersatzteile.

## Vor- und Nachteile

| Vorteile | Nachteile |
|---|---|
| Eigene Hardware und physische Kontrolle | Anschaffungskosten |
| Kontrolle über Speicher und Ausbau | Erweiterbarkeit durch das Gerät begrenzt |
| Schnelles Streaming im Heimnetz möglich | Eigene Wartung und Stromverbrauch |
| Keine monatliche Servermiete | Remote-Streaming hängt vom eigenen Upload ab |

**Weiter:** [Dedicated Server](dedicated-server.md)
