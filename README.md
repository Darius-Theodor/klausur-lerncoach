# klausur-lerncoach

Ein Agent-Skill für Klausurvorbereitung unter Zeitdruck.

Der Assistent baut das für den nächsten Schritt nötige Fachwissen aus den
Kursquellen von null auf, zerlegt klausurnahe Lernaufgaben in lösbare Schritte,
wartet nach jeder Frage und repariert genau die getroffene Lücke. Erst eine neue
Kontrollvariante läuft am Stück unter Klausurbedingungen. Der Lernstand liegt in
Dateien statt im Chatverlauf und überlebt dadurch Sitzungsabbrüche, Kontextlimits
und Modellwechsel.

Gebaut für die Lage: **Ziel ist bestehen, nicht die Note; die knappe Ressource ist
Zeit; die fachliche Baseline ist Null.** Erprobt an einem vollständigen
Visual-Computing-Durchlauf und isoliert gegen technische sowie qualitative Fächer
mit und ohne Altklausur getestet.

## Installieren

```sh
npx skills add Darius-Theodor/klausur-lerncoach --all
```

Installiert in alle erkannten Agents — Claude Code (`~/.claude/skills/`) und Codex
(`~/.codex/skills/`) nutzen dasselbe Format.

Danach den Skill ausdrücklich aufrufen, zum Beispiel:

> Nutze den Klausur-Lerncoach für RN.

Beim ersten Mal für ein Fach legt der Skill die Artefakte an (Rahmendaten,
Kompetenzabdeckung, Aufgabenlücken, Meilensteine, Logistik), danach steigt jeder
Lernblock reibungsfrei ein.

## Ohne Agent-Skills

Läuft auch in ChatGPT oder jedem anderen Assistenten: `skills/klausur-lerncoach/SKILL.md`
als Datei anhängen. Die Datei ist so geschrieben, dass sie standalone trägt — die
Dateien unter `references/` hängst du bei Bedarf einzeln dazu (`setup.md` einmal am
Anfang, `abschluss.md` in den letzten Tagen).

Nicht verfügbar auf claude.ai im Browser und in Cowork-Sessions — die laden Skills
aus dem Account, nicht aus `~/.claude`. Dort entweder als .zip unter
Settings → Features hochladen oder die Datei anhängen.

## Was drin ist

| Datei | Inhalt |
|---|---|
| `SKILL.md` | Pfadwahl, Lernblock, Zerlegung, Nachweis und Stufen, adaptive Steuerung, Artefakte |
| `references/setup.md` | neues Fach anlegen — die neun Schritte vor dem ersten Lernblock |
| `references/material.md` | Materialhierarchie, Vorgehen ohne Altklausur, Transkripte |
| `references/spickzettel.md` | Aufnahmekriterien und laufende Verdichtung |
| `references/abschluss.md` | gemischte Wiederholung, Probeklausur, Endspurt |
| `references/herkunft.md` | woher die Regeln kommen — nur bei Zweifeln an einer Regel |
| `templates/` | `LERNSTART.md`, `LERNSTATUS.md`, `SPICKZETTEL.md` |

## Die Grundideen

- **Wissen vor Prüfung.** Vor jedem neuen Teilschritt erklärt der Agent aus den
  Kursquellen genau das Wissen, das dafür fehlt. Die Lernaufgabe ist kein Kalt-Test.
- **Zerlegung.** Original- und quellenbasierte Ersatzaufgaben werden in der
  *Bearbeitungsreihenfolge* in Teilschritte zerlegt, die einzeln von null aus
  lösbar sind. Der Nachweis ist danach eine neue Variante am Stück.
- **Nachweis.** Eine Stufe steigt nur wegen einer selbst gelösten Aufgabe, und der
  Nachweis hält fest, mit wie viel Hilfe sie zustande kam. Wiedererkennen einer
  Musterlösung trägt keine Stufe.
- **Adaptive Steuerung.** Keine feste Minuten- oder Aufgabenquote. Bei jedem
  tatsächlichen Lernstart und an natürlichen Aufgabenschnitten gewinnt die Aufgabe
  mit dem besten Verhältnis aus Prüfungsnutzen und Lernaufwand.
- **Mit oder ohne Altklausur.** Fehlende Aufgabentypen werden aus Lernzielen,
  Übungen, Folien und Transkripten abgeleitet, transparent gekennzeichnet und mit
  einer anderen Kontrollvariante nachgewiesen.
- **Kein Kalt-Testen.** Eine blind geschriebene Altklausur demoralisiert bei Baseline
  Null und liefert keine brauchbare Lückenliste. Die Diagnose entsteht im Lernen.

## Lizenz

MIT
