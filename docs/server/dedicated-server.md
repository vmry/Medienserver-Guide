# Dedicated Server

Ein **Dedicated Server** ist ein physischer Rechner, den du vollständig bei einem Hostinganbieter mietest. Er steht in einem Rechenzentrum. Der Anbieter betreibt die Hardware; bei der hier beschriebenen Variante verwaltest du das Betriebssystem und deine Anwendungen selbst.

## Was du mietest

Typischerweise gehören dazu:

- **CPU:** der Prozessor, der Berechnungen ausführt.
- **RAM:** der Arbeitsspeicher für laufende Programme.
- **HDDs oder SSDs:** Datenträger für Betriebssystem und Medien.
- **Netzwerkanbindung:** die Verbindung des Servers zum Internet.
- **Öffentliche IP-Adresse:** eine Adresse, über die der Server im Internet erreichbar sein kann.
- **Administrativer Zugriff:** die Berechtigung, Software zu installieren und das System zu verwalten.

Auf solchen Servern läuft häufig **Linux**, eine Familie von Betriebssystemen. Plex oder Jellyfin bildet auch hier die Verbindung zwischen deinen Dateien und den Wiedergabegeräten.

```text
Rechenzentrum
└── Dedicated Server
    ├── Betriebssystem, häufig Linux
    ├── Plex oder Jellyfin
    └── Medienbibliothek
              │
              ▼
           Internet
              │
       ┌──────┼───────────┐
       TV     PC     Smartphone
```

## Netzwerk, Speicher und Kosten

Eine Rechenzentrumsanbindung kann für Remote-Streaming praktisch sein. Die tatsächlich verfügbare Geschwindigkeit und mögliche Grenzen für das übertragene Datenvolumen hängen vom Vertrag ab. Auch der Internetanschluss des Wiedergabegeräts muss schnell genug sein.

Du zahlst eine laufende Servermiete. Viel Speicher kann die Kosten deutlich erhöhen. Zusätzliche Datenträger oder andere Hardware bekommst du nur im Rahmen der Möglichkeiten des Anbieters; gegebenenfalls ist ein Wechsel auf einen anderen Server nötig.

Die Hardware gehört dem Anbieter, und deine Dateien liegen auf fremden Datenträgern. Du musst seine Nutzungsbedingungen und das geltende Recht beachten.

## Vor- und Nachteile

| Vorteile | Nachteile |
|---|---|
| Gute Rechenzentrumsanbindung möglich | Monatliche Miete |
| Betrieb unabhängig von Strom und Internet zu Hause | Großer Speicher kann teuer werden |
| Keine eigene Hardware zu Hause betreiben | Keine direkte physische Kontrolle |
| Für Remote-Zugriffe praktisch | Daten liegen auf fremder Hardware |
| Hardwarewartung durch den Anbieter | Betriebssystem und Anwendungen selbst verwalten |

**Weiter:** [Homeserver oder Dedicated Server?](vergleich.md)
