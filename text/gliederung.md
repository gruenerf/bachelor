#Bachelorthesis

#Arbeitstitel:

Anforderungsanalyse agiler, nach Scrum organisierter, PHP-basierter Websiteprojekte und die Erstellung einer auf diesen Anforderungen basierenden Toolchain zur Unterstützung des Entwicklungsworkflows

#Fragestellung:

Mit Hilfe welcher Tools kann der Entwicklungsprozess in Scrum Teams bei der Umsetzung von Webprojekten auf organisatorischer und programmatischer Ebene gezielt unterstützt und begleitet werden?

#Inhalt:
0. [Einleitung](#0)
1. [Anforderungsanalyse mit Scrum organisierter Websiteprojekte](#1)
    - [Beschreibung Scrum](#1.1)
    - [Ziele Scrumprojekt](#1.2)
    - [Scrum-Rollen](#1.3)
      - [Product-Owner](#1.3.1)
      - [Scrum-Master](#1.3.2)
      - [Scrum-Team](#1.3.3)
    - [Scrum-Prozesse](#1.4)
      - [Erstellung Product Backlog](#1.4.1)
      - [Sprint Planung + Sprint Backlog](#1.4.2)
      - [Sprint](#1.4.3)
      - [Daily Scrum (Burndown Chart)](#1.4.4)
      - [Sprintabschluss](#1.4.5)
      - [Nachbereitung](#1.4.6)
2. [Tools zur Unterstützung des Workflows (Vor- und Nachteile)](#2)
    - [Allgemeine Projekt Unterstützung (Scrum Tools)](#2.1)
    - [Sprint Unterstützung](#2.2)
      - [Entwickler](#2.2.1)
      - [Testing](#2.2.2)
      - [Build + Deploy](#2.2.3)
3. [Erstellung und Dokumentation der Toolchain](#3)
    - [IST-Analyse des Entwicklungsworkflows](#3.1)
        - [Projekterstellung](#3.1.1)
        - [Development](#3.1.2)
        - [Deployment](#3.1.3)
    - Zielsetzung / Featurelist
    - Toolauswahl + Begrüdung
    - Architektur Gesamtsystem
    - Konfigurationsbeschreibung Einzelkomponenten
    - Funktionsweise / Bedienung
4. [Anwendung der Toolchain in der Praxis -> Evaluation](#4)
    - Projektbeschreibung
    - Definition der Bewertungskriterien
    - Bewertung der Toolchain
5. [Ausblick](#5)


#Gliederung (detail):

##<a name="0"></a>0. Einleitung:
    - Herleitung
    - Relevanz des Themas
    - Fragestellung
    - Struktur der Arbeit
    - Zielsetzung

##<a name="1"></a>1. Anforderungsanalyse mit Scrum organisierter Websiteprojekte:

###<a name="1.1"></a>1.1 Beschreibung Scrum
    - Framework für agile Entwicklung
    - Agiles Manifest
    - "Agile Software Development with Scrum ", Ken Schwaber / Mike Beedle
    - Scrum Ablauf

###<a name="1.2"></a>1.2 Ziele von Scrum
    - Präsentierbare Prototypen nach jeder Integration
    - Mensch steht im Mittelpunkt (Team oder Kunde)

###<a name="1.3"></a>1.3 Scrum Rollen
####<a name="1.3.1"></a>1.3.1 Product-Owner
    - verantwortlich für Eigenschaften (erstellung + prio) und wirtschaftl. Erfolg des Produkts
    - 1 Person
    - Stakeholderkontakt
    - Rahmenbedingungen

####<a name="1.3.2"></a>1.3.2 Scrum-Master
    - verantwortlich für Erfolg von Scrum
    - Führungskraft
    - Teammitglied oder nicht

####<a name="1.3.3"></a>1.3.3 Scrum-Team
    - Arbeitet an der Umsetzung der Funktionalitäten
    - Hat alle Kompetenzen zur Umsetzung des Projektes
    - Schätzung des  Entwicklungsaufwand

###<a name="1.4"></a>1.4 Scrum Prozesse
####<a name="1.4.1"></a>1.4.1 Erstellung Product Backlog
    - In Absprache Zwischen PO und Stakeholder
    - Möglichst korrekte Schätzung von Zeit/Kosten Aufwand
    - Featureliste
    - nicht zwingend final

####<a name="1.4.2"></a>1.4.2 Sprint Planung + Sprint Backlog
    - Einfachheit
    - Modularität der Features

####<a name="1.4.3"></a>1.4.3 Sprint
    - Versionierung
    - CMS bzw. PHP inkl Datenbank vs. static content
    - JS Frameworks vs. plain JS
    - Sass/Less vs. Css
    - Minifizierung zu Rechen- und Speicheroptimierung
    - Rollbacks ermöglichen
    - Durch Kundenorientierung bedingt: Unterschiedliche Previewumgebungen
    - Testing (Cross-Browsertesting, UnitTesting, End-to-End)
    - Linting
    - Automatisierung
    - nachhaltiger Code

####<a name="1.4.4"></a>1.4.4 Daily Scrum (Burndown Chart)
    - Meeting mit Team
    - Aktuelle Schwierigkeiten/Arbeiten

####<a name="1.4.5"></a>1.4.5 Sprintabschluss
    - Build + Deployment

####<a name="1.4.6"></a>1.4.6 Nachbereitung
    - Erstellung neues Sprint Backlog
    - Veränderungen für zukünftige Sprints anhand Analyse der vergangen Prozesse

##<a name="2"></a>2. Tools zur Unterstützung des Workflows
###<a name="2.1"></a>2.1 Allgemeine Projekt Unterstützung (Scrum Tools)
    - Ticketing System: GitLab, Git Issues, Mantis, trello
    - Code-Versionierung: git,svn,mercurial     
    - Scrum Tools: Vivify, flying donut, scrum wise, scrumdo, taiga

###<a name="2.2"></a>2.2 Sprint Unterstützung
####<a name="2.2.1"></a>2.2.1 Sprint Entwicklung
    - Package manager: npm, bower, composer
    - Automatisierung: Grunt, Gulp, Codekit
    - Entscheidung für CMS/PHP-Framework

####<a name="2.2.2"></a>2.2.2 Sprint Testing
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
            
####<a name="2.2.3"></a>2.2.3 Sprint Build + Deploy
    - Datenbank-Migration: liquidbase
    - Continuous Deployment:
      - Jenkins
      - Apache Continuum
      - TeamCity
      - Travis CI

##<a name="3"></a>3. Erstellung und Dokumentation einer unterstützenden Toolchain
###<a name="3.1"></a>3.1 IST-Analyse des Entwicklungsworkflows:
####<a name="3.1.1"></a>3.1.1 Projekterstellung:
    - Initialisieren der Versionierung
    - Anlegen DB
    - Auswahl des CMS
    - Download der nötigen Packages
    - Editieren der config -> Datenbankzugangsdaten
    - Run Setup um das CMS zu installieren
    - Setup local server
    - Initial commit in der Versionierung

####<a name="3.1.2"></a>3.1.2 Development:
    - watch Prozesse
    - Präprozessoren
    - Minifizierung/Vernküpfen von Javascript durch Concat, Uglify und co
    - CSS-Prefixing
    - Bildanpassungen
    - Fehlerüberprüfung
    - Livetesting

####<a name="3.1.3"></a>3.1.3 Deployment:
    - Build Prozess
    - Testing
    - Deployment auf Testing, Staging, Production  
    - Database Migration
        - Datenbank-diff (UUID)
        - Database upload
- Zielsetzung / Featurelist
- Toolauswahl + Begründung
- Architektur Gesamtsystem
- Konfigurationsbeschreibung Einzelkomponenten
- Funktionsweise / Bedienung

##<a name="4"></a>4. Anwendung der Toolchain in der Praxis
- Projektbeschreibung
- Definition der Bewertungskriterien
- Bewertung der Toolchain

##<a name="5"></a>5. Ausblick
