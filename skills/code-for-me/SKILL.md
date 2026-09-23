---
name: code-for-me
description: >
  Setzt eine Anforderung eigenständig um, nachdem zuerst alle offenen Fragen
  geklärt wurden. Startet mit einer Interview-Phase (Fragen zu unklaren
  Entscheidungen, in Runden, mit Empfehlung), erst danach folgt eigenständige
  Umsetzung bis zur Fertigstellung oder bis eine Abweichung vom Plan eine
  Rückfrage nötig macht.
disable-model-invocation: true
---

## Zweck

Dieser Modus klärt zunächst alle offenen Fragen zu einer Anforderung, bevor
irgendetwas umgesetzt wird — danach läuft die Umsetzung eigenständig durch,
bis sie fertig ist oder eine Abweichung vom vereinbarten Plan eine Rückfrage
nötig macht. Anders als /code-with-me werden Zwischenschritte hier nicht
einzeln erklärt — der Nutzer will hier delegieren, nicht mitlernen.

## Phase 1: Klärungsrunde

Angelehnt an das "Grilling"-Muster: Anforderungen als Baum aus Fragen
behandeln, nicht als einzelne Liste.

- Baue gedanklich einen **Entscheidungsbaum**: jede offene Entscheidung kann
  Folgeentscheidungen nach sich ziehen.
- Arbeite in **Runden**. Die **Frontier** sind alle Fragen, deren
  Voraussetzungen schon geklärt sind — stelle die ganze Frontier auf einmal,
  nummeriert, mit Empfehlung:
  ```
  ❓ **F1** — **<Titel>**: <Frage, ggf. mit Optionen>
  ➡️ <deine Empfehlung>
  ```
- Nach jeder Antwortrunde: Frontier neu berechnen, nächste Runde stellen.
- **Fakten sind deine Aufgabe, nie die des Nutzers**: Was im Code/Dateisystem
  nachschaubar ist, selbst recherchieren. Nur echte Entscheidungen (die von
  den Zielen des Nutzers abhängen) gehen an ihn.
- Phase 1 endet erst, wenn die Frontier leer ist. Fasse zum Schluss kurz
  zusammen, was vereinbart wurde, und warte auf Bestätigung.

## Phase 2: Eigenständige Umsetzung

- Nach Bestätigung: Anforderung eigenständig umsetzen, ohne bei jedem
  Schritt nachzufragen.
- Bevor das Ergebnis als fertig gemeldet wird: tatsächlich verifizieren
  statt nur zu vermuten — vorhandene Tests/Build/Linter ausführen, oder wenn
  keine vorhanden sind, das Feature direkt ausführen. Schlägt das fehl,
  selbst beheben statt es nur in der Abschluss-Zusammenfassung zu erwähnen
  (das zählt nicht als Planabweichung, die eine Rückfrage braucht — außer
  der Fix selbst erfordert wieder eine Entscheidung mit echten Trade-offs).
- Unterbrich nur, wenn:
  - eine Entscheidung mit echten Trade-offs ansteht, die Phase 1 nicht
    abgedeckt hat,
  - die Umsetzung vom vereinbarten Plan abweichen muss (z.B. weil sich eine
    Annahme als falsch herausstellt),
  - ein Schritt fehlschlägt und der Fix selbst eine Entscheidung erfordert.
- Am Ende: kurze Zusammenfassung, was umgesetzt wurde und ob/wo vom Plan
  abgewichen wurde.
