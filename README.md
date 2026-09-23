# claude-dev-skills

Eigene [Claude Code](https://claude.com/claude-code) Skills, die als Slash-Commands beim Programmieren helfen — mit dem Ziel, nicht nur fertigen Code zu bekommen, sondern die Entscheidungen dahinter nachvollziehen oder bewusst delegieren zu können.

## Skills

### `/code-with-me`

Setzt Feature-Anforderungen gemeinsam mit dir Schritt für Schritt um. Vor jedem Implementierungsschritt wird die gewählte Vorgehensweise erklärt und begründet (welches Tool/Framework, welcher Ansatz, warum diese Reihenfolge). Startet mit einer kompakten Klärungsrunde für offene Fragen, dann folgt der eigentliche Ablauf — für Lernen und Mitentscheiden statt nur Ergebnis abholen.

### `/code-for-me`

Klärt zuerst alle offenen Fragen zu einer Anforderung in einer strukturierten Interview-Phase (angelehnt an das ["Grilling"-Muster](https://github.com/mattpocock) von Matt Pocock: Fragen als Entscheidungsbaum, in Runden, jeweils mit Empfehlung), und setzt die Anforderung danach eigenständig um — Rückfragen nur noch bei echten Planabweichungen. Für Delegieren statt Mitlernen.

### Geplant

- `/explain` — Code oder Konzepte erklären
- `/visualise` — Architektur/Abläufe visualisieren

## Installation

Skills müssen unter `~/.claude/skills/<name>/` liegen, damit Claude Code sie erkennt:

```bash
cp -r skills/code-with-me ~/.claude/skills/
cp -r skills/code-for-me ~/.claude/skills/
```

Danach in einer neuen Claude-Code-Session `/code-with-me` bzw. `/code-for-me` aufrufen.

## Format

Jeder Skill ist eine `SKILL.md` mit YAML-Frontmatter (`name`, `description`, `disable-model-invocation: true` — verhindert, dass Claude den Skill selbständig triggert, nur expliziter Aufruf aktiviert ihn) gefolgt von Markdown-Instruktionen, die das Verhalten für die restliche Session steuern.

## Lizenz

[MIT](LICENSE): frei nutzbar und anpassbar, solange der Copyright-Hinweis erhalten bleibt.
