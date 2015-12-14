#Welchen Rahmen hat diese Arbeit?
Diese Arbeit setzt sich mit der Frage auseinander in wie Arbeitsschritte und Prozesse in einem modernen Webprojekt durch Tools begleitet
und unterstützt werden können. Hierzu ist es zu Beginn von Nöten zu definieren was genau ein modernes Webprojekt ist.
Im allgemeinen lässt sich zwischen 4 unterschiedlichen Formen von Webprojekten unterscheiden.
- Das klassische Website Projekt, welches aus einer Frontendausgabe (HTML+CSS+JS) und einem Backend in einer beliebigen Sprache (meistens PHP)
- Die modernere Form des Website Projektes, bestehend aus der Frontendausgabe (HTML+CSS+JS) und einem CMS im Backend (auch zumeist PHP)
- Das reine Backendprojekt, zB die Entwicklung einer API
- Das reine Frontendprojekt, zB die Entwicklung einer APP

#Warum wähle ich einen bestimmten Projekttypen aus mit dem ich mich befasse?
Im weiteren Verlauf wird sich diese Arbeit auf den Projekttyp eines Websiteprojektes mit CMS beschränken, da dieser Projekttyp bei den meisten
Agenturrelevanten arbeiten verwendet wird. Dennoch lassen sich ein Großteil der Aussagen dieser Arbeit auch auf die anderen Projekttypen anwenden.
Abseits der Projektart haben Webprojekte auch ganz allgemeine Anforderungen:

#Welche Anforderungen hat dieser Projekttyp im allgmeinen und an die Projektstruktur?
Die Anforderungen an ein Webprojekt lassen sich in 3 Gruppen aufteilen: organisatorisch, programmatisch, qualitativ

programmatisch:
In den letzten Jahren wurden viele bis dahin standardisierte Techniken durch neuere Techniken, Frameworks oder Programme unterstützt, erweitert und dadurch noch
mächtiger gemacht.

{{ CSS vs Sass }}
{{ JS vs JQuery/AngularJS }}
{{ static Content vs CMS }}

qualitativ:
Codequalität und vor allem die Wiederverwendbarkeit von Code zur steigerung der Produktivität gewinnen mehr und mehr an wichtigkeit.
Gerade in größeren Teams in denen mehrere Personen am gleichen Code arbeiten steigt die Wichtigkeit den Code auf Fehler überprüfen und im Zweifel die Möglichkeit
das Projekt auf den letzten lauffähigen Stand zurückzusetzen zu können.

{{ Qualizeug }}

organisatorisch:
Es müssen Wege gefunden werden in Teams von unterschiedlicher Größe auch zeitlich getrennt von einander an Projekten gemeinsam zu Arbeiten.
Das bedeutet, dass Code zentral verwaltet und immer erreichbar sein muss und weiter, dass der Code parallel von mehreren Personen bearbeitet werden kann,
ohne, dass es dabei zu größeren Fehlern oder im schlimmsten Fall verlust von Code kommen kann.

Weiter führt eine immergrößere Kundenorientierung zu neuen Softwareentwicklungsmethoden wie zB Agile Softwareentwicklung oder FDD, welche ein kontinuiierliches
Prototyping von dem in Entwicklung stehenden Produkt ermöglichen.

{{ Agile Softwareentwicklung }}
{{ FDD }}

#Welche Hilfsmittel gibt es um den Anforderungen gerecht zu werden?
Es gibt bereits einige Tools, welche dem Entwickler dabei helfen diesen Anforderungen gerecht zu werden.
Da es zu jeder Anforderung eine große Anzahl verschiedener, aber alles dem selben Zweck dienlicher Tools gibt, versuche ich im Folgenden diese Anhand zuvor definierter
Kriterien zu Analysieren und zu bewerten:

##Programmatisch:
{{ package manager }}
Da Webprojekte inzwischen auf vielen anderen Projekten und Frameworks aufbauen ist es wichtig diese Dependencies einfach zu verwalten und in der richtigen Version dem Projekt
zuzuordnen.

###Kriterien:
Verfügbare Packages
Nutzeranzahl
Kofiguration
Zuständigkeit
Sonstige Funktionen

{{ automatisierung }}
Aufgrund der häufigen Kompilierung von Sass/Less zu Css Coffescript zu JS, Concatieren und Refactorn, Linting usw. ist es notwendig wenn diese Prozess automatisiert ablaufen.
Automatisierungstools hierfür sind zB. Grunt, Gulp, Codekit

###Kriterien:
Verfügbare Erweiterungen
Nutzeranzahl
Geschwindigkeit
Konfiguration
Open Source

{{ Datenbank Migration }}
Da die meisten Projekte auf einer Datenbank aufbauen ist es natürlich auch wichtig, dass diese nach der lokalen Entwicklung ihren weg auf die jeweilige Deployment Umgebung finden

##Qualitativ:

{{ Testing }}
###Kriterien:
???

##Organisatorisch:

{{ Versionierung }}
###Kriterien:
Unterstützung mehrere Branches
Nutzeranzahl
Geschwindigkeit
Rollback möglichkeit

Um all diese Tools miteinander zu verknüpfen und vor allem an die Projektorganisatorische Schritte zu binden gibt es den Ansatz der verschiedenen DevOps.
DevOps ist ein Zusammenschluss der Worte Development und Operations. Was soviel bedeutet wie eine Kombination aus Organisatorischen und Programmatischen Elementen.

#Könnten diese Hilfsmittel weiter automatisiert und vereinfacht verknüpft werden?
Continous Delivery ist hier das Zauberwort. Bei dem Konzept dreht sich innerhalb eines Projektes alles darum, dass in zeitnahen Abständen Prototypen automatisiert erstellt und
in den jeweiligen Präsentationsumgebungen zur verfügung gestellt werden.

Vorteile hierbei sind: Kundenorientierung, konstantes Testen des Codes, also frühzeitige Fehlererkennung, kurze Integrationsintervalle und dadurch aktuelleres Projekt und keine
großen schwerfälligen Integrationen mehr....
Nachteile: Umgewöhng wenn man andere Softwareentwicklungsmethoden gewohnt ist

Verschiedene Buildarten:
Bei pullrequest,
bei jedem commit,
...

Auch hierfür gibt es einige Tools, welche die Automatisierungen und Buildprozesse verwalten.

###Kriterien:
Community
Open Source
Kostenpflichtig
Umfang
Unterstützte Versionierungen

Umsetzung der Toolkette:

#Wie sieht der Typische Workflow innerhalb eines solchen Projektes aus?

#Welche Tools würden sich idealerweise für eine solche Toolchain eignen und warum?
Meine Wahl der Tools ist auf folgende gefallen

#Wie sieht die angestrebte Architektur der Toolchain aus?

#Evaluation

#Ausblick