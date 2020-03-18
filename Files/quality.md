# Softwarequalität
## Maintanability
- modulare Architektur → gewährleistet einfache Erweiterbarkeit und verringert Komplexität
- Komponenten erfüllen genau eine definierte Funktion
- Kommunikation über einheitliche Schnittstellen
- Schnittstellen dürfen entweder gar nicht oder nur global verändert werden, sodass jede Komponente mit einer gleichen Schnittstellendefinition arbeitet
Veränderungen eines Komponenten (z.B.: Fehlerkorrekturen) haben keinen Einfluss auf andere Komponenten. 

## Usability
### Learnability
- (Web-) Design der Anwendung ist immer ähnlich (z.B. Kacheldesign)
- Anlehnung des Designs an ähnliche Applikationen wie Webshops
- Einmalige Erarbeitung von Abläufen, sodass diese für den Endnutzer immer gleich sind
- Guides / Touren für Erstnutzer
### Accessibility
- Web-Application, Mobile-Application für Android, IOS und Windows
- Breadcrumbs unterstützen Navigation, sodass s
- Einheitliche, lesbare Farben mit High-Contrast Modus (+ Darkmode)
- Mehrsprachigkeit und Anpassung an kulturelle Konventionen nach i18n 
### Feedback
- Interaktive Elemente (Warenkorb-, Bezahlbutton, usw.) erhalten Tooltips
- Klare Kommunikation über Fehlerbehandlung

## Availability
|Verfügbarkeit | Downtime/Jahr | Downtime / Monat | Downtime / Woche|
---|---|---|--- 
99,999% | 5 min 16 sec | 25,9 sec | 6,05 sec

### Fehlererkennung
- Ping < 50ms 
    - durch global verteilte Server
    - Wahl eines Server bei der Verbindung ist abhängig von Ping, Server mit der niedrigsten Ping wird ausgewählt
- Heartbeat & Sanity Checks
    - Periodische Überprüfung, dass Systeme laufen und korrekt funktionieren
    - Für jedes Modul separat durchzuführen
- Condition Monitoring
    - Überprüfen, ob sich Prozesse wie erwartet verhalten
    - Denkbar wäre bspw. das erkennen von Prozessen, die in Endlosschleifen gefangen sind

### Fehlerbehebung
- Exception Handling für Module und Funktionen sorgt für geplante Ausnahmebehandlung
- Retry Strategien in Intervallen zur Mitigation von Racing Conditions und temporär nicht verfügbaren Services
- Versionierung der Architektur für Rollbacks
- Graceful degradation
    - Fehlerhafte Module und Funktionen abschalten
    - Setzt funktionierende und umfassende Fehlererkennung voraus
    - Freischaltung nach Fix

### Fehlervermeidung
- Datenbanken arbeiten mit Transaktionen 
- Competence Sets durch umfangreiches Exception Handling erfüllt → siehe Fehlerbehebung 
- Exception Prevention: Die Logik des Codes verhindert Exceptions durch Input Validation, Überprüfen von Array Grenzen, <code>null</code> Werten u.Ä.

### Resilienz
- Isolation: modulare Architektur verhindert Kaputtgehen des gesamten Systems
- Redundanz: Global verteilte Server (siehe Fehlererkennung) realisieren Redundanz unter Verlust einer geringen Ping
- Lose Kopplung durch modulare Architektur und idempotente Kommunikation zwischen Komponenten
- Fallback → siehe Fehlerbehebung
Graceful Degradation of Service → siehe Fehlerbehebung

## Portability
- Installability und Replaceability entfallen, sofern Kompatibilität mit populären Web Browsern (Firefox, Chrome, Edge, Opera, Safari, ...) gewährleistet ist
- Internationalisierung siehe Usability → Accessibility 
## Interoperability 
- Verwendung der Standards JSON und HTTP(S) für den Informationsaustausch mit Dritten 
- Bezug von Daten Dritter über angebotenen Schnittstellen, Anbieten eigener Daten über eigene APIs, inklusive Dokumentation zur Nutzung der APIs
- Einheitliche Syntax und Semantik
## Testability
- Automatische Tests gewährleisten eine umfangreiche Abdeckung
- Unit Tests zum Test einzelner Komponenten, Nutzung von Mockdaten
- Integration Tests mehrer Komponenten, insbesondere nach Veränderung eines Komponenten
- Laufende Tests, kann mit Fehlererkennung / Sanity Checks kombiniert werden



