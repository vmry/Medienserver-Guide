# Jellyfin einrichten

Die genaue Installation hängt von deinem Betriebssystem und deiner Hardware ab. Der folgende Ablauf beschreibt die grundlegende Einrichtung bis zur ersten Wiedergabe.

## Vorbereitung und Weboberfläche

Lege deine Medien in getrennten [Film- und Serienordnern](../grundlagen/ordnerstruktur.md) ab. Der Jellyfin-Server muss diese Ordner und Dateien lesen können.

Nach der Installation erreichst du die Weboberfläche im lokalen Netzwerk standardmäßig über:

```text
http://SERVER-IP:8096
```

Ersetze `SERVER-IP` durch die lokale IP-Adresse deines Servers. Eine **IP-Adresse** ist die Netzwerkadresse eines Geräts. Der **Port** `8096` bezeichnet hier den Zugang zum Webdienst auf diesem Gerät. Er kann in deiner Installation abweichen; siehe die [offizielle Netzwerkdokumentation](https://jellyfin.org/docs/general/post-install/networking/).

Diese HTTP-Adresse ist für den lokalen Einstieg gedacht. Eine abgesicherte Remote-Einrichtung ist damit noch nicht erledigt.

## Einrichtung Schritt für Schritt

1. Installiere **Jellyfin Server** in der zu deinem System passenden Version.
2. Öffne die Weboberfläche im Browser.
3. Lege im Einrichtungsassistenten deinen Benutzer mit einem Passwort an.
4. Füge eine Filmbibliothek und eine Serienbibliothek mit den zugehörigen Medienordnern hinzu.
5. Lass Jellyfin die Ordner scannen und die Bibliotheken aufbauen.
6. Installiere eine passende Jellyfin-App auf deinem Wiedergabegerät und verbinde sie mit deinem Server.

## Beispiel für die Bibliotheken

| Name | Inhaltstyp | Beispielordner |
|---|---|---|
| Filme | Filme / Movies | `/media/movies` |
| Serien | Serien / Shows | `/media/tv` |

Die Bezeichnungen können je nach Oberflächensprache abweichen. Verwende die tatsächlichen Ordner deines Servers.

## Die erste Wiedergabe prüfen

Kontrolliere nach dem Scan, ob Titel, Staffeln und Episoden richtig erkannt wurden. Spiele dann einen Film und eine Serienepisode auf deinem Client ab. Teste auch Tonspuren und Untertitel.

Falls die Wiedergabe stockt, prüfe die Netzwerkverbindung und ob gerade [Transcoding](../grundlagen/transcoding.md) nötig ist. Eine funktionierende erste Bibliothek ist die Grundlage, auf der du Speicher und Nutzung später schrittweise erweitern kannst.
