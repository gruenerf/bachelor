url: http://www.heise.de/developer/artikel/Eine-Einfuehrung-in-Continuous-Delivery-Teil-1-Grundlagen-2176380.html
Autor: Alexander Birk, Christoph Lukas
Titel: Eine Einführung in Continuous Delivery, Teil 1: Grundlagen
Datum: 08.05.2014 - 12:11

Klassische Softwareentwicklung mit Phasenmodell: Entwicklung ->qualitätssicherung -> Auslieferung
    monatelang entwickeln, dann Anforderungen an QS weitgegeben, diese Testet und bessert nach,dann release

Innerhalb der letzten Jahren haben mehr Unternehemen auf inkrementell-iterative Vorgehen umgestellt (Zwischenstände der software werden schon qualitätsgesichert an kunden übergebebn) Kette aus entwicklung, qs und lieferung schon mehrfach im entwicklungsprozess durchlaufen

Bei agilen Methoden gehört auslieferung von lauffähiger Software im rythmus weniger Wochen zum fundament -> manuelle tests blockieren den fluss, testumgebung nicht in genügender anzahl vorhanden, installation mphsam und erst danach kann testen beginnen

Continuous Delivery versucht dem durch automatisierung entgegen zu wirken
    änderungen der software immer getestet, wenn erfolgreich lässt sich das system knopfdruckwendend installiren
    Kette aus entwicklung,qs und, liegerung erfolgt kontinuierlich
    
Jez Humble und Chris reed haben 2006 auf der Agile 2006 in einem Vortrag vorgestellt

In der CD Pipeline wird QS durch kombination aus automatischen und manuellen Tests realisiert
    Unit tests -> komponenten isoliert in ihrer funktion
    akzeptanztests -> einhalten der Anforderungne
    performancetests -> nichtfunktionale Anforderungen
Organisation der Tests in Stufen, die nur durchlaufen wenn vorige Stufe passt

Test Stufen Continuous Delivery Pipeline:
    Commit Stage:
        wird durch Änderung von Versionskontrollsystem ausgelöst
        bauen der Komponenten und ausführen der unit tests
    Acceptance Test Stage (TODO: manuell oder auto):
        Integrations-, akzeptanz- und systemtests
    Manuelle Test- und Freigabeschritte
    
Während Commit und Acceptance tests ergebnisse als feedback(email, instant messages, extreme feedback)
    Fehler können so frühzeitig erkannt werden, durch konstantes starten der tests kann rückschluss auf aktuelle änderungen gemacht werden
    
Technische Umsetzung:
    Abbildung der einzelnen Stufen mit Build Server -> modellierung der einzelnen  Aufgaben in Jobs
    Commitstage: kompilierung der komponenten und ausführen der unit tests
        Wenn erfolgreich: Zusammenfügen der Komponenten zu Bundle und ablegen in Repository
        Weitere Tests auf basis dieses Bundles -> Ebenso deployment
        Übergabe an Akzeptanztests, die software aus sicht des Benutzers testen
        Wenn erfolgreich: Feedback an Entwickler, und eventuelle manuelle Tests
        Wenn alles erfolgreich: Deploy auf Knopfdruck
        
        
2 wichtige prinzipien von CD:
    Testen jeder Änderung der Anwendung
    Softwarestand jedes mal an zentraler stelle gebaut

Was gewinnen Projekte mit CD?
    Große Softwarerelases können zum Scheitern von Projekten führen, da manche funktionen schlecht manuell testbar sind, ebenso lastverhlaten
    CD verschlankt diesen prozess durch den wegfall amnueller aufgaben
    wenn etwas schiefgeht ist auch das rollback nicht allzu kompliziert
    Auch kann durch kleinere Iterationen kundenfeedback direkter geschehen und vermieden werden, dass man an den anforderungen des Kudnen vorbeientwickelt
    Flexibilität durch die möglichkeit zu experimentieren
    Ebenso besseres Feedback für den Entwickleer und damit verbunden auch eine höhere sicherheit ebim entwickeln ->hohe code qualitätt
    Sparpotenzial, da fehler und probleme früher erkannt werden bevor sie größeren schaden anrichten
    
Herausforderungen:
    Verankerung der Tests im Entwicklungsprozess zur Softwarequalitätssicherung
        Hierzu müssen testframeworks evaluiert, know-how muss erworben werden, zeit test zu schreiben muss für eden entwickler zum schreiben eines features dazugehören
        Automatisierung der Tests und ergebnissem
        Bei Umsetzung der Acceptance test stage muss auch deployment automatisiert sein und die KOnfig der Testumgebung stehen
         Erfordert zusammenarbeit von Betriebteam und Entwicklern also einreisen der "silogrenzen" zwischen Dev und Ops
         Qualität des aktuellen Softwarestandes wird transparenter (wer macht änderungen  und welche änderung verursacht fehler)
         
        
        
    