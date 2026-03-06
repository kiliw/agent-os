# Agenten

Spezialisierte KI-Rollen für typische Unternehmens-Funktionen. Jeder Agent hat eine klare Identität, Denkweise und Ausgabeformat – konfiguriert für seinen spezifischen Bereich.

## Was ist ein "Agent" in diesem System?

Ein Agent ist kein separates Tool oder Programm. Es ist ein **System-Prompt** der einem KI-Modell eine klare Rolle, Denkweise und Arbeitsweise gibt. Du richtest ihn einmal ein – in Claude Projects, einem ChatGPT Custom GPT, oder einem anderen Tool deiner Wahl – und arbeitest dann konsistent mit ihm.

Der Unterschied zu einem generischen KI-Assistenten: Der Agent weiß wer er ist, was er kann, wie er denkt und wie er antwortet. Du musst das nicht jedes Mal neu erklären.

## Die vier Kern-Agenten

```
CEO-Agent
├── Strategische Entscheidungen, Priorisierung, OKR-Review
├── Denkt in Quartalen und Jahren
└── Delegiert an: Research, Operations, Marketing

Research-Agent
├── Marktanalyse, Wettbewerb, Trends, Kundensegmente
├── Denkt in Daten, Quellen, MECE-Strukturen
└── Liefert an: CEO-Agent, Marketing-Agent

Operations-Agent
├── Prozesse, SOPs, Workflows, Effizienz
├── Denkt in Systemen, Checklisten, Verantwortlichkeiten
└── Liefert an: CEO-Agent, alle Funktionen

Marketing-Agent
├── Positionierung, Content, Kampagnen, Messaging
├── Denkt in Jobs-to-be-done, Kanälen, Conversion
└── Nutzt: Research-Agent-Outputs, CEO-Strategie
```

## Wie die Agenten zusammenspielen

In der Praxis läuft ein komplexes Projekt oft so ab:

1. **CEO-Agent** bekommt das Ziel: "Wir wollen in einen neuen Markt expandieren"
2. **Research-Agent** analysiert den Markt: Größe, Wettbewerb, ungedeckte Bedürfnisse
3. **CEO-Agent** trifft Entscheidungen auf Basis der Research-Findings
4. **Marketing-Agent** entwickelt Positionierung und Go-to-market für den neuen Markt
5. **Operations-Agent** baut die nötigen Prozesse und Strukturen auf

Du steuerst diese Übergaben manuell, indem du den Output eines Agenten als Input für den nächsten nutzt. [Workflows](../workflows/) beschreiben diese Abläufe Schritt für Schritt.

## Einen Agenten anpassen

Jeder Agent hat Variablen die du für dein Unternehmen befüllen solltest. Suche im System-Prompt nach `[PLATZHALTER IN ECKIGEN KLAMMERN]` und ersetze sie:

- `[UNTERNEHMENSNAME]` → Der Name deines Unternehmens
- `[BRANCHE]` → Deine Branche (z.B. "B2B SaaS", "E-Commerce", "Beratung")
- `[AKTUELLE ZIELE]` → Deine Q-Ziele oder OKRs

Speichere deine angepasste Version lokal unter `private/agents/` – dieser Ordner ist in `.gitignore` und kommt nie ins öffentliche Repo.

## Neuen Agenten erstellen

Nutze [`AGENT_TEMPLATE.md`](./AGENT_TEMPLATE.md) als Ausgangspunkt. Die Vorlage führt dich durch alle relevanten Abschnitte.

## Verfügbare Agenten

| Agent | Beschreibung | System-Prompt |
|-------|-------------|--------------|
| [CEO-Agent](./ceo-agent/) | Strategie, Priorisierung, Entscheidungsunterstützung | [system-prompt.md](./ceo-agent/system-prompt.md) |
| [Research-Agent](./research-agent/) | Marktanalyse, Wettbewerb, Trends | [system-prompt.md](./research-agent/system-prompt.md) |
| [Operations-Agent](./operations-agent/) | Prozesse, SOPs, Workflows | [system-prompt.md](./operations-agent/system-prompt.md) |
| [Marketing-Agent](./marketing-agent/) | Positionierung, Content, Kampagnen | [system-prompt.md](./marketing-agent/system-prompt.md) |
