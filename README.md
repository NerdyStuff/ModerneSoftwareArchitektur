# Moderne Softwarearchitektur
Repository für moderne Softwarearchitektur

Präsentation: https://docs.google.com/presentation/d/1_yt3ar8iu2F7N605o76C4I5c6zrK9IS6SiFBhvYivCk/edit#slide=id.g72c1398093_0_41

# Inhaltsverzeichnis
1) [Requirements](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/README.md#1-requirements)<br>
1.1) Kernkompetenzen des Online-shoppens<br>
1.2) Vorstellungen zur Plattform<br>
1.3) Functional Requirements<br>
1.4) Non-Functional Requirements<br>
1.5) Business Requirements<br>
1.6) Constraints<br>
1.7) Personas<br>
 1.7.1) Persona 1: Karen Kaufer<br>
 1.7.2) Persona 2: Alan Turing<br>
 1.7.3) Persona 3: Simon Blume<br>
 1.7.4) Persona 4: Lars Echterling<br>
2) [Domänen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#2-domänen)<br>
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
2.9) Schaubild<br>
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
4) [Softwarearchitektur Design](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#4-softwarearchitektur-design)
4.1) Erste Iteration
4.2) Zweite Iteration
4.3) Dritte Iteration
5) [Software Entwicklung Prinzipien und Praktiken](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#5-software-entwicklung-prinzipien-und-praktiken)<br>
5.1) Lose Kopplung<br>
5.2) Hohe Kohäsion<br>
5.3) Reduzierte Komplexität<br>
5.4) SOLID- Prinzip<br>
5.5) Inversion of Control<br>
5.6) Dependency Injection<br>
6) [Softwarearchitektur Patterns](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#6-softwarearchitektur-patterns)<br>
6.1) MVC<br>
 6.1.1) Problemebeschreibung<br>
 6.1.2) Lösungsbeschreibung<br>
 6.1.3) Bewertung<br>
 6.1.4) Einsatzgebiete<br>
6.2) Schichtenarchitektur<br>
 6.2.1) Problembeschreibung<br>
 6.2.3) Lösungsbeschreibung<br>
 6.2.4) Bewertung<br>
 6.2.5) Einsatzgebiete<br>
