# Research-Agent

Der tiefe Analytiker. Er verwandelt vage Fragen in strukturierte Erkenntnisse – durch systematische Analyse von Märkten, Wettbewerbern, Kundensegmenten und Trends.

## Wofür ist er da?

Immer wenn du Entscheidungen auf Basis von Marktdaten, Wettbewerbsinfos oder Kundenwissen treffen musst – und nicht tagelang recherchieren willst. Der Research-Agent strukturiert die Analyse, hilft dir die richtigen Fragen zu stellen, und produziert verwertbare Outputs die direkt in Entscheidungen einfließen können.

**Typische Aufgaben:**
- Marktgrößen schätzen und Segmente identifizieren
- Wettbewerbslandschaft kartieren
- Kundengruppen profilieren
- Trends und Signale einordnen
- Sekundärquellen-Analyse strukturieren

## Dateien

| Datei | Inhalt |
|-------|--------|
| [`system-prompt.md`](./system-prompt.md) | Der vollständige System-Prompt zum Einrichten |
| [`use-cases.md`](./use-cases.md) | Konkrete Anwendungsfälle mit Beispiel-Inputs |

## Wie einrichten

1. Öffne [`system-prompt.md`](./system-prompt.md)
2. Ersetze die Variablen für deine Branche und deinen Markt
3. Richte einen separaten "Project" oder Chat-Kontext ein (getrennt vom CEO-Agenten)
4. Optional: Füge relevante Marktdaten oder Kundeninterviews als Kontext-Dokument hinzu

## Wichtiger Hinweis

Der Research-Agent kann keine echte Web-Suche durchführen (außer wenn du ihn mit einem Tool wie Perplexity oder Web-Browsing verbindest). Ohne solche Tools analysiert er auf Basis seines Trainingswissens und deiner Inputs – das ist oft ausreichend für eine erste Strukturierung, aber sollte mit echten Quellen verifiziert werden.
