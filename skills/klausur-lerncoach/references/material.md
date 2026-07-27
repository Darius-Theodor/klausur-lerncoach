# Material

## Hierarchie

1. **Originalaufgaben zuerst** — Altklausur, offizielle Probeaufgaben. Generierte Varianten erst, wenn die durch sind.
2. **Vorlesungstranskript als Musterlösung und Bewertungshinweis** — die Abschlussbesprechung sagt oft ausdrücklich, worauf Punkte gegeben werden.
3. **Folien und Skript nur bei einer konkreten Wissenslücke öffnen.** Nie „zum Überblick durchgehen".
4. **Vorlesungsvideos nicht nachholen.** Bei Bedarf transkribieren und den Text durchsuchen (unten).

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

## Videos verwertbar machen

Lokal transkribieren statt anschauen. Auf Apple Silicon läuft `mlx_whisper` mit `large-v3-turbo` bei etwa 45-facher Echtzeit — eine 90-Minuten-Vorlesung dauert rund zwei Minuten. Der Text ist danach durchsuchbar und als Beleg zitierbar.

```bash
mlx_whisper --model mlx-community/whisper-large-v3-turbo \
  --language de --output-format txt vorlesung.mov
```

Fallstrick bei Opencast und ähnlichen Vorlesungsportalen: die Spur mit gesunder Audio-Bitrate (> 10 kbit/s) wählen. Die „Folien"-Spuren haben tote Audiokanäle und ergeben leere Transkripte.
