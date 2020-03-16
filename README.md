# ModerneSoftwareArchitektur
Repository für moderne Softwarearchitektur

# Inhaltsverzeichnis
1) [Requirements](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/README.md#1-requirements)
2) [Domäne](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/README.md#2-dom%C3%A4ne)
3) [Software Qualitätsattribute](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#3-software-qualit%C3%A4tsattribute)
4) [Softwarearchitektur Design](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#4-softwarearchitektur-design)
5) [Software Entwicklung Prinzipien und Praktiken](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#5-software-entwicklung-prinzipien-und-praktiken)
6) [Softwarearchitektur Patterns](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#6-softwarearchitektur-patterns)
7) [Moderne Architekturen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#7-moderne-architekturen)
8) [Performance](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#8-performance)
9) [Security](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#9-security)
10) [Dokumentation](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#10-dokumentation)
11) [DevOps und Softwarearchitektur](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#11-devops-und-softwarearchitektur)
12) [Die Skills eines Softwarearchitekten](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#12-die-skills-eines-softwarearchitekten)
13) [Evolutionäre Architekturen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#13-evolution%C3%A4re-architekturen)
14) [Wie werde ich ein guter Softwarearchitekt](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#14-wie-werde-ich-ein-guter-softwarearchitekt)
15) [Architektur und Legacy Applications](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#15-architektur-und-legacy-applications)


## 1) Requirements
**Requirement Engineering**

### Kernkompetenzen des Online-shoppens:

Wie ist ihr derzeitiges Einkaufsverhalten?
*- Produkt, dass gekauft werden soll in Werbekatalogen suchen, die per Post geschickt wurden. Dann in einen Laden in der nähe gehen und mit Bargeld bezahlen.*

Wo sind die größten Probleme im derzeitigem Kaufverhalten?
*- Die physische Distanz zum Geschäft ist groß.
- Die Produktauswahl dauert lange.
- Die öffnungszeiten sind ein Problem.*

Finden Sie spezielle Produkte auf Anhieb im Geschäft?
*- Nein, nicht in jedem, vorallem Abends nicht, wenn alles ausverkauft ist.*

Welche Produkte würden Sie eher nicht online kaufen?
*- Dinge, die getestet werden müssen wie Kleidung, oder Dinge, die in echt gesehen werden müssen. Diese würden lokal gekauft.*

Könnten Sie sich vortstellen Bücher oder Büromaterial online zu kaufen mit Lieferung nach Hause?
*- Ja.*

Würden Sie dafür eine Liefergebühr bezahlen?
*- Ja. Aber wenn es lokal verfügbar ist und billiger würde ich es eher lokal kaufen.*

Was wäre, wenn Amazon Ihnen gewährleistet, dass ein Produkt verfügbar ist und innerhalb von 1-2 Werktagen zu Hause ist?
*- Dann wäre ein Onlinekauf vorstellbar.*

### Vorstellungen zur Plattform:

Wie würden Sie sich vorstellen ein Buch zu kaufen?
*- Eingabe in einer Leiste zum suchen. Dann wird das Buch angezeigt. Dann kann es gekauft werden.*

Würden Sie nach der Nutzun des Dienstes eine Bewertung abgeben?
*- Ja, wenn eine Errinnerung dafür kommt.*

Wie soll der Bezahlvorgang aussehen?
*- Frage nach der Kreditkarte, oder bezahlen mit PayPal, Vorkasse oder per SEPA.*

Würden sie für eine zusätzliche Dienstleistung, dass ein Produkt schneller kommt, bezahlen?
*- Ja, wenn es garantiert ist.*

Wie viel Geld würden Sie maximal dafür ausgeben pro Jahr?
*- 50 bis 60 Euro*
 
Wie stellen sich die Suche vor?
*- Es soll nach Kategorien und relevanten Ergebnissen gefiltert werden können. Relevante Ergebnisse sollen angezeigt werden.*

Gibt es noch weitere Suchfilter, die Sie gerne hätten?
*- Filtern nach Preis, Produktspezisischen Eigenschaften, Marke, Sprache, Bewertung, ISBN soll möglich sein.+

Weitere Punkte:
*Bestellungen sollen in Historie angezeigt werden, Retouren sollen einfach sein, Lieferverfolgunng, Stornierung, hohe Kulanz*

### Functional Requirements:
- 1 Sekunde pro Aufruf maximal
- Globale schnelle Verfügbarkeit
- Hohe Verfügbarkeit
- Mobile Erreichbarkeit
- Kauf mit Account und als Gast
- Account soll Adressen und Bezahlinformationen speichern können
- Bestellhistorie soll sichtar sein
- Interfaces zu Post, DHL, Verkäufern und deren Systemen (Oberflächen), zum Kunden

### Business Requirements:
- Traditionellen Einzelhandel ersetzen
- Probleme: Verfügbarkeit, Wartezeit, Anreisezeit, etc.
- Schaffen einer Online Plattform um diese Zeiten zu verkürzen und Verfügbarkeit zu erhöhen
- Ähnlichkeiten: Verkauf von Produkten
- Abgrenzung: Abwicklung des Kaufvorgangs online, Lieferung
- Anforderung vom Markt: Einfacherer Kauf als im klassischen Einzelhandel

## 2) Domäne
## 3) Software Qualitätsattribute
## 4) Softwarearchitektur Design
## 5) Software Entwicklung Prinzipien und Praktiken
## 6) Softwarearchitektur Patterns
## 7) Moderne Architekturen
## 8) Performance
## 9) Security
### Abwehren von Angriffen:
- Bruteforce Angriffe auf Login durch maximale Versuche berenzen
- Authentifizierung des Users über Passwort / 2 Faktor Authentifizierung
- Verschlüsselte Verbindungen zwischen User und Server
- Sicherstellen, dass persönliche Daten nicht nach außen dringen

### Sicherheit im Ruhezustand:
- Persistenz der Daten
- Sichern des RAMs, wenn System neu gestartet wird
- Daten dürfen sich nicht ändern, wenn System im Ruhezustand

### Sicherheit bei Gebrauch:
- Zugriffsbeschränkungen
- Veränderungen durch unberechtigte verhindern, um Integrität zu schützen

### Sicherheit bei Transport:
- Daten müssen auf vollständigkeit überprüft werden (z.B. durch Checksummen \[stellen auch Integrität sicher\])

### Vermeiden, dass dritte Zugang zu Daten bekommen:
-> Verschlüsselte Kommunikation
-> Sichere Passwörter (mindest Länge)

### Integrität:
-> Daten dürfen nur verändert werden, wenn eine Authentifizierung stattfindet
(z.B. OAuth Token)

### Wertvolle Teile der Architektur:
- Nutzerdaten
- Zahlungsinformationen
- Transaktionsmodule
- Logistikmodule

### Potentielle Bedrohungen:
- Angriffe über die Webseite
  - Bruteforce
  - Login
- Phishing Mails um Kundendaten zu erlangen
- SQL Injections
- Denial of Service (Dos / DDos)
- Man in the middle Angriffe -> Spoofing/Tampering
- Login als Administrator

### Potentieller Schaden daraus:
- Verlust von Daten
- Image Schaden
- Verlust von Vertrauen der Kunden
- Wirtschaftlicher Schaden
- Zerstörung von Infrastruktur

### Klassifizierung der Bedrohungen:
**Schadenshöhen:**

Hoch
- Verlust von Kundendaten
- Verlust von Zahlungsinformationen
- Man in the middle
- Login als Administrator
 
Mittel
- Imageschaden
- Zerstörung von nicht kritischer Infrastruktur
- Denial of Service

Niedrig
- Verlust von nicht relevanten Daten
- Phishing mails

**Reproduzierbarkeit:**

Hoch
- Phishing mails
- Denial of Service

Mittel
- Man in the middle
- Zerstörung kritischer Infrastruktur
- Login als Administrator

Niedrig

**Nachvollziehbarkeit:**

Hoch

Mittel

Niedrig

**Affected User:**

Hoch
- Denial of Service
- Verlust von Kundendaten
- Verlust von Zahlungsinformationen

Mittel
- SQL Injections

Niedrig
- Verlust nicht relevanter Daten

**Grad der Erkennbarkeit**

Hoch
- Phishing
- Dos/DDos

Mittel
- Login als Administrator
- SQL Injections

Niedrig
- Man in the middle

### Secure by Design:
- Keine Logins für Administrator von außen
- Nutzereingaben werden auf Injections geprüft
- Firewalls nutzen
- Dos/DDos Erkennung mit Firewall etc
- Alle Schutzmaßnahmen sind normalerweise an
- Nutzer bekommen nur Zugriff auf die Dinge, die sie brauchen
- Weniger Schnittstellen, die standartisiert sind und alle gesichert sind
- Hohe Fehlertoleranz => Keine Fehler nach a geben um Entdecken von Problemen zu verhindern -> Meldung an Administrator
- Passwortschutz

### Kryptografie:
- Nutzen von SSL/HTTPS für kommunikation mit Browser
-> Umleiten von HTTP zu HTTPS
- Passwörter gehasht speichern
- Datenbanken und Daten verschlüsseln
- Authentifizierung mittels Key / Tokens für interne Arbeiten

### Identity und Access Management:
- Verifizeirung der nutzer und des Servers mittels Zertifikaten
- OAuth Token
- Keys
- Signaturen (z.B. PGP)

Um eine gute Sicherheit zu gewährleisten sollten Pakete aktualisiert werden,
Server Wartungen durchgeführt werden, Logs angelegt werden und regelmäßig geprüft werden.
Honeypots können genutzt werden um von Angreifern zu lernen.

## 10) Dokumentation
## 11) DevOps und Softwarearchitektur
## 12) Die Skills eines Softwarearchitekten
## 13) Evolutionäre Architekturen
## 14) Wie werde ich ein guter Softwarearchitekt
## 15) Architektur und Legacy Applications
