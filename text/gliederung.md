#Inhalt:
1. [Anforderungsanalyse moderner Webprojekte](#1)
    - [Organisatorisch](#1.1)
    - [Programmatisch](#1.2)
    - [Qualitativ](#1.3)
2. [IST-Analyse des Entwicklungsworkflows](#2)
    - [Projekterstellung](#2.1)
    - [Development](#2.2)
    - [Deployment](#2.3)
3. [Tools zur Unterst&uuml;tzung des Workflows (Vor- und Nachteile)](#3)
    - [Organisatorisch](#3.1)
    - [Programmatisch](#3.2)
    - [Qualitativ](#3.3)
4. [Continuous Integration/ -Delivery / -Deployment](#4)
    - Beschreibung
    - Vor- und Nachteile
    - Verschiedene Buildarten
    - Tools
5. [Erstellung und Dokumentation der Toolchain](#5)
    - Zielsetzung / Featurelist
    - Toolauswahl + Begr&uuml;dung
    - Architektur Gesamtsystem
    - Konfigurationsbeschreibung Einzelkomponenten
    - Funktionsweise / Bedienung
6. [Anwendung der Toolchain in der Praxis -> Evaluation](#6)
    - Projektbeschreibung
    - Definition der Bewertungskriterien
    - Bewertung der Toolchain
7. [Ausblick](#7)


#Gliederung (detail):

##<a name="1"></a>Anforderungsanalyse:

###<a name="1.1"></a>Organisatorisch
- Einzelner Entwickler vs Team
- Geografische und zeitliche Distanzen zwischen Teammitgliedern
- Agile software Entwicklung f&uuml;r pr&auml;sentierbare Prototypen (Agile Manifesto)
    Feature Driven Development/Scrum

###<a name="1.2"></a>Programmatisch
- CMS vs. static content
- JS Frameworks vs. plain JS
- Sass/Less vs. Css
- Minifizierung zu Rechen- und Speicheroptimierung
- Datenbanken
- Rollbacks erm&ouml;glichen
- Durch Kundenorientierung bedingt: Unterschiedliche Previewumgebungen

###<a name="1.3"></a>Qualitativ
- Fehler&uuml;berpr&uuml;fung
- Versionierung
- Unittesting
- nachhaltiger Code
- Modularit&auml;t und Wartbarkeit
 

##<a name="2"></a>IST-Analyse des Entwicklungsworkflows:

###<a name="2.1"></a>Projekterstellung:
- Anlegen git Repo
- Anlegen DB
- Selecting CMS
- Download der n&ouml;tigen Packages
- Editieren der config -> Datenbankzugangsdaten
- Run Setup um das CMS zu installieren
- Setup local server
- Git push initial commit

###<a name="2.2"></a>Development:
- watch Prozesse
- Pr&auml;prozessoren
- Minifizierung/Vernk&uuml;pfen von Javascript durch Concat, Uglify und co
- CSS-Prefixing
- Bildanpassungen
- Fehler&uuml;erpr&uuml;ung
- Livetesting

###<a name="2.3"></a>Deployment:
- Build Prozess
- Testing
- Deployment auf Testing, Staging, Production  
- Database deployment
	- Database diff (UUID)
	- Database upload

##<a name="3"></a>Tools zur unterst&uuml;tzung des Workflows

###<a name="3.1"></a>Organisatorisch:
- Versionierung f&uuml;r shared Code: git,svn,mercurial

###<a name="3.2"></a>Programmatisch
- Package manager: npm, bower, composer
- Automatisierung: Grunt, Gulp, Codekit
- Database diff: liquidbase

###<a name="3.3"></a>Qualitativ
- Testing: Grunt, Gulp, Codekit

##<a name="4"></a>Continuous Integration/ -Delivery / -Deployment:
- Beschreibung
- Vor- und Nachteile
- Verschiedene Buildarten
- Tools:
    - Jenkins
    - Apache Continuum
    - TeamCity
    - Travis CI

##<a name="5"></a>Erstellung und Dokumentation einer unterst&uuml;tzenden Toolchain
- Zielsetzung / Featurelist
- Toolauswahl + Begr&uuml;ndung
- Architektur Gesamtsystem
- Konfigurationsbeschreibung Einzelkomponenten
- Funktionsweise / Bedienung

##<a name="6"></a>Anwendung der Toolchain in der Praxis
- Projektbeschreibung
- Definition der Bewertungskriterien
- Bewertung der Toolchain

##<a name="7"></a>Ausblick


















