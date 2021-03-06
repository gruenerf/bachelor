1 Scrum löst eure Probleme nicht
    Scrum erwartet von Product owner die einzelnen Feature zu Bewerten und anhand der bewertung zu priorisieren
    -> dadurch weiß das Team genau was als nächstes umzusetzen ist
    Scrum behebt das Problem nicht, dass es schwer ist punkte zu priorisieren, sondern es "zwingt" uns dazu das projekt besser zu verstehen
    Der Product owner muss sich diese gedanken machen und sich mit stakeholdern abstimmen -> permanentes reflektieren
    -> Strukturierteres Projekt
    Burndown chart im Sprint visualisiert den Fortschritt -> zeigt entwicklern auf wann sie hinterherhinken und wann gut sind
    -> werkzeug um Probleme aufzuzeigen nicht aber zu lösen
           
4 Klassisches Vorgehen
    Abschluss eines Projektes durch strukturiertes Abarbeiten der anfallenden Aufgaben. Optimierung durch konkrete Vorgehensmodelle:
    Früher: vmodell, wasserfallmodell
    heute: agile techniken
    Probleme mit alten Methoden: sind nciht auf schnellebiges internetbusiness ausgelegt, da zu starr
        änderungen sind nicht geplant (alles vorher definiert) doch features werden konstant weiterentwickelt
    Abschlusshektik kann so vermieden werden
           
8 Scrum- man muss nicht alles verstehen
    Im webumfeld ist es schwer von beginn an alles zu spezifizieren, da der kunde oft nicht weiß was er überhaupt will
    Definition und abgeschlossenes Projekt sind oft komplett unterschiedlich
    Bei scrum versucht man daher features erst spät festzulegen/konkretisierenn. durch die iterationen hat man auslieferbare produkte
    falls das budget nicht reicht können gewisse features nicht umgesetzt werden man hat aber dennoch ein ausliegerbares prdukt
    schätzungen ohne personentage
        Schötzung über story points. Was diese bedeuten wird in der praxis meist nach 3 sprints berechnet -> führt zu präzisen schätzungen
    selbstbestimmung des teams:
        Sprintplanung- in ersten 2 sprints über- und unterschätzen sich die teams jeweils. pendelt sich beim 33. sprint ein
    
10 Das agile Manifest
    Februas 2001 17 kulge köpfe (kent back, martin fowler, alistair cockburn, ken schwaber) 
    
28  Test Driven Development
    - schreiben der Tests bereits im Vorfeld (S.79)
    - dann durchführen der Unittests
    - nach und nach von rot zu grün
    - implementieren der Methoden
    - erst wenn  jeder Test vollständig durchläuft ist die Klasse einsatzbereit

    -> führt zu einfachen Klassen und Strukturen, da keine Untestbaren Methoden entwickelt werden
    -> Fokussierung auf eigentliche Anforderungen

38 Regeln lernen um sie richtig zu brechen
    Regeln zu Brechen, auch bei Srum ist ok, nur muss man dazu die Hintergründe verstanden haben und realisieren, dass möglicherweise das Komplette Proinzip dadurch kaputt gehen kann, da Gruppenpsychologische Faktoren nicht mehr berücksichtigt werden können
      (S.101) -> allerdings ist das brechen durch alternative Wege eben bessser, da diese die Hintergründe auch berücksichtigen (S.102)

39 qualitätssicherung (s.104f)
        Unittests -> abdeckung 80%
        reviews -> 4 augen prinzip für code
        statische codanalyse -> ohne zutun und daher kostenlos
        lasttest
        funktionale systemtests -> als ergänzung zu codetests
        akzeptanztes um Kundenakzeptanz zu erfragen

52 codequalität (S.131f)
  Agile Methoden und spontaneÄnderungen können in Code murks enden-> lange skripte, wenig kommentare und damit schlechter wartbarkeit

53 Fünf augen und der Code (133ff)
  Automatisierung als fünftes Auge -> Simple Tasks wie einhalten der Formatierung, Softwaremetriken, syntaax fehlern, ob unit tests ausreichen

58 Contiuous Integration (147ff)
  Grundideen:
    1. Kontinuierliches Bauen des Gesamtsystems
    2. Frühzeitiges und regelmäßiges Einchecken in die versionsverwaltung

    Das kontinuierliche Bauen von CI-Server übernommen -> um nach jedem Commit zu überprüfen ob das programmierte im Gesamtsystem funktioniert
    Voraussetzung: hohe automatisierte Testabdeckung (wir  von Skriopten übernommen die Testresultate erzeugen)
    Wenn tests gut geschrieben kann anhand des ergebnisses bestimmt werden ob system funktioniert
    Kontinuierliches Schreiben von Tests
    Hilft, dass entwickler eine Applikation nicht "kaputtprogrammieren" könen

59 Wie automatisierte Tests den Verstand erweitern
    Automatisierte Tests - primär Programmiertechnik und sekundär Qualitätssicherung
    Entwerfen von Tests ist integraler Bestandteil des Kodierens (gleich wie eingreifen in Produktivcode)
    In den Testcode werden informationen einprogrammiert und somit in verständliche,persistente Form gebracht, die Sonst nur im Kopp des Programmieres befinden

60 Continous Testing
    Anpassung des CI-Servers auf den eigenen Qualitätsanspruch. ZUmeist beginn mit der Ausführung voin Unittests
    testarten:
      Unittests: Überprüfen Codeebene auf korrektheit
      Statische Codeanalyse: Erkennung Code-Smells, Softwaremetriken -> Wichtig, dass man Verstöße ignorieren kann (Da metriken nur indikatoren nicht aber fixe aussage sind)
      Funktionale Tests: Simulation des Nutzers der sich durch das Angebot klickt, Überprüft korrekte Integration (Zusammenspiel der einzelnen Systemkomponenten)
      Continuous Performace: Geschwindigkeitstests (zB. Abfrage URL -> Antwortzeit)
      Syntaktische Prüfung: Sollte in Versiosverwaltung integriert werden, da es keinen Compiler gibt der den fehlerhaften Code frühzeitig erkennt -> Saher gefahr, dass es in Produktion landet

      Problem an vielen Tests ist, dass wenn alle ausgeführt werden -> zeitraubend
      Daher abhängigkeit:
        Erst syntaktische korrektheit
        (-> sonst failen) Unit tests
        (-> sonst failen) funktionale Tests
