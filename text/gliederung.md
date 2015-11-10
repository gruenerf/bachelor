#Inhalt:
1. [Anforderungsanalyse moderner Webprojekte](#1)
    - [Organisatorisch](#1.1)
    - [Programmatisch](#1.2)
    - [Softwarequalität](#1.53)
2. [IST-Workflow](#2)
3. [Tools zur Unterst&uuml;tzung des Workflows (Vor- und Nachteile)](#3)
4. [Auswahl bestimmter Tools f&uuml;r eine Toolchain](#4)
5. [Erstellung und Dokumentation der Toolchain](#5)
6. [Erstellung eines Projektes mit der Toolchain -> Evaluation](#6)
7. [Ausblick](#7)


#Gliederung (detail):

##<a name="1"></a>Anforderungsanalyse:

###<a name="1.1"></a>Organisatorisch
- 1 Entwickler vs Team
- Geografische Distanzen
- Agile software Entwicklung f&uuml;r pr&auml;sentierbare Prototypen (Agile Manifesto)
    Feature Driven Development/Scrum
- Durch Kundernorientierung bedingt: Unterschiedliche Previewumgebungen

###<a name="1.2"></a>Programmatisch
- CMS vs. static content
- Verschiedene JS Frameworks
- Sass vs. Css
- Minifizierung zu Rechen und Speicheroptimierung
- Datenbanken
- Rollbacks erm&ouml;glichen

###<a name="1.3"></a>Softwarequalität
- Fehler&uuml;berpr&uuml;fung
- Versionierung
- Unittesting
- nachhaltiger Code
- Modularit&auml;t und Wartbarkeit
 

##<a name="2"></a>IST-Analyse des Workflows:

###<a name="2.1"></a>Aufsetzen eines Projektes:
- Anlegen git Repo
- Anlegen DB
- Selecting CMS
- Downloading necessary data
- Editing config -> add database name
- Run setup to install the cms
- Setup local server
- Git push initial commit

###<a name="2.2"></a>During development:
- watch prozesse
- Pr&auml;prozessoren
- Minifizierung Javascript, uglify und co
- Prefixing
- Bildanpassungen
- Fehlertesting
- Livetesting

###<a name="2.3"></a>Deployment:
- Build Prozess
- Testing
- Copy files via ftp/sftp to server
- Database deployment
	- Database diff (UUID)
	- Database upload
- Testing, Staging, Production  

###<a name="2.4"></a>Continous Integration:
- Beschreibung
- Grund
- Verschiedene Buildarten


##<a name="3"></a>Unterst&uuml;tzende-Tools

###<a name="3.1"></a>Aufsetzen:
- Versionierung: git,svn,mercurial
- Datenbank: mySQL
- Package manager: npm, bower, composer

###<a name="3.2"></a>During development:
- Automatisierung: Grunt, Gulp, Codekit

###<a name="3.3"></a>Continous Integration/Continous Delivery /- Deployment:
- Jenkins
- Apache Continuum
- TeamCity
- Travis CI

###<a name="3.4"></a>Deployment:
- Gulp, Grunt
- Database diff

##<a name="4"></a>Toolauswahl und -verkn&uuml;pfung
- Ausgew&auml;hlte Tools / Begr&uuml;ndung
- Verkn&uuml;pfung der Tools zu Gesamtsystem (Skizze)


##<a name="5"></a>Erstellung und Dokumentation der Toolchain
- Zielsetzung
- Projektplan
- Beschreibung der Konfiguration der Einzelkomponenten
- Beschreibung des Zusammenwirkens

##<a name="6"></a>Evaluation der Toolchain anhand eines Webprojektes
- Projektbeschreibung
- Definition der Bewertungskriterien
- Bewertung der Toolchain

##<a name="7"></a>Ausblick


