7) [Moderne Architekturen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#7-moderne-architekturen)
8) [Performance](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#8-performance)
9) [Security](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#9-security)<br>
9.1) Abwehren von Angriffen<br>
9.2) Sicherheit im Ruhezustand<br>
9.3) Sicherheit bei Gebrauch<br>
9.4) Sicherheit bei Transport<br>
9.5) Vermeiden, dass dritte Zugang zu Daten bekommen<br>
9.6) Integrität<br>
9.7) Wertvolle Teile der Architektur<br>
9.8) Potentielle Bedrohungen<br>
9.9) Potentieller Schaden daraus<br>
9.10) Klassifizierung der Bedrohungen<br>
9.11) Secure by Design<br>
9.12) Kryptografie<br>
9.13) Identity und Access Management<br>
10) [Dokumentation](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#10-dokumentation)
11) [DevOps und Softwarearchitektur](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#11-devops-und-softwarearchitektur)
12) [Evolutionäre Architekturen](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#13-evolution%C3%A4re-architekturen)
13) [Architektur und Legacy Applications](https://github.com/NerdyStuff/ModerneSoftwareArchitektur#15-architektur-und-legacy-applications)

# Business Story
In Zeiten einer von Corona geplagten Welt, in der man nicht mehr gemütlich am Wochenende shoppen gehen kann, realisiert man, wie abhängig man von physischen Geschäften ist.
Wir haben uns gefragt: "Warum eigentlich?".
<p>
In Tagen des Internets und globaler Vernetzung ist die Grundlage für ein digitales Geschäft  bereits geschaffen. 
Mit Amazon wollen wir Menschen weltweit die Möglichkeit geben, bequem und ohne das Haus verlassen zu müssen Produkte aus der ganzen Welt zu kaufen.
Ein zentraler Sammelpunkt an dem beinahe alle vorstellbaren Produkte dieser Welt verfügbar sind, macht Einkaufen nicht nur einfacher und schneller, sondern auch sicherer.
</p>

## 1) Requirements

### 1.1) Kernkompetenzen des Online-Shoppens:

Wie ist ihr derzeitiges Einkaufsverhalten?
- *Produkt, dass gekauft werden soll in Werbekatalogen suchen, die per Post geschickt wurden. Dann in einen Laden in der Nähe gehen und mit Bargeld bezahlen.*

Wo sind die größten Probleme im derzeitigem Kaufverhalten?
- *Die physische Distanz zum Geschäft ist groß.*
- *Die Produktauswahl dauert lange.*
- *Die Öffnungszeiten sind ein Problem.*

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
- *Eingabe in einer Leiste zum Suchen. Dann wird das Buch angezeigt. Dann kann es gekauft werden.*

Würden Sie nach der Nutzung des Dienstes eine Bewertung abgeben?
- *Ja, wenn eine Erinnerung dafür kommt.*

Wie soll der Bezahlvorgang aussehen?
- *Frage nach der Kreditkarte, oder bezahlen mit PayPal, Vorkasse oder per SEPA.*

Würden sie für eine zusätzliche Dienstleistung, dass ein Produkt schneller kommt, bezahlen?
- *Ja, wenn es garantiert ist.*

Wie viel Geld würden Sie maximal dafür ausgeben pro Jahr?
- *50 bis 60 Euro*
 
Wie stellen Sie sich die Suche vor?
- *Es soll nach Kategorien und relevanten Ergebnissen gefiltert werden können. Relevante Ergebnisse sollen angezeigt werden.*

Gibt es noch weitere Suchfilter, die Sie gerne hätten?
- *Filtern nach Preis, produktspezifischen Eigenschaften, Marke, Sprache, Bewertung, ISBN soll möglich sein.*

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
- Suche von bestellbaren Produkten mit Filtern und Kriterien
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
- Filtern von nicht angemessenen und illegalen Inhalten & Produkten

### 1.7) Personas
#### 1.7.1) Persona 1: Karen Kaufer

- Name: Karen Kaufer
- Alter: 45 Jahre
- Deutsch, geringe Englisch Kenntnisse
- Verheiratet, zwei Kinder
- Buchhalterin bei einem mittelständigen Unternehmen, durchschnittliches Einkommen
- Kein tiefgründiges technisches Wissen, kann aber problemlos das Internet navigieren und mit Computern umgehen

<b> Einkaufsverhalten </b>
- Impulsivkäuferin, nutzt Website, um sich Angebote anzugucken
- Sieht sie in ihren personalisierten Vorschlägen Produkte die ihr gefallen, kauft sie diese
- Hat bei Benutzen der Website meist keinen genauen Need, möchte sich erstmal nur umgucken
- Möchte mit Lastsschrift oder Kreditkarte bezahlen können
- Möchte sich nach mehrmaligem Einkaufen ein Benutzerkonto anlegen, um zukünftige Käufe schneller abwickeln zu können

<b> Paint-Points </b>
- Ist von zu vielen Details überfordert, möchte beim Kauf nur das Wichtigste über ein Produkt erfahren
- Benutzt die Seite nicht noch einmal, wenn der Kaufvorgang zu kompliziert ist oder lange dauert
- Hasst lange Lieferzeiten, hat kein Verständnis für Verzögerungen
- Möchte leichte Retouren haben, da sie viel wieder zurückschickt

<b> Needs & Wishes </b>
- Benutzerkonto, in dem Informationen über Liefer-, Rechnungsadressen und Zahlungsinfromationen gespeichert werden
- Einfache Benutzung, die an die anderer Webshops angelegt ist 

#### 1.7.2) Persona 2: Alan Turing
<b> Biographie </b>
- Name: Alan Turing
- Alter: 27 Jahre
- Deutsch, gute Englischkenntnisse
- IT-Admin eines mittelständigen Unternehmen, etwas überdurchschnittliches Einkommen
- Kennt sich technisch sehr gut aus
- Hat schon 5000 Stunden Dota 2 

<b> Einkaufsverhalten </b>
- Hat konkrete Vorstellung von Produkten, die er kaufen möchte
- Benötigt umfassende und detailierte Beschreibungen von Produkten, um zu überprüfen, ob Produkt mit seinen Vorstellungen übereinstimmt
- Möchte vor dem Kauf Rezensionen anderer Kunden lesen
- Bezahlt mit Lastschrift

<b> Paint-Points </b>
- Ungenaue Suchfunktionen, findet trotz exakten Angaben in der Suche unpassende Produkte

<b> Needs & Wishes </b>
- Akzeptiert lange Lieferzeiten bei Produkten aus dem Ausland, würde aber am liebsten die Lieferung bereits am selben Tag erhalten, auch gegen Aufpreis

#### 1.7.3) Persona 3: Simon Blume
<b> Biographie </b>
- Name: Simon Blume
- Alter: 35 Jahre
- Wohnt in Prenzlauer Berg, Berlin
- Hat einen hippen Laden, in dem er vegane, Bio-Spielzeuge für Kinder verkauft
 
<b> Verkaufsverhalten </b>
- Will seine Produkte online verkaufen
- Wenn er ein neues Produkt entwirft, möchte er dieses mit Bildern und Produktbeschreibung einpflegen
- Produkte die er nicht mehr herstellt, entfernt er wieder aus seinem Katalog

<b> Paint-Points </b>
- Will keinen Aufwand einer eigenen Shopsoftware
- Hasst es, wenn er nicht weiß, wieviel Geld er bekommt und wieviel er an Amazon abtreten muss muss

<b> Needs & Wishes </b>
- Möchte dass seine Produkte ohne viel Aufwand gut dargestellt werden
- Will eine klare Anweisung, wie er seine Produkte dort einstellen kann
- Möchte Beratung zum Verkaufsprozess 


#### 1.7.4) Persona 4: Lars Echterling 
<b> Biographie </b>
- Name: Lars Echterling
- Alter: 54 Jahre
- Auftragsbearbeiter bei DHL für den Bereich Amazon Deutschland Südwest
- Zuständig für die Lieferungen, die von Amazon zu DHL reinkommen

<b> Verhalten </b>
- Benutzt DHL Programm, was die API von Amazon benutzt

<b> Paint-Points </b>
- Hasst es, wenn sein Programm lange lädt
- Wenn eine Bestellung falsch ausgeliefert wird, bekommt er Ärger

<b> Needs & Wishes </b>
- Will ohne viel Aufwand seinen Job machen
- Will mit Mitarbeitern bei Amazon direkt sprechen können bei Problemen
- Kommunikation mit Amazon soll gut funktionieren
- Möchte eine gute Integration mit seinem DHL Programm

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
- Externes Programm möglich
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

### 2.7) Lagerveraltung
- Chaotische Lagerhaltung für Platzoptimierung
- Automatisertes Lager
- Lagerhaltungssystem meldet Lagerbestände

### 2.8) Produktekatalog
- Große Auswahl an Produkten
- Große Produktvielfalt

#### 2.8.1) Anbieter
- Große Anzahl an Anbietern für Produkte
- Enger Kontakt mit Anbietern

### 2.9) Schaubild
![Domain Driven Design](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/Files/DDD.png)

## 3) Software Qualitätsattribute
### 3.1) Maintanability
- Microservice Architektur → gewährleistet einfache Erweiterbarkeit und verringert Komplexität
- Komponenten erfüllen genau eine definierte Funktion
- Kommunikation über einheitliche Schnittstellen
- Schnittstellen dürfen entweder gar nicht oder nur global verändert werden, sodass jede Komponente mit einer gleichen Schnittstellendefinition arbeitet
- Veränderungen eines Komponenten (z.B.: Fehlerkorrekturen) haben keinen Einfluss auf andere Komponenten. 

### 3.2) Usability
#### 3.2.1) Learnability
- (Web-) Design der Anwendung ist immer ähnlich (z.B. Kacheldesign)
- Anlehnung des Designs an ähnliche Applikationen wie Webshops
- Einmalige Erarbeitung von Abläufen, sodass diese für den Endnutzer immer gleich sind
- Guides / Touren für Erstnutzer
#### 3.2.2) Accessibility
- Web-Application, Mobile-Application für Android, IOS und Windows
- Breadcrumbs unterstützen Navigation
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

Wir benutzen zur Gestaltung der Architektur die Technik von Microsoft für Architektur und Design.
Bei dieser Planung wurde Top-Down Planning benutzt, da dies bei so großen komplexen Projekten sinnvoller ist.

### Iteration 1

#### Schritt 1
In Schritt 1 legen wir das grundlegende Ziel der aktuellen Iteration fest.

In dieser Iteration wollen wir die grobe Architektur unsere Plattform festlegen sowie Abhängigkeiten von Drittsystemen.

#### Schritt 2
In diesem Schritt sollen wichtige Key Scenarios identifiziert werden, die unsere Plattform abdecken muss.

Produkte kaufen, Verfügbarkeit auf der Welt, Lieferung nach Hause.

#### Schritt 3
In diesem Schritt soll eine Übersicht der Anwendungen erstellt werden, die diese Ziele erreichen.

Anwendungstyp: Website<br>
Einschränkungen: Schnell, Sicher, Benutzerfreundlich<br>
Zielumgebung: Website auf Userseite, Mobil oder Desktop<br>
Architekturstil: Microservices, Client-Server<br>
Relevante Technologien: Docker, Kubernetes, Client-Server, HTTPS, Datenbanken<br>
**Skizze:**<br>
![Erste Iteration](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/Files/Iterationen/Erste/ErsteIteration.png)

#### Schritt 4
In diesem Schritt werden die wesentlichen Hindernisse dieser Architektur beschrieben.

Als Hindernis könnte hier die Anbindung und Kommunikation der Partnerunternehmen wie die Logistikdienstleister und evtl. Lagerdienstleister anzusehen sein.
Auch ist besonders im Bezug auf größe des System die Performance als Hindernis anzusehen.

#### Schritt 5
In diesem Schritt werden Lösungskandidaten definiert.

Falls Architektur weiter bearbeitet werden muss -> weiter zu Schritt 2 <br>

Lösungsvorschlag siehe Skizze.
Diese Skizze muss noch granularer definiert werden. Dazu wird als nächstes ein Blick auf den Annahmeserver geworfen.

### Iteration 2

#### Schritt 2
In diesem Schritt sollen wichtige Key Scenarios identifiziert werden, die unsere Plattform abdecken muss.

Der User sendet eine Anfrage an Amazon, diese wird von einem Server angenommen, der aus einer großen Menge redundanter Server besteht. Dieser Server leitet dann die Anfrage auf verschiedene Microservices weiter und koordiniert diese.

#### Schritt 3
In diesem Schritt soll eine Übersicht der Anwendungen erstellt, die diese Ziele erreichen.

Anwendungstyp: Website<br>
Einschränkungen: Schnell, Sicher, Benutzerfreundlich<br>
Zielumgebung: Website auf Userseite, Mobil oder Desktop<br>
Architekturstil: Microservices, Client-Server, Redundante Server<br>
Relevante Technologien: Docker, Kubernetes, Client-Server, HTTPS, Datenbanken<br>
**Skizze:**<br>
![Zweite Iteration](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/Files/Iterationen/Zweite/Gesamt2.png)


#### Schritt 4
In diesem Schritt werden die wesentlichen Hindernisse dieser Architektur beschrieben.

Hier ist besonders die Kommunikation und Datenkonsistenz eine Herausforderung.

#### Schritt 5
In diesem Schritt werden Lösungskandidaten definiert.

Falls Architektur bearbeitet werden muss -> weiter zu Schritt 2 <br>

Der Lösungskandidat wurde in der Skizze gezeigt und wird in die Gesamtarchitektur eingefügt.

### Iteration 3

#### Schritt 2
In diesem Schritt sollen wichtige Key Scenarios identifiziert werden, die unsere Plattform abdecken muss.

Es wird ein weiter Blick auf Data Warehouse der Lagerhaltung geworfen. Diese wird genauer definiert.
#### Schritt 3
In diesem Schritt soll eine Übersicht der Anwendungen erstellt werden, die diese Ziele erreichen.

Anwendungstyp: ERP /BW Anwendung<br>
Einschränkungen: Schnell, Sicher, Benutzerfreundlich, Hohe Verfügbarkeit<br>
Zielumgebung: Desktop<br>
Architekturstil: Microservices, Redundante Server<br>
Relevante Technologien: Docker, Kubernetes, Datenbanken, Business Warehouse<br>
**Skizze:**<br>
![Dritte Iteration](https://github.com/NerdyStuff/ModerneSoftwareArchitektur/blob/master/Files/Iterationen/Dritte/Gesamt3.png)

#### Schritt 4
In diesem Schritt werden die wesentlichen Hindernisse dieser Architektur beschrieben.

#### Schritt 5
In diesem Schritt werden Lösungskandidaten definiert 

falls Architektur bearbeitet werden muss -> weiter zu schritt 2 <br>

Der Lösungskandidat wurde in die Skizze eingefügt

## 5) Software Entwicklung Prinzipien und Praktiken
Folgende Prinzipien und Praktiken sollen für eine Qualitätserhöhung, Betriebsvereinfachung, Erhöhung der Wiederverwendbarkeit, Fehlererkennung und einfacheres Testen des Softwaresystems umgesetzt werden:
### 5.1) Lose Kopplung: 
- Die einzelnen Module sind unabhängig voneinander
- Prinzip: The Law of Demeter (LoD)
  - Limitierte Kommunikation zwischen den Modulen (nur Freunde reden miteinander)
  - Ein Objekt in einem Modul soll nur Methoden von sich selbst, von Objekten, die ihm übergeben wurden, von Unterobjekten, von Objekten die er erzeugt hat oder von globalen Objekten aufrufen
  - Ein Modul soll so wenig wie möglich über andere Module wissen
### 5.2) Hohe Kohäsion:
- Maß für den Zusammenhalt von Elementen innerhalb eines Moduls
- Ziel: Functional cohesion: Alle Elemente in einem Modul dienen dem gleichen, eindeutigen und klar definierten Zweck -> andere Elemente sollten in ein anderes oder neues Modul ausgelagert werden
- Jedes Modul sollte eine eindeutige, klar definierte Aufgabe besitzen -> Alle Elemente in diesem Modul sollen gemeinsam auf diese Aufgabe hinarbeiten
### 5.3) Reduzierung von Komplexität
- Eine hohe Komplexität erzeugt Probleme
- Prinzipien zur Reduzierung von Komplexität: 
  - KISS: Code einfach halten
  - DRY: Keine Redundanzen
  - Information hiding: Das Was vom Wie trennen
  - YAGNI: Keine Funktionalität implementieren, die nicht benötigt wird
  - Seperation of Concern: Verantwortlichkeiten trennen
### 5.4) SOLID- Prinzip:
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
### 5.5) Inversion of Control:
- Beschreibt die Arbeitsweise von Frameworks: die Steuerung der Ausführung bestimmter Unterprogramme wird an das Framework abgegeben
### 5.6) Dependency Injection:
- Technik, bei der ein Objekt die Beziehungen eines anderen Objektes liefert
- Beziehung kann z.B. als Service genutzt werden. Dabei bestimmt nicht der Klient welchen Service er nutzt, sondern jemand anderes -> Grundanforderung
- Ziel: Trennen der Verantwortlichkeiten der Erzeugung und Benutzung von Objekten
- Typen:
  - Constructor Injection: Beziehungen werden durch den Konstruktor des Klienten geliefert
  - Setter/Property Injection: Klient stellt eine setter-Methode für die Injection zur Verfügung
  - Interface/Method Injection: Interface der Beziehung stellt eine Injectionsmethode zur Verfügung -> Klienten müssen ein Interface implementieren, das eine setter-Methode implementiert


## 6) Softwarearchitektur Patterns

Als ein Pattern wollen wir MVC benutzen.

### 6.1) MVC

#### 6.1.1) Problemebeschreibung
Aufbau der Website; Logische Trennung der verschiedenen Funktionen ist nicht gegeben.
Arbeitsteilung wird dadurch erschwert.

#### 6.1.2) Lösungsbeschreibung
Controller, Model und View
##### Controller
&rarr; Logik, Vermittlung
&rarr; Kontrolliert Views & Models
##### View
&rarr; Darstellung, UI für Benutzer
##### Model
&rarr; Daten & Statushaltung

#### 6.1.3) Bewertung
#####  Vorteile
 Klare Trennung, hoher Verständlichkeitsgrad
##### Nachteile
 Organisationsaufwand, dieser ist jedoch sehr gering

#### 6.1.4) Einsatzgebiete
Programmierung/ Architektur des Frontends

MVC wollen wir in Verbindung mit der Schichtenarchitektur benutzen.

### 6.2) Schichtenarchitektur

#### 6.2.1) Problembeschreibung
Aufteilung zwischen Server und Client ist unklar, dadurch kann die Programmierung nicht stattfinden.

#### 6.2.3) Lösungsbeschreibung
Horizontale Schichten, orientiert an MVC. Dabei wird zwischen Präsentation, Funktion und Daten unterschieden.
Hier ist die Frage, welcher dieser Schichten vom Client übernommen wird und welche vom Server. Dabei haben wir uns für einen Thin-Client entschieden, da bei einem Online Store die Sicherheit extrem wichtig ist und bei einem Thin-Client die geringste Manipulationsgefahr besteht. Außerdem ist es am schnellsten und von der Hardware des Clients abgekoppelt. 

#### 6.2.4) Bewertung
##### Vorteile
&rarr; Schnelligkeit und geringe Client-Hardwareanforderungen
&rarr; Wiederverwendbarkeit wird unterstützt
&rarr; Höhere sicherheit
&rarr; Bessere Skalierbarkeit

##### Nachteile
&rarr; Interfaces zwischen den Layern verursachen Mehraufwand
&rarr; Höhere Performance für den Server nötig

#### 6.2.5) Einsatzgebiete
Architektur des Gesamtsystems

## 7) Moderne Architekturen

Wir haben uns für folgende Architekturen entschieden:
### Microservice-Architecture
Wir haben uns für eine Microservice Architektur entschieden, da wir für unseren Anwendungsfall hier die meisten Vorteile sehen.
Zum einen ist die leichte Erweiterbarkeit einer Microservice-Architektur für unseren Service sehr Vorteilhaft, da unsere Platform sich auch auf andere Bereiche erweitern will. (Stream, Neue Produkte, Angebote etc.) Außerdem ist uns Ausfallsicherheit sehr wichtig, so wie Geschwindigkeit und Skalierbarkeit, da wir mit einer hohen Benutzerzahl rechnen.

### Cloud Native
Diese Architektur wollen wir mit einer Cloud Native Architektur verbinden. Wir sind der meinung, dass wir über eine Cloud Architektur unsere Platform für die Zukunft bereit machen. So können wir sowohl Hyperscaler, also Saas Angebote nutzen um unsere Skalierbarkeit zu realisieren, als auch eine globale Verteilung erreichen.

Mit dieser kombinierten Architektur sind wir sowohl für die Gegenwart wie auch für die Zukunft gut aufgestellt.

## 8) Performance
Performance ist für unsere global verwendete Software stetig zu verbessern. Hierbei sind die in den Qualitätsattributen definierten Forderungen zu erreichen. Unsere Entwicklerteams verwenden ein systematisches Vorgehen.

### Profile
Anhand der Kennzahlen Durchsatz, Bandbreite, Last und Auslastung wird die Performance der Anwendung gemessen.

### Analyse
In der Analyse suchen wir die Schwachstellen unserer Software (Bottlenecks) heraus. Meist sind die Fehler in der Anwendung vorhanden. Andere häufige Performance Schwachstellen sind die Datenbank, die CPU oder das Netzwerk. 

### Implement
Die Ergebnisse aus der Analyse werden durch unsere Entwicklerteams umgesetzt.

### Monitor
Durch weiteres beobachten unserer Kennzahlen schauen wir auf weitere Schwachstellen. Auch bei der Behebung der Schwachstellen können neue Schwachstellen entstehen, die wir somit ebenfalls aufdecken.

## 9) Security
### 9.1) Abwehren von Angriffen:
- Bruteforce Angriffe auf Login durch maximale Versuche berenzen
- Authentifizierung des Users über Passwort / 2 Faktor Authentifizierung
- Verschlüsselte Verbindungen zwischen User und Server
- Sicherstellen, dass persönliche Daten nicht nach außen dringen

### 9.2) Sicherheit im Ruhezustand:
- Persistenz der Daten
- Sichern des RAMs, wenn System neu gestartet wird
- Daten dürfen sich nicht ändern, wenn System im Ruhezustand

### 9.3) Sicherheit bei Gebrauch:
- Zugriffsbeschränkungen
- Veränderungen durch unberechtigte verhindern, um Integrität zu schützen

### 9.4) Sicherheit bei Transport:
- Daten müssen auf vollständigkeit überprüft werden (z.B. durch Checksummen \[stellen auch Integrität sicher\])

### 9.5) Vermeiden, dass dritte Zugang zu Daten bekommen:
-> Verschlüsselte Kommunikation
-> Sichere Passwörter (mindest Länge)

### 9.6) Integrität:
-> Daten dürfen nur verändert werden, wenn eine Authentifizierung stattfindet
(z.B. OAuth Token)

### 9.7) Wertvolle Teile der Architektur:
- Nutzerdaten
- Zahlungsinformationen
- Transaktionsmodule
- Logistikmodule

### 9.8) Potentielle Bedrohungen:
- Angriffe über die Webseite
  - Bruteforce
  - Login
- Phishing Mails um Kundendaten zu erlangen
- SQL Injections
- Denial of Service (Dos / DDos)
- Man in the middle Angriffe -> Spoofing/Tampering
- Login als Administrator

### 9.9) Potentieller Schaden daraus:
- Verlust von Daten
- Image Schaden
- Verlust von Vertrauen der Kunden
- Wirtschaftlicher Schaden
- Zerstörung von Infrastruktur

### 9.10) Klassifizierung der Bedrohungen:
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

### 9.11) Secure by Design:
- Keine Logins für Administrator von außen
- Nutzereingaben werden auf Injections geprüft
- Firewalls nutzen
- Dos/DDos Erkennung mit Firewall etc
- Alle Schutzmaßnahmen sind normalerweise an
- Nutzer bekommen nur Zugriff auf die Dinge, die sie brauchen
- Weniger Schnittstellen, die standartisiert sind und alle gesichert sind
- Hohe Fehlertoleranz => Keine Fehler nach a geben um Entdecken von Problemen zu verhindern -> Meldung an Administrator
- Passwortschutz

### 9.12) Kryptografie:
- Nutzen von SSL/HTTPS für kommunikation mit Browser
-> Umleiten von HTTP zu HTTPS
- Passwörter gehasht speichern
- Datenbanken und Daten verschlüsseln
- Authentifizierung mittels Key / Tokens für interne Arbeiten

### 9.13) Identity und Access Management:
- Verifizierung der Nutzer und des Servers mittels Zertifikaten
- OAuth Token
- Keys
- Signaturen (z.B. PGP)

Um eine gute Sicherheit zu gewährleisten sollten Pakete aktualisiert werden,
Server Wartungen durchgeführt werden, Logs angelegt werden und regelmäßig geprüft werden.
Honeypots können genutzt werden um von Angreifern zu lernen.

## 10) Dokumentation
Das System sollte sowohl mit den Anforderung und Requierments gut dokumentiert sein, wie auch der Code und die Architektur gut dokumentiert werden soll. 
Diese Dokumentation soll zentral gelagert und für alle zugänglich sein.

## 11) DevOps und Softwarearchitektur
Durch die Nutzung von Continuous Integration und Automatisierungsprozessen kann schnell eine gute Software an den Endkunden ausgeliefert werden. Unsere Entwicklungsteams sollten aus Vertretern der verschiedenen Fachbereichen bestehen um die Fähigkeiten der Entwickler optimal nutzen zu können. Alle Fortschritte sollten messbar sein. Durch die Nutzung eines Backlogs oder Issues können die Fortschritte der einzelnen Komponenten genau bestimmt werden und Fehler schnell erkannt werden. Die Kundenbedürfnisse müssen während der Entwicklung mit einbezogen werden. Erfahrungen und Wissen können durch Dokumentationen und interne Schulungen ausgetauscht werden. Da wir microservices verwenden wollen können die einzelnen Interfaces genau getestet und gewartet werden. Zusätzlich können die Services automatisch in die Cloud deployed werden, was die Skalierbarkeit und die Verfügbarkeit gewährleistet. 

## 12) Evolutionäre Architekturen
Das System muss so gebaut werden, dass es auf Veränderungen vorbereitet ist und leicht erweitert werden kann. Hierzu ist unsere Microservice-Arhcitektur sehr passend. Modifikationen werden mithilfe von Fitness-Funktionen überwacht und bewertet.

Zum Beispiel könnte das über Performance Anforderungen geregelt werden. Wenn nach einer Archtiketur Modifikation eine Performance Anforderung mit dem dazugehörigen Test nicht erfüllt wird, so muss die Änderung überarbeitet werden. So kann stetig unsere Services verbessern und dabei die Anforderungen im Blick halten.

## 13) Architektur und Legacy Applications
Um Legacy Applications müssen wir uns zur Zeit noch keine Gedanken machen, da unser System neu ist und somit noch keine älteren Anwendungen mit bedenken müssen. Aus Benutzerseite muss sicher gegangen werden, dass ältere Zugriffsmethoden wie IE funktionieren.

Da unsere Anwendung wahrscheinlich länger erhalten bleiben wird, legen wir besonderen Wert darauf, unseren Code testbar und auch in der Zukunft wartbar zu machen. Auch soll darauf geachtet werden, dass der Code möglichst verständlich und sauber ist, sodass dieses Produkt noch in Zukunft erweitert und gewartet werden kann.

# Gruppe
- Tizian Groß
- Benno Grimm
- Tristan Emig
- Anna-Lena Richert
- Anton Ochel
- Marcel Mertens
