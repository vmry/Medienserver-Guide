# 🎬 Der eigene Medienserver
## Plex, Jellyfin, NAS & Dedicated Server einfach erklärt

> [!NOTE]
> **Hinweis:** Dieser Guide erklärt die technischen Grundlagen rund um private Medienserver und typische Infrastruktur aus der Piracy- und Self-Hosting-Szene. Welche Inhalte du speichern oder abrufen darfst, hängt von deinem Land und der jeweiligen Quelle ab.

---

## 📑 Inhalt

1. [Das Ziel](#1-das-ziel)
2. [So funktioniert ein Medienserver](#2-so-funktioniert-ein-medienserver)
3. [Plex oder Jellyfin?](#3-plex-oder-jellyfin)
4. [Wo soll der Server laufen?](#4-wo-soll-der-server-laufen)
5. [Homeserver & NAS](#5-homeserver--nas)
6. [Dedicated Server](#6-dedicated-server)
7. [NAS vs. Dedicated Server](#7-nas-vs-dedicated-server)
8. [Speicherbedarf](#8-speicherbedarf)
9. [Direct Play](#9-direct-play)
10. [Transcoding](#10-transcoding)
11. [Hardware-Transcoding](#11-hardware-transcoding)
12. [Ordnerstruktur](#12-ordnerstruktur)
13. [Jellyfin einrichten](#13-jellyfin-einrichten)
14. [Plex einrichten](#14-plex-einrichten)
15. [Der fertige Aufbau](#15-der-fertige-aufbau)
16. [Was reicht zum Einstieg?](#16-was-reicht-zum-einstieg)
17. [Kurz zusammengefasst](#17-kurz-zusammengefasst)

---

## 1. Das Ziel

Wer tiefer in die Welt rund um Filme, Serien, Piracy und Self-Hosting eintaucht, stößt schnell auf Begriffe wie **Plex**, **Jellyfin**, **NAS**, **Dedicated Server**, **Transcoding** oder **Direct Play**.

Das Ziel ist simpel: Statt Filme und Serien jedes Mal über Ordner oder einen normalen Videoplayer zu öffnen, baust du dir praktisch deinen **eigenen privaten Streamingdienst**.

Du öffnest auf Fernseher, Smartphone oder PC eine App und bekommst Filmcover, Beschreibungen, Staffeln, Episoden, Wiedergabefortschritt, Untertitel und verschiedene Tonspuren übersichtlich dargestellt.

Genau dafür gibt es **Plex** und **Jellyfin**.

> [!TIP]
> **Kurz gesagt:** Deine Dateien liegen auf einem Server. Plex oder Jellyfin macht daraus eine Oberfläche, die sich wie ein eigener Streamingdienst bedienen lässt.

---


---

## 2. So funktioniert ein Medienserver

```text
SERVER
│
├── Filme
├── Serien
└── Plex / Jellyfin
        │
        ▼
     Netzwerk
        │
        ├── Fernseher
        ├── Smartphone
        ├── Tablet
        └── PC
```

Der Server enthält die eigentlichen Videodateien. Plex oder Jellyfin durchsucht sie und baut daraus eine Medienbibliothek.

Aus:

```text
/Filme/Dune (2021)/Dune (2021).mkv
```

wird beispielsweise ein Eintrag mit Poster, Beschreibung, Erscheinungsjahr, Laufzeit und Besetzung.

---


---

## 3. Plex oder Jellyfin?

Beide Programme machen aus vorhandenen Mediendateien einen persönlichen Streamingdienst.

### 🟠 Plex

Plex ist besonders auf eine einfache Einrichtung und ein großes Client-Ökosystem ausgelegt.

**Vorteile:**

- einfache Einrichtung
- ausgereifte Oberfläche
- sehr viele Apps
- gute Smart-TV-Unterstützung
- Benutzerverwaltung
- Wiedergabeverlauf und „Weiterschauen“
- automatische Metadaten
- Remote-Nutzung möglich

**Nachteile:**

- nicht vollständig Open Source
- stärkere Abhängigkeit vom Plex-Ökosystem
- bestimmte Funktionen oder Nutzungsszenarien können kostenpflichtig sein

### 🟣 Jellyfin

Jellyfin verfolgt einen stärkeren Self-Hosting-Ansatz und ist kostenlos sowie Open Source.

**Vorteile:**

- kostenlos
- Open Source
- komplett selbst gehostet
- hohe Kontrolle
- lokale Benutzerverwaltung
- gut für Linux und Homeserver geeignet

**Nachteile:**

- teilweise technischer einzurichten
- Client-Unterstützung je nach Plattform weniger komfortabel als Plex

### ⚖️ Direktvergleich

| | Plex | Jellyfin |
|---|---|---|
| Einrichtung | sehr einfach | etwas technischer |
| Open Source | Nein | Ja |
| Eigener Server | Ja | Ja |
| Apps | sehr große Auswahl | kleinere Auswahl |
| Anpassbarkeit | mittel | hoch |
| Self-Hosting-Fokus | mittel | sehr hoch |
| Anfängerfreundlichkeit | sehr hoch | hoch |

> [!TIP]
> **Plex:** möglichst wenig konfigurieren und bequem streamen.  
> **Jellyfin:** möglichst viel selbst kontrollieren.

---


---

## 4. Wo soll der Server laufen?

Plex oder Jellyfin müssen auf einem Rechner laufen, der erreichbar ist, wenn du streamen möchtest.

Für einen größeren Medienserver sind zwei Varianten besonders interessant:

| Variante | Einfach erklärt |
|---|---|
| 🏠 **Homeserver / NAS** | Die Hardware und Festplatten stehen bei dir zuhause. |
| 🌐 **Dedicated Server** | Du mietest einen physischen Server in einem Rechenzentrum. |

---


---

## 5. Homeserver & NAS

Die klassische Variante ist ein eigener Server zu Hause.

Das kann ein NAS, Mini-PC, alter Desktop-PC oder selbstgebauter Homeserver sein.

```text
Homeserver / NAS
│
├── Betriebssystem
├── Plex oder Jellyfin
├── HDDs / SSDs
└── Medienbibliothek
        │
        ▼
    Heimnetzwerk
```

Der große Vorteil: **Hardware und Datenträger befinden sich bei dir.**

### Was ist ein NAS?

NAS bedeutet **Network Attached Storage**.

Vereinfacht ist ein NAS ein kleiner Server, dessen Hauptaufgabe die Speicherung und Bereitstellung von Dateien ist.

Beispiel:

```text
NAS
├── HDD 1: 12 TB
├── HDD 2: 12 TB
├── HDD 3: 12 TB
└── HDD 4: 12 TB
```

Auf vielen NAS-Systemen kann zusätzlich Plex oder Jellyfin laufen.

Das Gerät übernimmt damit gleichzeitig:

```text
Speicher + Medienserver
```

### Vorteile

- eigene Hardware
- volle Kontrolle über den Speicher
- sehr schnelles Streaming im Heimnetz
- Speicher durch zusätzliche/größere HDDs erweiterbar
- keine monatliche Servermiete

### Nachteile

- Anschaffungskosten
- Stromverbrauch
- Hardware muss selbst gewartet werden
- Remote-Streaming hängt vom Upload des eigenen Internetanschlusses ab

Im eigenen Netzwerk läuft der Datenverkehr beispielsweise einfach so:

```text
NAS → Switch/Router → Fernseher
```

Für lokales Streaming muss der Film also nicht erst über das Internet übertragen werden.

---


---

## 6. Dedicated Server

Die zweite Möglichkeit ist ein physischer Server in einem Rechenzentrum.

Du mietest dabei Hardware eines Hostinganbieters und administrierst das Betriebssystem selbst.

Typischerweise bekommst du:

- CPU
- RAM
- SSDs oder HDDs
- Netzwerkanbindung
- öffentliche IP-Adresse
- administrativen Zugriff

Auf solchen Systemen läuft häufig Linux.

```text
Dedicated Server
      │
      ├── Linux
      ├── Plex / Jellyfin
      └── Medien
             │
             ▼
          Internet
             │
       ┌─────┼─────┐
       TV    PC   Smartphone
```

### Vorteile

- gute Rechenzentrumsanbindung
- Server läuft unabhängig vom eigenen Zuhause
- kein eigener Hardwarebetrieb zuhause
- für Remote-Zugriffe grundsätzlich praktisch

### Nachteile

- monatliche Kosten
- großer Speicher kann teuer werden
- Hardware gehört dem Anbieter
- Daten befinden sich auf fremder Hardware
- Anbieterbedingungen und geltendes Recht müssen beachtet werden

---


---

## 7. NAS vs. Dedicated Server

| | Homeserver / NAS | Dedicated Server |
|---|---|---|
| Hardware | gehört dir | gemietet |
| Standort | zuhause | Rechenzentrum |
| Anfangskosten | höher | meist niedriger |
| laufende Kosten | Strom | Servermiete |
| Speicher | selbst erweiterbar | abhängig vom Anbieter |
| lokales Streaming | hervorragend | über Internet |
| Remote-Streaming | abhängig vom eigenen Upload | meist gute Anbindung |
| physische Kontrolle | hoch | gering |
| Hardwarewartung | selbst | Anbieter |

Für eine große langfristige Sammlung ist ein Homeserver/NAS häufig attraktiv.

Wer ohnehin Infrastruktur in einem Rechenzentrum betreibt, kann Plex oder Jellyfin auch dort hosten.

---


---

## 8. Speicherbedarf

Der Speicherbedarf wird schnell unterschätzt.

Beispiel:

```text
500 Filme × durchschnittlich 15 GB
= 7.500 GB
= ungefähr 7,5 TB
```

Dazu kommen Serien, die mit vielen Staffeln ebenfalls mehrere hundert Gigabyte belegen können.

Die Dateigröße hängt unter anderem von folgenden Faktoren ab:

- Auflösung
- Codec
- Bitrate
- HDR
- Bildrate
- Audiospuren
- Untertitel

Derselbe Film kann deshalb beispielsweise einmal 8 GB und in einer hochwertigeren 4K-Fassung 60 GB groß sein.

---


---

## 9. Direct Play

**Direct Play** bedeutet, dass der Client die vorhandene Mediendatei direkt wiedergeben kann.

```text
Filmdatei
   │
   ▼
Server
   │
   │ unverändert
   ▼
Client
```

Das ist der Idealfall.

> [!TIP]
> **Merksatz:** Direct Play = Datei wird praktisch unverändert abgespielt.

Der Server muss das Video nicht neu berechnen und benötigt entsprechend wenig Rechenleistung.

---


---

## 10. Transcoding

Kann ein Wiedergabegerät die vorhandene Datei nicht direkt abspielen, kann Plex oder Jellyfin das Video während der Wiedergabe umwandeln.

Das nennt man **Transcoding**.

```text
4K HEVC
   │
   ▼
SERVER
   │
   │ Transcoding
   ▼
1080p H.264
   │
   ▼
Client
```

> [!IMPORTANT]
> **Merksatz:** Transcoding = der Server muss das Video während des Streamings umwandeln.

Transcoding benötigt deutlich mehr Rechenleistung als Direct Play.

Besonders mehrere gleichzeitige 4K-Transcodes können schwache Server schnell überfordern.

---


---

## 11. Hardware-Transcoding

Statt sämtliche Videokonvertierung über die normale CPU auszuführen, können geeignete Prozessoren oder GPUs bestimmte Videoformate hardwarebeschleunigt verarbeiten.

Bei vielen Intel-Prozessoren steht dafür beispielsweise **Intel Quick Sync Video** zur Verfügung.

```text
Videodatei
    │
    ▼
Hardware Video Engine
    │
    ▼
angepasster Stream
```

Wenn mehrere Benutzer gleichzeitig streamen oder häufig Transcoding notwendig ist, sollte dieser Punkt bei der Hardwarewahl berücksichtigt werden.

---


---

## 12. Ordnerstruktur

Eine saubere Bibliothek erleichtert Plex und Jellyfin die automatische Erkennung.

### Filme

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

### Serien

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

Saubere Dateinamen und Staffelstrukturen vermeiden später viele Probleme bei der Zuordnung.

---


---

## 13. Jellyfin einrichten

Die genaue Installation hängt vom verwendeten System ab. Der grundsätzliche Ablauf bleibt aber gleich:

1. **Jellyfin Server installieren**
2. **Weboberfläche öffnen**
3. **Benutzer anlegen**
4. **Film- und Serienordner hinzufügen**
5. **Bibliothek scannen lassen**
6. **Jellyfin-App auf dem Wiedergabegerät installieren**

Im lokalen Netzwerk ist die Weboberfläche standardmäßig typischerweise über Port `8096` erreichbar:

```text
http://SERVER-IP:8096
```

### Beispiel für die Bibliotheken

```text
Name: Filme
Typ: Movies
Ordner: /media/movies
```

und:

```text
Name: Serien
Typ: Shows
Ordner: /media/tv
```

Jellyfin scannt die Ordner und erstellt daraus die Bibliothek.

---


---

## 14. Plex einrichten

Das Grundprinzip bei Plex ist ähnlich:

1. **Plex Media Server installieren**
2. **Server mit Plex einrichten**
3. **Bibliothek „Filme“ anlegen**
4. **Bibliothek „Serien“ anlegen**
5. **Medienordner auswählen**
6. **Bibliothek scannen lassen**
7. **Plex-App auf dem Wiedergabegerät installieren**

```text
Filme  → /media/movies
Serien → /media/tv
```

Plex durchsucht anschließend die Verzeichnisse und versucht, Dateien automatisch den passenden Filmen und Serien zuzuordnen.

Der wesentliche Unterschied zu Jellyfin liegt daher weniger in der Bibliotheksstruktur als im Ökosystem, den Clients, der Benutzerverwaltung und der Frage, wie stark du auf einen externen Anbieter setzen möchtest.

---


---

## 15. Der fertige Aufbau

### 🏠 Homeserver

```text
                    INTERNET
                       │
                    ROUTER
                       │
                 ┌─────┴─────┐
                 │           │
              SERVER       Clients
                 │
          Plex/Jellyfin
                 │
        ┌────────┴────────┐
        │                 │
      Filme             Serien
```

### 🌐 Dedicated Server

```text
               RECHENZENTRUM
                     │
              Dedicated Server
                     │
              Plex/Jellyfin
                     │
              Medienbibliothek
                     │
                  Internet
                     │
          ┌──────────┼──────────┐
          │          │          │
          TV        PC      Smartphone
```

Plex beziehungsweise Jellyfin bildet dabei die Schicht zwischen den gespeicherten Dateien und den Wiedergabegeräten.

---


---

## 16. Was reicht zum Einstieg?

Für einen einfachen Medienserver brauchst du im Kern nur:

```text
Server
+
Speicher
+
Plex oder Jellyfin
+
Client
```

Du brauchst nicht sofort ein Rack voller Server oder dutzende Festplatten.

Ein kleiner Homeserver kann bereits ausreichen. Entscheidend ist zunächst, die einzelnen Komponenten und ihre Aufgaben zu verstehen.

Später kann das System schrittweise erweitert werden.

---


---

## 17. Kurz zusammengefasst

Die grundlegende Architektur ist simpel:

```text
Medien
   │
   ▼
Speicher
   │
   ▼
Plex / Jellyfin
   │
   ▼
Netzwerk / Internet
   │
   ▼
Client
```

**Plex** ist besonders interessant, wenn Komfort, breite Geräteunterstützung und eine möglichst einfache Einrichtung wichtig sind.

**Jellyfin** ist besonders interessant, wenn Open Source, Self-Hosting und möglichst viel eigene Kontrolle im Vordergrund stehen.

Als Hardware kann entweder ein **Homeserver/NAS** oder ein **Dedicated Server** im Rechenzentrum dienen.

Damit steht das Fundament des eigenen Medienservers.
