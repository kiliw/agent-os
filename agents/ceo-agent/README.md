# CEO-Agent

Der strategische Denkpartner für Gründer und Unternehmer. Er hilft bei Entscheidungen, Priorisierungen und der Übersetzung von Zielen in konkrete Pläne – immer mit dem Gesamtbild im Blick.

## Wofür ist er da?

Der CEO-Agent ist kein ausführender Agent – er denkt und priorisiert. Er hilft dir dabei, die richtigen Fragen zu stellen, Entscheidungen strukturiert durchzudenken und den Fokus auf das Wesentliche zu behalten. Er delegiert (konzeptuell) an die anderen Agenten und synthetisiert ihre Outputs zu Entscheidungen.

**Typische Aufgaben:**
- Strategische Entscheidungen durchdenken (Pivot, Markteintritt, Partnerschaften)
- OKRs und Quartals-Ziele setzen und reviewen
- Prioritäten aus einem langen Backlog destillieren
- Fortschritt bewerten und nächste Schritte definieren

## Dateien

| Datei | Inhalt |
|-------|--------|
| [`system-prompt.md`](./system-prompt.md) | Der vollständige System-Prompt zum Einrichten |
| [`use-cases.md`](./use-cases.md) | Konkrete Anwendungsfälle mit Beispiel-Inputs |

## Wie einrichten

1. Öffne [`system-prompt.md`](./system-prompt.md)
2. Ersetze `[UNTERNEHMENSNAME]`, `[BRANCHE]` und `[AKTUELLE ZIELE]` mit deinen Daten
3. Richte einen neuen "Project" in Claude (oder Custom GPT in ChatGPT) ein
4. Füge den angepassten System-Prompt ein
5. Starte mit einem der Use Cases aus [`use-cases.md`](./use-cases.md)

## Zusammenspiel mit anderen Agenten

Der CEO-Agent ist der Ausgangspunkt für komplexe Aufgaben. Er definiert was gebraucht wird, die Spezialisten liefern es.

```
CEO-Agent gibt vor → Research-Agent analysiert
                   → Operations-Agent strukturiert
                   → Marketing-Agent kommuniziert
CEO-Agent synthetisiert ← alle drei
```
