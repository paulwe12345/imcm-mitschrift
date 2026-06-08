# IMCM-Mitschrift

Das ist die README.md-Datei. med steht für Markdown. Markdown ist eine im Internet weit verbreitete Auszeichnungssprache (*Markup-Language*)

- HTML (Hypertext Markup Language)
- XML (Extensible Markup Language)
- YAML, YML (Yet Another Markup Language) 

## Playlist zur Funktionsweise des Internets

### Teil 1 - What is the Internet?

- wurde in den 1970er-Jahren erfunden
- Motivation: schaffung eines dezentralen Netzwerks das auch noch nach einem Atomschlag noch funktioniert (Kontext des Kalten Krieges)
- Funktionsweise: Paketvermittlung (*Packet Switching*) - jedes Datenpaket sucht sich eine eigene Route durch das Netzwerk
- Internet: das Netz der Netze - besteht aus vielen kleinen Netzen unterschiedlicher Internetanbietern (*Internet Service Provider - ISP*, z.B.: A1, Magenta, Salzburg AG, ...)

### Teil 2 - The Internet: Wires, Cables & Wifi

- Informationen werden im Internet als Bits übertrage.
- Bits haben zwei Werte: 0 oder 1. 
- 8 Bits ergeben 1 Byte. Mit einem Byte kann man 256 verschiedene Werte speichern (2^8).

- Bits können über verschiedene Übertragungsmedien zwischen Computern versendt werden.
- Die Anzahl der Übertragenen Bits pro Sekunde wird als Bandbreite bezeichnet - z.b.: 300MBit/s -> 300 Millionen Bit können pro Sekunde über diese Leitung laufen.
- Die zwei Hauptübertrager sind :

1. Kupfer / Elektrizität
    - billig
    - einfache Verarbeitung
    - weit verbreitet
    - hohe Verluste über lange Distanzen (hunderte Meter)


2. Glasfaser / Licht
    - teuer
    - schwierige Verarbeitung
    - schnelle Übertragung
    - verlustfrei
    - geeignet für Ozeankabel

3. Funk / Radiowellen
    - hoher Komfort, Internet überall
    - hohe Verluste über Distanzen

### Teil 3 - The Internet: IP-Adressen & DNS
- Protokolle sind die Regeln der Kommunikation
- eines der wichtigsten Protokolle im Internet ist das Internet Protocol (IP) 
- jedes Gerät im Internet hat zumindestens eine (eindeutige) IP-Adresse, viele Geräte haben aber eine externe IP (ähnlich wie Hausnummern) und eine Interne IP (ähnlich wie die Raumnummern)
- das Domain Name System (DNS) übersetzt menschenlesbare Domainnamen (z.b.: www.google.com) in IP-Adressen
- DNS-Server führen Tabellen mit Domainnamen und den entsprechenden IP-Adressen

### Teil 4 - The Internet: Packets, Routing and Reliability
- Daten die über das Internet versendet werden werden in Pakete aufgeteilt
- Packete sind in der regel 1500 Byte groß (=1.5KB). Das heißt ein 10MB großes Bild würde in 6667 Pakete aufgeteilt werden (10MB = 10.000KB = 10.000.000 Byte / 1500 Byte = 6667 Pakete)
- Pakete können unterschiedliche Routen durch das Internet nehmen. Die Routenplanung erfolgt spezielle Computer sogenante Router. Die Router entscheiden welche Route die Pakete nehmen sollen, basierend auf der auslastung verschiedener Routen, der Entfernung zum Ziel und anderen Faktoren.
- jedes Paket enthält die IP-Adressen der Quelle und des Ziels, sowie die Reihenfolge der Pakete (damit sie am Ziel wieder in der richtigen Reihenfolge zusammengesetzt werden können)
- am Ziel wird die vollständigkeit der Pakete durch das *Transmission Control Protocol* (TCP) überprüft. Wenn Pakete verloren gehen fordert TCP die erneute Übertragung an. TCP sorgt auch dafür, dass die Pakete in der richtigen Reihenfolge zusammengesetzt werden. 
- TCP und IP bilden gemeinsam die Basis für die Funktionsweise des Internets - man spricht auch von TCP/IP-Modell
### Teil 5 - The Internet: HTTP, HTML

- das *Hypertext Transfer Protocol* (HTTP) ist das Protokoll für die Übertragung von Webseiten
- der ablauf ist immer wie folgt: 
    1. der Browser sendet eine HTTP-Anfrage an den Web-Server
    2. der Web-Server verarbeitet die Anfrage und sendet eine HTTP-Antwort zurück. Dabei versieht er die Antwort mit einem [HTTP-Statuscode].
     #### HTTP-Statuscode-Klassen
    > - 1xx: die Anfrage wird verarbeitet
    > - 2xx: die Anfrage wurde erfolgreich verarbeitet
    > - 3xx: die Anfrage wurde umgeleitet
    > - 4xx: Client-Error: fehler auf der Seite des Clients (z.b. 404 - Seite nicht gefunden)
    > - 5xx: Server-Error: fehler auf der Seite des Servers

<br>    

- Daten werden mittels GET-Anfragen angefordert
- User-Inputs werden mittels POST-Anfragen verschlüsselt übermittelt
- GET und Post sind sogenannte *HTTP-Methoden*. Es gibt noch weitere Methoden die wir erst später kennenlernen.
- HTTP-Anfragen können auch **Cookies** enthalten. Das sind kleine Textdateien, die aus Schlüssel-Wert-Paaren (*key-value-pairs*) bestehen. Ist ein Cookie einmal gesetzt, wird es bei jeder weiteren Anfrage an den selben Server automatisch mitgesendet. So kann der Server den Nutzer wiedererkennen.

### Teil 8 - The Internet: How Search Works
- Suchmaschienen-Bots (*Crawler*) durchsuchen das Internet regelmäßig nach neuen Webseiten und aktualisieren die Informationen über bestehende Webseiten. Sie katalogisieren die Informationen der Websites. Der Katalog wird auch *Index* genannt.
- Wenn wir einen Suchbegriff bei Google oder einer anderen Suchmaschine eingeben, wird nicht das WWW durchsucht, sondern der Index.
- Suchergebnisse werden auf Basis eines "geheimen" Algorithmus geranked - Ergebnisse die weiter oben stehten werden öfter angeklickt als Ergebnisse die weiter unten stehen. Daher ist es wichtig möglichst weit oben in den Suchergebnissen zu stehen.
- Einfluss auf das Ranking haben unter anderem: 
    - die Häufigkeit von bestimmten Schlüsselwörtern auf der Webseite (*Keywords*)
    - die Anzahl der Links die auf die Webseite verweisen (*Backlinks*)
    - Wie viele Nutzer auf eine Website klicken.

- die Suchergebnisse werden an die Benutzer*innen angepasst! Das heißt, nicht jeder sieht die gleichen Informationen, selbst wenn sie idente Suchanfragen durchführen.
- [Startpage] (https://www.startpage.com/) ist eine datensparsame Suchmaschine, die ihren Benutzer*innen die Verwendung von Google ohne Tracking oder Personalisierung erlaubt.
