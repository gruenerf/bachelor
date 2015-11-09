#Gliederung:

##Anforderungsanalyse:

###Organisatorisch
- 1 Entwickler vs Teams
- Geografische Distanzen

###Programmatisch
- Verschiedene JS Frameworks
- CMS vs. static content
- Sass vs. Css
- Minifizierung zu Rechen und Speicheroptimierung
- Fehlerüberprüfung
- Unittesting
- Versionierung
- Datenbanken
- modulare Komponenten, die einfach geupdated und installiert werden können
- Rollbacks ermöglichen

###Kundenorientierung
- Unterschiedliche Previewumgebungen
- Agilesoftware Entwicklung für präsentierbare Prototypen (Agile Manifesto)


##IST-Analyse des Workflows:

###Aufsetzen eines Projektes:
- Anlegen git Repo
- Anlegen DB
- Selecting CMS
- Downloading necessary data
- Editing config -> add database name
- Run setup to install the cms
- Setup local server
- Git push initial commit

###During development:
- watch prozesse
- Präprozessoren
- Minifizierung Javascript, uglify und co
- Prefixing
- Bildanpassungen
- Fehlertesting
- Livetesting

###Deployment:
- Build Prozess
- Testing
- Copy files via ftp/sftp to server
- Database deployment
	- Database diff (UUID)
	- Database upload
- Testing, Staging, Production  

###Continous Integration:
- Beschreibung
- Grund
- Verschiedene Buildarten


##Unterstützende-Tools

###Aufsetzen:
- Versionierung: git,svn,mercurial
- Datenbank: mySQL
- Package manager: npm, bower, composer

###During development:
- Automatisierung: Grunt, Gulp, Codekit

###Deployment:
- Gulp, Grunt
- Database diff

###Continous Integration/Continous Delivery /- Deployment:
- Jenkins
- Apache Continuum
- TeamCity
- Travis CI

##Toolauswahl und -verknüpfung
- Ausgewählte Tools / Begründung
- Verknüpfung der Tools zu Gesamtsystem (Skizze)


















