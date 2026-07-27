# Herkunft der Regeln

Nur lesen, wenn eine Regel im Skill unnötig streng wirkt. Jede hier genannte Regel steht dort, weil ihr Fehlen einmal konkret Punkte gekostet hat.

Erprobt in der Klausurenphase Sommer 2026 an einem Durchlauf Visual Computing: 12 Themen, Baseline Null, rund zwei Tage. Alle sieben Fehler unten stammen aus diesem Durchlauf (23.–25.07.2026).

## Was getragen hat

- **Zustand in Dateien statt im Chat.** Überlebt Sitzungsabbrüche, Kontextlimits und Modellwechsel.
- **Ausdrücklicher Start ohne Rückfragen.** Der teuerste Moment ist der Einstieg, nicht das Lernen.
- **Zerlegte Originalaufgaben.** Von Null auf lösbar in Minuten statt Stunden — der wirksamste Einzelbaustein.
- **Fester Dialogrhythmus, flexible Schrittgröße.** Erklären → eine Anwendung → warten trug durchgehend; sobald das Prinzip saß, wurden unnötige Minischritte dagegen als störend erlebt.
- **Ehrliches Sitzungsprotokoll**, das Fehler notiert und nicht nur Erfolge. Es ist die Grundlage der Fehlerliste und des Spickzettels.
- **Aktive Reparaturschleife** (fehlende Voraussetzung gezielt erklären → neue Anwendung → korrekt) statt dieselbe allgemeine Erklärung nur zu wiederholen.
- **Nachweispflicht für Stufenerhöhungen.** Der einzige Schutz gegen Selbsttäuschung.

## Die sieben Fehler

1. **Die offizielle Themenliste wurde nie als Checkliste gegen den Status gelegt.** Der Lernplan kam aus der Altklausur. Folge: fünf ausdrücklich angesagte Themen fielen komplett durchs Raster.
   → Jeder Punkt der Themenliste wird beim Anlegen genau eine Statuszeile ([`setup.md`](setup.md) §2).

   **Teuer gelernte Ergänzung:** Die Themenliste taugt als Einschluss-, nicht als Ausschlusskriterium. Texturen fehlten auf der Liste; auf direkte Nachfrage sagte der Prof im Transkript aber, er würde sie „nicht komplett ausschließen". Deshalb der Abgleich **beider** Quellen vor dem ersten Lernblock (§3–4).

2. **Statische Themenreihenfolge statt Punkte pro Aufwand.** Ein 10-Punkte-Rechenschema, das in 40 Minuten gesessen hätte, stand auf Platz 10 und blieb offen — während an bereits sitzenden Themen nachpoliert wurde.
   → Priorität wird mindestens einmal pro Lernblock neu berechnet.

3. **Die Stufe `stabil` wurde faktisch nie verwendet.** Die Schleife optimierte konsequent bis `übungsfähig` und zog weiter — breit statt tief. Bis kurz vor der Klausur gab es damit keinerlei Evidenz über die Leistung ohne Hilfe.
   → Die gemischte Wiederholung ohne Hinweise ist ein eigener, terminierter Schritt. Und: `stabil` entsteht nie im selben Block wie `übungsfähig`, weil der Zeitversatz Teil des Nachweises ist.

4. **Die Probeklausur hatte kein Datum.** Sie stand als letzter Punkt der Abschlussphase und wäre bei Zeitdruck als Erstes ausgefallen — obwohl sie der einzige echte Messpunkt ist.
   → Fester Termin beim Anlegen des Plans, rückwärts vom Klausurdatum mit Puffertag.

5. **Hilfsmittel-Logistik wurde nicht früh geklärt** — handschriftlich oder gedruckt, Taschenrechnertyp, Raum, Ausweis.
   → Checkliste beim Anlegen, nicht am Vorabend.

6. **Der Spickzettel wuchs ungebremst.** Er muss am Ende auf die erlaubte Fläche passen; ohne laufende Verdichtung wird das ein Arbeitsabend direkt vor der Klausur.
   → Ab der Hälfte der Themen bei jeder Aufnahme einen Eintrag streichen oder zusammenfassen.

7. **Es wurde geprüft, bevor das nötige Wissen vermittelt war.** Im VC-Durchlauf wurden unter anderem `location`, `uniform` sowie `out`/`in` abgefragt, bevor ihre Bedeutung beziehungsweise die Shader-Pipeline erklärt war. Der Lernende musste mehrfach mit „keine Ahnung" oder dem ausdrücklichen Hinweis auf Nullwissen die Erklärung erst auslösen. Ursache war die konkrete Anweisung „Aufgabe unter Klausurbedingungen", während „Baseline Null" nur allgemein und die Materialnutzung reaktiv formuliert war.
   → Baseline Null ist die bekannte Ausgangslage, kein erst zu diagnostizierender Fehler. Vor jedem Teilschritt die nötige Wissensvoraussetzung aus den Kursquellen beschaffen und erklären; Klausurbedingungen gelten erst für eine neue Nachweisvariante am Stück.

