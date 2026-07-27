# Material

## Quellen haben verschiedene Rollen

Keine einzelne Rangliste entscheidet alles:

1. **Aufgabenquelle:** Altklausur und offizielle Probeaufgaben bestimmen Aufgabenstil, Umfang und Punkte. Fehlen sie, wird die erste Lernaufgabe quellenbasiert aus Übungen, Transkripten und offiziellen Themen abgeleitet; eine davon verschiedene generierte Variante kommt erst als Nachweis.
2. **Wissensquelle:** Vorlesungsfolien, Skript und Übungen liefern die Begriffe und Verfahren, die vor dem jeweiligen Teilschritt von null erklärt werden.
3. **Lösungs- und Bewertungsquelle:** Musterlösung, Klausurbesprechung und Transkript zeigen den erwarteten Rechenweg, akzeptierte Formulierungen und Folgefehler.
4. **Themenquelle:** Offizielle Themenliste und ausdrückliche Aussagen der Lehrperson bestimmen, was gelernt oder ausgeschlossen wird.

Wenn Fachwissen im Status nicht bereits nachgewiesen ist, liegt bei Baseline Null eine konkrete Wissenslücke vor. Warte nicht auf eine falsche Antwort, um Folien oder Skript zu öffnen.

## Vorbereitung eines Lernblocks

Vor der ersten Frage:

1. Wähle eine Originalaufgabe oder baue nach dem Abschnitt „Wenn es keine Altklausur gibt“ eine quellenbasierte Ersatzaufgabe.
2. Klär mit Lösung oder Besprechung die erwarteten Lösungsschritte und Punkte. Bei einer Ersatzaufgabe legst du beides vor der ersten Frage selbst quellenbasiert fest und markierst die Punkte als Schätzung.
3. Zerleg den Weg in Wissensvoraussetzungen und Lösungsschritte.
4. Öffne für den ersten Schritt die genaue Stelle in Vorlesung, Skript oder Übung.
5. Zeig die vollständige Lernaufgabe als sichtbaren Kontext. Bei bild- oder layoutabhängigen Aufgaben renderst und zeigst du den relevanten Originalausschnitt. Kennzeichne eine Ersatzaufgabe und nenne knapp ihre Quellenbasis.
6. Erklär nur dieses Wissen und stell danach eine damit lösbare Teilfrage.

Vor jedem späteren Teilschritt wiederholst du Schritt 4, sobald neues Fachwissen nötig wird. Nutze vorhandenes Kursmaterial statt Modellgedächtnis. Lies trotzdem keine vollständige Vorlesung auf Vorrat.

Vorlesungsvideos nicht vollständig nachholen. Bei Bedarf transkribieren und den Text gezielt durchsuchen.

## Gewichtung bei Widerspruch

Offizielle Themenliste für *diese* Klausur → ausdrückliche Aussagen aus der Abschlussbesprechung → Altklausur → eigene ältere Lernnotizen.

Eine Altklausur belegt **Aufgabenstil**, nicht die Punkteverteilung des aktuellen Termins. Bonuspunkte aus Praktikum oder Übung nie als sicher einrechnen.

## Wenn es keine Altklausur gibt

Der Normalfall, nicht die Ausnahme. Der wichtigste Aufgabenpool fehlt und muss ersetzt werden, in dieser Reihenfolge:

1. **Praktikums- und Übungsaufgaben** sind der beste Ersatz — selber Lehrstuhl, selber Stil. Teile, die nur am Rechner funktionieren (Tool-Bedienung, Screenshots), aussortieren, wenn die Klausur auf Papier geschrieben wird.
2. **Aussagen aus den Transkripten als Aufgabenquelle.** Sätze wie „das frage ich manchmal in der Klausur" oder „das üben wir in Tabellenform, das ist näher an der Klausur" sind faktisch Aufgabenstellungen — direkt in eine Statuszeile übersetzen.
3. **Generierte Aufgaben pro Kernthema**, aber erst an dritter Stelle und immer im Stil der beiden Quellen oben. Ohne diesen Anker driften generierte Aufgaben ins Lehrbuchhafte ab und prüfen Dinge, die nie drankommen.
4. **Die Probeklausur selbst bauen** — aus Praktikums- und generierten Aufgaben eine Mischklausur in der echten Länge. Ohne Altklausur ist das mehr Arbeit, und genau deshalb wichtiger: sonst existiert überhaupt kein Messpunkt.

Ohne Altklausur sind die Transkripte nicht Ergänzung, sondern Hauptquelle für alles, was über den reinen Stoff hinausgeht.

Für jeden Themenbaustein entsteht zuerst **eine** Ersatz-Lernaufgabe als angeleitetes Gerüst und zusätzlich **eine andere** Kontrollvariante für den späteren Nachweis am Stück. Die Kontrollvariante muss nicht im selben Block folgen, aber vor der Stufe `übungsfähig`. Gib die Ersatzaufgabe nicht als Original aus. Wenn Umfang, Punkte oder Klausurstil nicht belegt sind, kennzeichne sie als geschätzt, statt Scheingenauigkeit zu erzeugen.

## Videos verwertbar machen

Lokal transkribieren statt anschauen. Auf Apple Silicon läuft `mlx_whisper` mit `large-v3-turbo` bei etwa 45-facher Echtzeit — eine 90-Minuten-Vorlesung dauert rund zwei Minuten. Der Text ist danach durchsuchbar und als Beleg zitierbar.

```bash
mlx_whisper --model mlx-community/whisper-large-v3-turbo \
  --language de --output-format txt vorlesung.mov
```

Fallstrick bei Opencast und ähnlichen Vorlesungsportalen: die Spur mit gesunder Audio-Bitrate (> 10 kbit/s) wählen. Die „Folien"-Spuren haben tote Audiokanäle und ergeben leere Transkripte.
