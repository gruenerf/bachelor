url: http://martinfowler.com/articles/continuousIntegration.html
Date. 01.05.2006
autor: martin fowler

CI is a developmnet practice where members of a team integrate their work fequently, usually each person integrates at least daily

Früher :Integration is a long and unpredictable process

Integration als "non-event" -> jede Änderung ist lediglich einige Stunden entfernt um zu einem geteilten Projektstand zu werden. Fehler werdens chnell gefunden und können behoben werden

Geheimnis: Jeden tag zu integrieren nter zu hilfe eines vcs

Der begriff "continous integration" entstand im Extreme Programming Prozess, als eine der 12 praktiken.

Obwohl CI kein spezielles Tool zum deploy braucht, ist die verwendung eines CI servers dennoch ratsam

Ablauf CI:
    Auschecken des source codes
    Verändern je nachdem was man machen will und ergänzen von oder ändern bestehender tests
    Automatisierter build auf dem development rechner
        -> KOmpiliert und ausführen von tests
        -> wenn alle tests klappen gilt der build als gut
        -> wenn jmd anderes bereits zum master commited bevor man selbst commited integrieren des neuen codes in den eigenen und erneut builden
        -> Commit zum master
        -> Erneuter build mit dem master code
        -> Wenn dieser Build klappt, dann ists fertig

Praktiken CI:
    Ein Zentrales Quell Repository:
        Software besteht aus vielen dateien um gebaut zu werden, diese zu managen vor allem in großen Teams kann mitunter sehr kompliziert werden
        Daher SCM
        Wichtig eine mainline (master) zu haben
    
    Automatisiere den Build
        Um den Quellcode zu einem funktionierenden System zu verwandeln ist ein komplizierter Prozess
        (Compilation, dateien rumschieben, Datenbank aktualisieren,...) 
        
    Selbsttestender Build   
        traditionell bedeutet build compilieren, verknüpfen und ein programm ausführbar zu machen.
        modern würde bedeuten, dass sicher der code währenddessen auch noch selbst überprüft
        Hierzu müssen tests (TDD-Style) geschrieben werden um sie später automatisier von einer Testsuite zuüberprüfen zu lassen
     
    Jeder commited zur mainline jeden Tag
        Integration basiert af kommnunikation
        durch die Integration in die Mainline und das passieren der tests werden probleme zwischen einzelnen Entwicklern frühzeitigaufgedeckt
        
    jeder Commit sollte die mainline auf einer Integrations Maschine builden
        Tägliche Commits führen dazu, dass das Team stetig getestete builds bekommt und die mainline sauber bleibt
        In der praxis kann es aber dnnoch zu problemen kommen, wenn entwickler ihren code nicht updaten oder es unterschiede in der Entwicklungsumgebung gibt
        Entweder manueller build, bei dem der Entwickler nach seinem Commit an den Integrationsrechner geht und den build manuell ausführt -> wenn alles gut geht ist erfertig
        Integrationsserver automatisiert diesen prozess und builded nach jedem commit automatisch und gibt feedback
        
    Direkte korrektur kaputter builds:
        Eine schlüsselkomponente von continuous integration ist, dass wenn ein mainline build fehlschlägt, die mainline direkt repariert wird. Denn der Hauptgedanke bei der arbeit mit  ci ist, dass das gesamte team auf basis einer soliden codebasis arbeiten.
        
    Der Build soll schnell bleiben:
        Der Grund für CI ist das bereitstellen von schnellem Feedback. 
        Wenn der build zu lange braucht kann dieser Punkt nicht gewährlesitet werden
        Annehmbare Dauer ist abhängig vom Projekt (XP Richtlinie: 10minuten)
    
    Testen in einem Klon der Production umgebung
        Ziel von Tests ist das beseitigen aller möglicher Probleme die das System in Production haben könnte
        Wenn man in einer anderen Umgebung testet kann dies dazufürhen, dass ein rstrisiko bleibt, dass die tests in production fehlschagem.
        Daher Testumgebung = Duplikat von Production (Gleiche Versionen, Datenbanksytem und OS, Verwenden der gleichen ip und ports, ebenso die selbe Hardware)
    
    Zugang zur neusten ausführbaren version einfach gestalten:
        Da Probleme meist erst entdeckt werden wen ein Blick auf die Softwaregeweorfen wird sollte der Zugang auch für den Kunden und interne Präsentationen verienfacht werden
    
    Jeder sieht was passiert
        Bei Ci geht es vor allem um Kommunikation -> das bedeutet, dass jeder einfach den aktuellen Stand des Systemes und damit verbunden die änderungen einsehen kann
        Vor allem der Stand der mainline muss einfach einsehbar sein
        Ci server helfen hierbei mit einer änderungshistory und den einzelnen änderungen die einzlene nutzer gemacht haben
        
    Automatisiertes Deployment
        Um CI benutzen zu können bedarf es meherer Umgebungen, eine um Commit Tests laufen zu lassen und eine um sekundäre tests auszuführen. Da man Code mhermals pro tag zwischen diesen Servern hin ud gerschiebt möchtee man das automatisieren. Das bedeutet es müssen skripts existiere welche diese aufgabe automatisieren
        Gleiche scripts auch für deploy in production. Dann aber ergänzt durch evtl rollbacjks
        
Nutezn von CI:
    
        