## Spätere Nachträge

- **Hilfestufe im Nachweis.** Ohne sie liest sich eine stark geführte Lösung im Status wie eine eigenständige, und die Stufe wirkt besser, als sie ist.
- **Punkte und Stufe getrennt führen.** Eine Originalaufgabe kann nach Führung vollständig verstanden sein und unter Klausurbedingungen trotzdem nur 4/6 wert gewesen sein. Beides ist eine eigene Information.
- **Antwortumfang respektieren.** Bereits erbrachte Zwischenschritte erneut zu verlangen, kostet Zeit und Motivation und misst nichts Neues.
- **Adaptive Themenwechsel statt harter Quote.** Ein Abbruchkriterium verhindert endloses Nachpolieren, aber feste Minuten- oder Aufgabenzahlen verzerren den unterschiedlich großen Lernaufwand. Deshalb an natürlichen Aufgabenschnitten anhand von Restzeit, offenen Themen, Fortschritt und Nähe zum Nachweis neu priorisieren.

## Fachübergreifende Testbefunde vom 27.07.2026

Nach der VC-Erprobung liefen isolierte Starts für Rechnernetze und Wissenschaftliches Arbeiten nur aus den jeweiligen Rohquellen, ohne bestehende Lernstände oder frühere Chats.

8. **Eine breite Themenzeile verdeckte fehlende Transferaufgaben.** Der RN-Start bündelte „L3 Routing und IP“ in einer Zeile und fand Dijkstra sowie Subnetting sofort. Erst ein ausdrücklicher Abdeckungs-Audit entdeckte, dass keine fertige Papieraufgabe den vollständigen Paketweg über mehrere Netze mit Routingentscheidung, ARP sowie wechselnden MAC- und gleichbleibenden IP-Adressen verband.
   → Offizielle Überschriften werden in getrennt nachweisbare Kompetenzbausteine übersetzt. Vor Abschluss eines breiten Themas wird vorhandener Aufgabenpool gegen verlangte Handlungen geprüft; ungedeckte Abläufe bekommen quellenbasierte Transfer- oder Syntheseaufgaben.

9. **Unbekannte Hilfsmittel führten zu unterschiedlichem Artefaktverhalten.** RN legte wegen ausdrücklichen Verbots korrekt keinen Spickzettel an; WAI erzeugte bei unbekannter Zulassung vorsorglich eine leere Spickzettel-Datei. Beide Agenten folgten derselben Skill-Version.
   → Spickzettel-Datei nur bei bestätigter Zulassung. Bei unbekanntem Status bleiben Kandidaten im Lernstatus; bei Verbot werden Lernhilfen in Nachweisen nicht benutzt.

10. **Starre Abschlussdaten kollidierten fachübergreifend.** Die isolierten Setups legten jede Probeklausur auf den Vortag. Bei RN am 06.08. und WAI am 07.08. landete dadurch die WAI-Probeklausur auf dem RN-Klausurtag.
    → Abschlussfenster zwischen Fächern koordinieren. Termine bleiben Anker; bei jedem tatsächlichen Lernstart gewinnt der aktuelle Stand und die jetzt sinnvollste Aufgabe, nicht ein verpasster Plan.

11. **„Prüfbarer Baustein“ blieb ohne Entscheidungstest agentenabhängig.** Im ersten Regressionslauf hatte RN zwar schon 20 statt 7 Statuszeilen, bündelte aber weiterhin IPv4/IPv6, ARP/NDP, ICMP und Traceroute; WAI führte einen Workflow-Sammelpunkt zusätzlich zu seinen Einzelteilen.
    → Eine Zeile darf nur zusammenbleiben, wenn eine realistische Kontrollvariante alles darin fair nachweisen kann. Breite Doppelungen tragen keine eigene Stufe; eine Synthesezeile nur dann, wenn das Zusammenspiel selbst eine zusätzliche Leistung ist.

12. **Vorbereitung erzeugte Lernartefakte ohne Lernnachweis.** WAI trug beim Setup bereits einen Workflow-Spickzettelkandidaten ein und legte eine dauerhafte Block-Prep-Datei an, bevor die erste Antwort vorlag.
    → Kandidaten erst nach tatsächlicher Bearbeitung oder Reparatur. Dauerhaft bleiben nur die definierten Start-, Status-, Plan- und gegebenenfalls Spickzetteldateien; Blockvorbereitung, Quellenextrakte und Renderings sind temporär.
