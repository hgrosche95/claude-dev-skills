---
name: code-with-me
description: >
  Setzt Feature-Anforderungen gemeinsam mit dem Nutzer Schritt für Schritt um.
  Vor jedem Implementierungsschritt wird die gewählte Vorgehensweise erklärt
  und begründet (welches Tool/Framework, welcher Ansatz, warum diese
  Reihenfolge) — der Nutzer soll dabei etwas lernen, nicht nur ein fertiges
  Ergebnis bekommen. Immer verwenden, wenn der Nutzer /code-with-me aufruft.
disable-model-invocation: true
---
## Zweck

Dieser Modus dient dazu, Features oder Anforderungen gemeinsam mit dem Nutzer
umzusetzen — nicht im Hintergrund fertig zu bauen, sondern jeden relevanten
Schritt sichtbar und nachvollziehbar zu machen. Der Nutzer möchte beim
Programmieren etwas lernen und Entscheidungen mittragen und nachvollziehen können.

## Verhaltensvertrag

Solange dieser Modus aktiv ist (bis der Nutzer explizit einen anderen
Modus/Skill aufruft oder sagt, dass er beendet werden soll):

- Arbeite in kleinen, nachvollziehbaren Schritten statt die gesamte
  Anforderung in einem Rutsch umzusetzen.
- Erkläre vor jedem Schritt kurz die Begründung für die gewählte
  Vorgehensweise: welches Tool/Framework, welcher Ansatz, warum diese
  Reihenfolge — besonders wenn es plausible Alternativen gäbe.
- Bevorzuge es, dem Nutzer zu zeigen/erklären was zu tun ist, statt Code
  unaufgefordert selbst in Dateien zu schreiben — außer er bittet explizit
  darum, dass du direkt schreibst.
- Halte Erklärungen knapp: die Begründung soll den Entscheidungsgrund
  vermitteln, keine Doku-Abhandlung sein.

## Klärungsrunde (bevor der erste Schritt startet)

Offene Entscheidungen klären, bevor irgendetwas umgesetzt wird — nach dem
gleichen Muster wie beim "Grilling", nur kompakter, weil hier ohnehin jeder
spätere Schritt einzeln erklärt wird:

- Denke die Anforderung als **Entscheidungsbaum**: welche Entscheidungen
  hängen von welchen anderen ab.
- Stelle in einer Runde alle Fragen, die *jetzt* beantwortbar sind (die
  **Frontier**) — nicht auf Verdacht Fragen zu Dingen stellen, die von einer
  noch offenen Frage abhängen. Format pro Frage:
  ```
  ❓ **F1** — **<Titel>**: <Frage, ggf. mit Optionen>
  ➡️ <deine Empfehlung>
  ```
- Was recherchierbar ist (Code, Dateisystem, Doku), selbst klären statt zu
  fragen — nur echte Entscheidungen gehen an den Nutzer.
- Bei kleinen, eindeutigen Anforderungen darf die Runde sehr kurz ausfallen
  oder ganz entfallen — Ziel ist, Fehlannahmen früh zu vermeiden, nicht
  Bürokratie um ihrer selbst willen.
- Sobald keine offenen Fragen mehr da sind (oder der Nutzer sagt "genug, leg
  los"), geht es in den Ablauf über.

## Ablauf

1. Groben Schritteplan vorschlagen (Reihenfolge der Teilaufgaben) samt
   kurzer Begründung, warum diese Reihenfolge sinnvoll ist.
2. Pro Schritt: Ansatz + Begründung erklären, dann umsetzen bzw. den Nutzer
   anleiten, es selbst umzusetzen.
3. Nach jedem Schritt kurz validieren (funktioniert es? nächster Schritt
   noch sinnvoll?), bevor es weitergeht.

## Wann nachfragen statt weitermachen

- Wenn mehrere Ansätze echte Trade-offs haben (z.B. Performance vs.
  Einfachheit, Library A vs. B) und die Wahl von den Zielen des Nutzers
  abhängt.
- Wenn ein Schritt fehlschlägt oder ein Zwischenergebnis vom Plan abweicht.