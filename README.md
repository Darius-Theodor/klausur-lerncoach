# klausur-lerncoach

Ein Agent-Skill für Klausurvorbereitung unter Zeitdruck.

Der Assistent wird damit vom Erklärbär zum Prüfer: er stellt Aufgaben unter
Klausurbedingungen, wartet, korrigiert mit Teilpunkten, repariert genau die
getroffene Lücke — und führt den Lernstand in Dateien statt im Chatverlauf, damit
er Sitzungsabbrüche, Kontextlimits und Modellwechsel überlebt.

Gebaut für die Lage: **Ziel ist bestehen, nicht die Note; die knappe Ressource ist
Zeit; die Baseline ist oft Null.** Erprobt an einem Durchlauf mit 12 Themen in rund
zwei Tagen.

## Installieren

```sh
npx skills add Darius-Theodor/klausur-lerncoach --all
```

Installiert in alle erkannten Agents — Claude Code (`~/.claude/skills/`) und Codex
(`~/.codex/skills/`) nutzen dasselbe Format.

Danach im Chat einfach:

> Ich möchte jetzt RN lernen.

Beim ersten Mal für ein Fach legt der Skill die Artefakte an (Rahmendaten,
Themenliste, Termine, Logistik), danach steigt jeder Lernblock reibungsfrei ein.

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
| `SKILL.md` | Pfadwahl, Lernblock, Zerlegung, Nachweis und Stufen, Budget, Artefakte |
| `references/setup.md` | neues Fach anlegen — die neun Schritte vor dem ersten Lernblock |
| `references/material.md` | Materialhierarchie, Vorgehen ohne Altklausur, Transkripte |
| `references/spickzettel.md` | Aufnahmekriterien und laufende Verdichtung |
| `references/abschluss.md` | gemischte Wiederholung, Probeklausur, Endspurt |
| `references/herkunft.md` | woher die Regeln kommen — nur bei Zweifeln an einer Regel |
| `templates/` | `LERNSTART.md`, `LERNSTATUS.md`, `SPICKZETTEL.md` |

## Die Grundideen

- **Klausurbedingungen.** Nach der Aufgabenstellung endet der Beitrag des Agenten.
  Was in der Klausur nicht auf dem Blatt stünde, steht auch hier nicht.
- **Zerlegung.** Originalaufgaben werden in der *Lösungsreihenfolge* in Teilschritte
  zerlegt, die einzeln von Null aus lösbar sind. Der Nachweis ist danach eine neue
  Variante am Stück.
- **Nachweis.** Eine Stufe steigt nur wegen einer selbst gelösten Aufgabe, und der
  Nachweis hält fest, mit wie viel Hilfe sie zustande kam. Wiedererkennen einer
  Musterlösung trägt keine Stufe.
- **Budget.** Rund drei Aufgaben oder 25 Minuten pro Thema, dann Zwangsentscheidung.
  `stabil` entsteht nie im selben Block wie `übungsfähig` — der Zeitversatz ist Teil
  des Nachweises.
- **Kein Kalt-Testen.** Eine blind geschriebene Altklausur demoralisiert bei Baseline
  Null und liefert keine brauchbare Lückenliste. Die Diagnose entsteht im Lernen.

## Lizenz

MIT
