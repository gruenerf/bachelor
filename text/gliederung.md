#Bachelorthesis

##Arbeitstitel:
Anforderungsanalyse moderner PHP-basierter Webprojekte und die Erstellung einer auf diesen Anforderungen basierenden Toolchain zur Unterst&uuml;tzung des Entwicklungsworkflows

##Fragestellung:
Mit Hilfe welcher Tools kann der Entwicklungsprozess in modernen Webprojekten gezielt unterst&uuml;tzt und begleitet werden?

##Inhalt:
1. [Anforderungsanalyse moderner Webprojekte](#1)
    - [Projektarten](#1.1)
    - [Organisatorisch](#1.2)
    - [Programmatisch](#1.3)
    - [Qualitativ](#1.4)
2. [IST-Analyse des Entwicklungsworkflows](#2)
    - [Projekterstellung](#2.1)
    - [Development](#2.2)
    - [Deployment](#2.3)
3. [Tools zur Unterst&uuml;tzung des Workflows (Vor- und Nachteile)](#3)
    - [Organisatorisch](#3.1)
    - [Programmatisch](#3.2)
    - [Qualitativ](#3.3)
4. [DevOps: Continuous Integration/ -Delivery / -Deployment](#4)
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


##Gliederung (detail):

###<a name="1"></a>1. Anforderungsanalyse:

####<a name="1.1"></a>1.1 Projektarten: 
- Frontend
- Backend
- Backend (CMS) + Frontend
- Backend (Framework) + Frontend

####<a name="1.2"></a>1.2 Organisatorische Anforderungen
- Einzelner Entwickler vs Team
- Geografische und zeitliche Distanzen zwischen Teammitgliedern
- Agile software Entwicklung f&uuml;r pr&auml;sentierbare Prototypen (Agile Manifesto)
    Feature Driven Development/Scrum

####<a name="1.3"></a>1.3 Programmatische Anforderungen
- CMS vs. static content
- JS Frameworks vs. plain JS
- Sass/Less vs. Css
- Minifizierung zu Rechen- und Speicheroptimierung
- Datenbanken
- Rollbacks erm&ouml;glichen
- Durch Kundenorientierung bedingt: Unterschiedliche Previewumgebungen

####<a name="1.4"></a>1.4 Qualitative Anforderungen
- Fehler&uuml;berpr&uuml;fung
- Versionierung
- Testing (Cross-Browsertesting, UnitTesting, End-to-End) 
- nachhaltiger Code
- Modularit&auml;t und Wartbarkeit
 

###<a name="2"></a>2. IST-Analyse des Entwicklungsworkflows:

####<a name="2.1"></a>2.1 Projekterstellung:
- Initialisieren der Versionierung
- Anlegen DB
- Auswahl des CMS
- Download der n&ouml;tigen Packages
- Editieren der config -> Datenbankzugangsdaten
- Run Setup um das CMS zu installieren
- Setup local server
- Git push initial commit

####<a name="2.2"></a>2.2 Development:
- watch Prozesse
- Pr&auml;prozessoren
- Minifizierung/Vernk&uuml;pfen von Javascript durch Concat, Uglify und co
- CSS-Prefixing
- Bildanpassungen
- Fehler&uuml;berpr&uuml;fung
- Livetesting

####<a name="2.3"></a>2.3 Deployment:
- Build Prozess
- Testing
- Deployment auf Testing, Staging, Production  
- Database Migration
	- Datenbank-diff (UUID)
	- Database upload

###<a name="3"></a>3. Tools zur Unterst&uuml;tzung des Workflows

####<a name="3.1"></a>3.1 Organisatorisch:
- Code-Versionierung: git,svn,mercurial

####<a name="3.2"></a>3.2 Programmatisch
- Package manager: npm, bower, composer
- Automatisierung: Grunt, Gulp, Codekit
- Datenbank-Migration: liquidbase

####<a name="3.3"></a>3.3 Qualitativ
- Linting: Grunt, Gulp, Codekit
- Testing: 
    - Cross-Browser-Testing: 
        - Browserstack
        - Saucelabs
    - Unit-Testing: 
        - JS: 
            - Mocha
            - Jasmine
        - PHP: 
            - PHPUnit 
            - Codeception
    - End-to-End-Testing: 
        - Protractor
        - PhantomJS

###<a name="4"></a>4. DevOps: Continuous Integration/ -Delivery / -Deployment:
- Beschreibung
- Vor- und Nachteile
- Verschiedene Buildarten
- Tools:
    - Jenkins 
    - Apache Continuum
    - TeamCity
    - Travis CI

###<a name="5"></a>5. Erstellung und Dokumentation einer unterst&uuml;tzenden Toolchain
- Zielsetzung / Featurelist
- Toolauswahl + Begr&uuml;ndung
- Architektur Gesamtsystem
- Konfigurationsbeschreibung Einzelkomponenten
- Funktionsweise / Bedienung

###<a name="6"></a>6. Anwendung der Toolchain in der Praxis
- Projektbeschreibung
- Definition der Bewertungskriterien
- Bewertung der Toolchain

###<a name="7"></a>7. Ausblick


















