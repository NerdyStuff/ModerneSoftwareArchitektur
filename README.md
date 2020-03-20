# Moderne Softwarearchitektur
Repository für moderne Softwarearchitektur

# Inhaltsverzeichnis
1) [Requirements](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/README.md#1-requirements)<br>
1.1) Kernkompetenzen des Online-shoppens<br>
1.2) Vorstellungen zur Plattform<br>
1.3) Functional Requirements<br>
1.4) Non-Functional Requirements<br>
1.5) Business Requirements<br>
1.6) Constraints<br>
2) [Domänen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/README.md#2-dom%C3%A4ne)<br>
2.1) Shopoberfläche<br>
2.2) CRM + Kundenverwaltung<br>
2.3) Produktempfehlungssystem<br>
2.4) Zahlungssystem<br>
2.5) Buchhaltung<br>
2.6) Versand<br>
2.6.1) Versanddienstleister<br>
2.7) Lager<br>
2.8) Produktekatalog<br>
2.8.1) Anbieter<br>
3) [Software Qualitätsattribute](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#3-software-qualit%C3%A4tsattribute)<br>
3.1) Maintanability<br>
3.2) Usability<br>
3.2.1) Learnability<br>
3.2.2) Accessibility<br>
3.3.3) Feedback<br> 
3.3) Availability<br>
3.3.1) Fehlererkennung<br>
3.3.2) Fehlerbehebung<br>
3.3.3) Fehlervermeidung<br>
3.3.4) Resilienz<br>
3.4) Portability<br>
3.5) Interoperability<br>
3.6) Testability<br>
4) [Softwarearchitektur Design](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#4-softwarearchitektur-design) (Benno + ALLE ANDEREN WICHTIG)
5) [Software Entwicklung Prinzipien und Praktiken](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#5-software-entwicklung-prinzipien-und-praktiken)
6) [Softwarearchitektur Patterns](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#6-softwarearchitektur-patterns)
7) [Moderne Architekturen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#7-moderne-architekturen)
8) [Performance](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#8-performance) (Tizian)
9) [Security](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#9-security)
10) [Dokumentation](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#10-dokumentation) (TBD)
11) [DevOps und Softwarearchitektur](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#11-devops-und-softwarearchitektur)(TBD)
12) [Die Skills eines Softwarearchitekten](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#12-die-skills-eines-softwarearchitekten)(TBD)
13) [Evolutionäre Architekturen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#13-evolution%C3%A4re-architekturen)(TBD)
14) [Architektur und Legacy Applications](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#15-architektur-und-legacy-applications) (TBD)


## 1) Requirements

### 1.1) Kernkompetenzen des Online-shoppens:

Wie ist ihr derzeitiges Einkaufsverhalten?
- *Produkt, dass gekauft werden soll in Werbekatalogen suchen, die per Post geschickt wurden. Dann in einen Laden in der nähe gehen und mit Bargeld bezahlen.*

Wo sind die größten Probleme im derzeitigem Kaufverhalten?
- *Die physische Distanz zum Geschäft ist groß.*
- *Die Produktauswahl dauert lange.*
- *Die öffnungszeiten sind ein Problem.*

Finden Sie spezielle Produkte auf Anhieb im Geschäft?
- *Nein, nicht in jedem, vorallem Abends nicht, wenn alles ausverkauft ist.*

Welche Produkte würden Sie eher nicht online kaufen?
- *Dinge, die getestet werden müssen wie Kleidung, oder Dinge, die in echt gesehen werden müssen. Diese würden lokal gekauft.*

Könnten Sie sich vortstellen Bücher oder Büromaterial online zu kaufen mit Lieferung nach Hause?
- *Ja.*

Würden Sie dafür eine Liefergebühr bezahlen?
- *Ja. Aber wenn es lokal verfügbar ist und billiger würde ich es eher lokal kaufen.*

Was wäre, wenn Amazon Ihnen gewährleistet, dass ein Produkt verfügbar ist und innerhalb von 1-2 Werktagen zu Hause ist?
- *Dann wäre ein Onlinekauf vorstellbar.*

### 1.2) Vorstellungen zur Plattform:

Wie würden Sie sich vorstellen ein Buch zu kaufen?
- *Eingabe in einer Leiste zum suchen. Dann wird das Buch angezeigt. Dann kann es gekauft werden.*

Würden Sie nach der Nutzun des Dienstes eine Bewertung abgeben?
- *Ja, wenn eine Errinnerung dafür kommt.*

Wie soll der Bezahlvorgang aussehen?
- *Frage nach der Kreditkarte, oder bezahlen mit PayPal, Vorkasse oder per SEPA.*

Würden sie für eine zusätzliche Dienstleistung, dass ein Produkt schneller kommt, bezahlen?
- *Ja, wenn es garantiert ist.*

Wie viel Geld würden Sie maximal dafür ausgeben pro Jahr?
- *50 bis 60 Euro*
 
Wie stellen sich die Suche vor?
- *Es soll nach Kategorien und relevanten Ergebnissen gefiltert werden können. Relevante Ergebnisse sollen angezeigt werden.*

Gibt es noch weitere Suchfilter, die Sie gerne hätten?
- *Filtern nach Preis, Produktspezisischen Eigenschaften, Marke, Sprache, Bewertung, ISBN soll möglich sein.*

Weitere Punkte:
*Bestellungen sollen in Historie angezeigt werden, Retouren sollen einfach sein, Lieferverfolgunng, Stornierung, hohe Kulanz*

### 1.3) Functional Requirements:
- Globale schnelle Verfügbarkeit
- Hohe Verfügbarkeit
- Mobile Erreichbarkeit
- Kauf mit Account und als Gast
- Account soll Adressen und Bezahlinformationen speichern können
- Bestellhistorie soll sichtbar sein
- Interfaces zu Post, DHL, Verkäufern und deren Systemen (Oberflächen), zum Kunden
- Anzeige von verschiedenen Produkten
- Suche von bestellbaren Produkten
- Stornieren von Produkten
- Rücksenden von Produkten

### 1.4) Non-Functional Requirements
- 1 Sekunde pro Aufruf maximal
- Verfügbarkeit der Server 99,99%
- Laden der mobilen Webseite über 2G Netz innerhalb von 2 Sekunden
- Zeit bis die Kaufbestätigung per E-mail beim Kunden ankommt weniger als 2 Minuten
- Akzeptieren von Bezahlungen via Kreditkarte, SEPA Lastschrift, Geschenkgutscheinen, Aktionsgutscheinen, Monatsabrechnung, iDEAL, Przelewy24 (P24)
- Anzeigen der Bestellhistorie in unter 3 Sekunden
- Anzeigen der Bestellhistorie für jedes Jahr, jeden Monat und dem gesamten Zeitraum
- Darstellung der Produkte nach Suche in Liste
- Anzahl der angezeigten Produkte vom Nutzer auswählbar zwischen 20, 50, 100 und 500 Ergebnissen
- Suche filterbar nach Kategorien wie Produktkategorie, Preis, Bewertung, Marke, etc.
- Geld zurücküberweisen bei Stornierung und Rücksendung von Ware innerhalb von einer Woche
- Rücksendungen werden angenommen innerhalb von 30 Tagen nach Lieferung

### 1.5) Business Requirements:
- Traditionellen Einzelhandel ersetzen
- Probleme: Verfügbarkeit, Wartezeit, Anreisezeit, etc.
- Schaffen einer Online Plattform um diese Zeiten zu verkürzen und Verfügbarkeit zu erhöhen
- Ähnlichkeiten: Verkauf von Produkten
- Abgrenzung: Abwicklung des Kaufvorgangs online, Lieferung
- Anforderung vom Markt: Einfacherer Kauf als im klassischen Einzelhandel (geringerer Zeitaufwand, Produktsuche, größere Auswahl an Zahlungsdienstleistern, Lieferung)

### 1.6) Constraints
- Einhalten der gesetzlichen Rahmenbedingungen
- DSGVO-Konforme Datenspeicherung
- Verbot für Minderjährige einen Kauf zu tätigen
- Einhalten der Zollbedingungen für die jeweiligen Länder
- Einhaltung der Verträge mit Lieferdienstleistern und Zahlungsdienstleistern

## 2) Domänen
### 2.1) Shopoberfläche
- Hohe Benutzerfreundlichkeit
- Einfache Bedienbarkeit
- Übersichtliche Darstellung
- Responsives Design

### 2.2) CRM + Kundenverwaltung
- 24/7 Support bei Fragen und Wünschen
- Anfragebearbeitung in maximal 10 Minuten
- Feedback- und Bewertungsfunktion
- Speichern von Kundeninformationen wie Adresse, Zahlungsdaten, Bewertungen, Bestellungen, etc.

### 2.3) Produktempfehlungssystem
- Empfehlungen geben auf Basis von Käufen
- Empfehlungen auf Basis von zuletzt angesehen
- Empfehlungen auf Basis von Kundenbewertungen
- Empfehlungen auf Basis von Geolocations
- Empfehlungen auf Basis von Nutzerverhalten
- Empfehlungen auf Basis von Trends

### 2.4) Zahlungssystem
- Unterstützen von einer vielzahl an Zahlungsanbietern (siehe 1.4.)
- Einfache Abrechnung von Zahlungen
- Schnelles Bezahlen (wenige Klicks)
- Nutzen von gespeicherten Zahlungsdaten zum Kauf

### 2.5) Buchhaltung
- Keine Buchung ohne Beleg
- Nutzen einer Softwareunterstüzung für die Buchhaltung
- Automatisierung von Buchhaltungsprozessen

### 2.6) Versand
- schneller Versand innerhalb eines Landes/Handelszone von wenigen Tagen mit Ausnahme von Produkten die aufwändig importiert werden müssen
- Versanddienstleister kümmern sich um Versand zum Endkunden
- Nur einladen in von Versanddienstleistern gestellte Transportmitteln

#### 2.6.1) Versanddienstleister
- Hermes
- DHL
- DPD
- FedEx
- etc.

### 2.7) Lager
- Chaotische Lagerhaltung für Platzoptimierung
- Automatisertes Lager
- Lagerhaltungssystem meldet Lagerbestände

### 2.8) Produktekatalog
- Große Auswahl an Produkten
- Große Produktvielfalt

#### 2.8.1) Anbieter
- Große Anzahl an Anbietern für Produkte
- Enger Kontakt mit Anbietern

## 3) Software Qualitätsattribute
### 3.1) Maintanability
- modulare Architektur → gewährleistet einfache Erweiterbarkeit und verringert Komplexität
- Komponenten erfüllen genau eine definierte Funktion
- Kommunikation über einheitliche Schnittstellen
- Schnittstellen dürfen entweder gar nicht oder nur global verändert werden, sodass jede Komponente mit einer gleichen Schnittstellendefinition arbeitet
Veränderungen eines Komponenten (z.B.: Fehlerkorrekturen) haben keinen Einfluss auf andere Komponenten. 

### 3.2) Usability
#### 3.2.1) Learnability
- (Web-) Design der Anwendung ist immer ähnlich (z.B. Kacheldesign)
- Anlehnung des Designs an ähnliche Applikationen wie Webshops
- Einmalige Erarbeitung von Abläufen, sodass diese für den Endnutzer immer gleich sind
- Guides / Touren für Erstnutzer
#### 3.2.2) Accessibility
- Web-Application, Mobile-Application für Android, IOS und Windows
- Breadcrumbs unterstützen Navigation, sodass s
- Einheitliche, lesbare Farben mit High-Contrast Modus (+ Darkmode)
- Mehrsprachigkeit und Anpassung an kulturelle Konventionen nach i18n 
#### 3.3.3) Feedback
- Interaktive Elemente (Warenkorb-, Bezahlbutton, usw.) erhalten Tooltips
- Klare Kommunikation über Fehlerbehandlung

### 3.3) Availability
|Verfügbarkeit | Downtime/Jahr | Downtime / Monat | Downtime / Woche|
---|---|---|--- 
99,999% | 5 min 16 sec | 25,9 sec | 6,05 sec

#### 3.3.1) Fehlererkennung
- Ping < 50ms 
    - durch global verteilte Server
    - Wahl eines Server bei der Verbindung ist abhängig von Ping, Server mit der niedrigsten Ping wird ausgewählt
- Heartbeat & Sanity Checks
    - Periodische Überprüfung, dass Systeme laufen und korrekt funktionieren
    - Für jedes Modul separat durchzuführen
- Condition Monitoring
    - Überprüfen, ob sich Prozesse wie erwartet verhalten
    - Denkbar wäre bspw. das erkennen von Prozessen, die in Endlosschleifen gefangen sind

#### 3.3.2) Fehlerbehebung
- Exception Handling für Module und Funktionen sorgt für geplante Ausnahmebehandlung
- Retry Strategien in Intervallen zur Mitigation von Racing Conditions und temporär nicht verfügbaren Services
- Versionierung der Architektur für Rollbacks
- Graceful degradation
    - Fehlerhafte Module und Funktionen abschalten
    - Setzt funktionierende und umfassende Fehlererkennung voraus
    - Freischaltung nach Fix

#### 3.3.3) Fehlervermeidung
- Datenbanken arbeiten mit Transaktionen 
- Competence Sets durch umfangreiches Exception Handling erfüllt → siehe Fehlerbehebung 
- Exception Prevention: Die Logik des Codes verhindert Exceptions durch Input Validation, Überprüfen von Array Grenzen, <code>null</code> Werten u.Ä.

#### 3.3.4) Resilienz
- Isolation: modulare Architektur verhindert Kaputtgehen des gesamten Systems
- Redundanz: Global verteilte Server (siehe Fehlererkennung) realisieren Redundanz unter Verlust einer geringen Ping
- Lose Kopplung durch modulare Architektur und idempotente Kommunikation zwischen Komponenten
- Fallback → siehe Fehlerbehebung
Graceful Degradation of Service → siehe Fehlerbehebung

### 3.4) Portability
- Installability und Replaceability entfallen, sofern Kompatibilität mit populären Web Browsern (Firefox, Chrome, Edge, Opera, Safari, ...) gewährleistet ist
- Internationalisierung siehe Usability → Accessibility 
### 3.5) Interoperability 
- Verwendung der Standards JSON und HTTP(S) für den Informationsaustausch mit Dritten 
- Bezug von Daten Dritter über angebotenen Schnittstellen, Anbieten eigener Daten über eigene APIs, inklusive Dokumentation zur Nutzung der APIs
- Einheitliche Syntax und Semantik
### 3.6) Testability
- Automatische Tests gewährleisten eine umfangreiche Abdeckung
- Unit Tests zum Test einzelner Komponenten, Nutzung von Mockdaten
- Integration Tests mehrer Komponenten, insbesondere nach Veränderung eines Komponenten
- Laufende Tests, kann mit Fehlererkennung / Sanity Checks kombiniert werden

## 4) Softwarearchitektur Design

## 5) Software Entwicklung Prinzipien und Praktiken
Folgende Prinzipien und Praktiken sollen für eine Qualitätserhöhung, Betriebsvereinfachung, Erhöhung der Wiederverwendbarkeit, Fehlererkennung und einfacheres Testen des Softwaresystems umgesetzt werden:
### Lose Kopplung: 
- Die einzelnen Module sind unabhängig voneinander
- Prinzip: The Law of Demeter (LoD)
  - Limitierte Kommunikation zwischen den Modulen (nur Freunde reden miteinander)
  - Ein Objekt in einem Modul soll nur Methoden von sich selbst, von Objekten, die ihm übergeben wurden, von Unterobjekten, von Objekten die er erzeugt hat oder von globalen Objekten aufrufen
  - Ein Modul soll so wenig wie möglich über andere Module wissen
### Hohe Kohäsion:
- Maß für den Zusammenhalt von Elementen innerhalb eines Moduls
- Ziel: Functional cohesion: Alle Elemente in einem Modul dienen dem gleichen, eindeutigen und klar definierten Zweck -> andere Elemente sollten in ein anderes oder neues Modul ausgelagert werden
- Jedes Modul sollte eine eindeutige, klar definierte Aufgabe besitzen -> Alle Elemente in diesem Modul sollen gemeinsam auf diese Aufgabe hinarbeiten
### Reduzierung von Komplexität
- Eine hohe Komplexität erzeugt Probleme
- Prinzipien zur Reduzierung von Komplexität: 
  - KISS: Code einfach halten
  - DRY: Keine Redundanzen
  - Information hiding: Das Was vom Wie trennen
  - YAGNI: Keine Funktionalität implementieren, die nicht benötigt wird
  - Seperation of Concern: Verantwortlichkeiten trennen
### SOLID- Prinzip
- S = Single Responsibility
  - Jede Klasse soll genau eine Verantwortlichkeit besitzen
- O = Open-Close-Principle:
  - Klassen können ohne bestehenden Code zu ändern, erweitert werden -> darf keine Änderungen in einer anderen Klasse auslösen
  - Module sollen erweitert werden können, jedoch soll es nicht möglich sein, den Sourcecode zu ändern
  - Ausnahmen: Bug fixes & Änderungen am Code, die keinerlei Auswirkung auf den Nutzer dieses Codes hat
- L = Liskov-Substitution Principle
  - Unterklassen müssen ihre Oberklassen ersetzen können
  - Änderungen in Unterklassen dürfen das Verhalten der Oberklasse nicht verändern
- I = Interface Segregation Principle
  - Implementierungen dürfen nicht von Methoden und/oder Attributen abhängig sein, die sie nicht benutzen
- D = Dependency Inversion Principle
  - Module höherer Ebenen sollen nicht von Modulen niedrigerer Ebenen abhängen. 
  - Abstraktionen sollten nicht von Details abhängen <br>
   &rarr; Module und Details sollten von Abstraktionen abhängen
### Inversion of Control:
- Beschreibt die Arbeitsweise von Frameworks: die Steuerung der Ausführung bestimmter Unterprogramme wird an das Framework abgegeben
### Dependency Injection:
- Technik, bei der ein Objekt die Beziehungen eines anderen Objektes liefert
- Beziehung kann z.B. als Service genutzt werden. Dabei bestimmt nicht der Klient welchen Service er nutzt, sondern jemand anderes -> Grundanforderung
- Ziel: Trennen der Verantwortlichkeiten der Erzeugung und Benutzung von Objekten
- Typen:
  - Constructor Injection: Beziehungen werden durch den Konstruktor des Klienten geliefert
  - Setter/Property Injection: Klient stellt eine setter-Methode für die Injection zur Verfügung
  - Interface/Method Injection: Interface der Beziehung stellt eine Injectionsmethode zur Verfügung -> Klienten müssen ein Interface implementieren, das eine setter-Methode implementiert


## 6) Softwarearchitektur Patterns

Als ein Pattern wollen wir MVC benutzen.

### MVC

#### Problemebeschreibung
Aufbau der Website; Logische Trennung der verschiedenen Funktionen ist nicht gegeben.
Arbeitsteilung wird dadurch erschwert.

#### Lösungsbeschreibung
Controller, Model und View
##### Controller
&rarr; Logik, Vermittlung
&rarr; Kontrolliert Views & Models
##### View
&rarr; Darstellung, UI für Benutzer
##### Model
&rarr; Daten & Statushaltung

#### Bewertung
##### Vorteile
 Klare Trennung, hoher Verständlichkeitsgrad
##### Nachteile
 Organisationsaufwand, dieser ist jedoch sehr gering

#### Einsatzgebiete
Programmierung/ Architektur des Frontends

MVC wollen wir in Verbindung mit der Schichtenarchitektur benutzen.

### Schichtenarchitektur

#### Problembeschreibung
Aufteilung zwischen Server und Client ist unklar, dadurch kann die Programmierung nicht stattfinden.

#### Lösungsbeschreibung
Horizontale Schichten, orientiert an MVC. Dabei wird zwischen Präsentation, Funktion und Daten unterschieden.
Hier ist die Frage, welcher dieser Schichten vom Client übernommen wird und welche vom Server. Dabei haben wir uns für einen Thin-Client entschieden, da bei einem Online Store die Sicherheit extrem wichtig ist und bei einem Thin-Client die geringste Manipulationsgefahr besteht. Außerdem ist es am schnellsten und von der Hardware des Clients abgekoppelt. 

#### Bewertung
##### Vorteile
&rarr; Schnelligkeit und geringe Client-Hardwareanforderungen
&rarr; Wiederverwendbarkeit wird unterstützt
&rarr; Höhere sicherheit
&rarr; Bessere Skalierbarkeit

##### Nachteile
&rarr; Interfaces zwischen den Layern verursachen Mehraufwand
&rarr; Höhere Performance für den Server nötig

#### Einsatzgebiete
Architektur des Gesamtsystems

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

## 14) Architektur und Legacy Applications


# Gruppe
- Tizian Groß
- Benno Grimm
- Tristan Emig
- Anna-Lena Richert
- Anton Ochel
- Marcel Mertens
