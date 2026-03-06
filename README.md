# Agent OS – KI-Agenten-System für moderne Unternehmer

![Posts](https://img.shields.io/badge/Posts-wachsend-blue?style=flat-square)
![Agents](https://img.shields.io/badge/Agents-4-green?style=flat-square)
![Prompts](https://img.shields.io/badge/Prompts-7-orange?style=flat-square)
![Beispiele](https://img.shields.io/badge/Beispiele-2-purple?style=flat-square)
![Lizenz](https://img.shields.io/badge/Lizenz-MIT-lightgrey?style=flat-square)

Ein open-source Framework, um mit KI-Agenten Unternehmen zu gründen, zu führen und zu skalieren. Agent OS bündelt kuratierte Prompts, spezialisierte Agenten-Definitionen und erprobte Workflows – damit ein einzelner Gründer die operative Schlagkraft eines ganzen Teams erreichen kann.

---

## Was ist Agent OS?

Moderne KI-Modelle sind leistungsfähig genug, um strategische und operative Unternehmensaufgaben zu übernehmen – wenn man sie richtig anleitet. Agent OS ist das fehlende Verbindungsstück: ein strukturiertes, wachsendes System aus Prompts, Agenten-Rollen und Workflows, das genau das ermöglicht.

Statt jedes Mal von vorne zu beginnen, kannst du auf erprobte Bausteine zurückgreifen:

- **Prompts** – sofort einsetzbare Vorlagen für typische Business-Aufgaben
- **Agenten** – spezialisierte KI-Rollen mit klaren Verantwortlichkeiten (CEO, Research, Operations, Marketing)
- **Workflows** – Schritt-für-Schritt-Anleitungen, wie mehrere Agenten zusammenspielen
- **Beispiele** – echte Outputs die zeigen, was möglich ist

Agent OS ist kein Tool das man installiert. Es ist ein System das man versteht, anpasst und anwendet.

---

## Struktur

```
agent-os/
├── posts/          # Begleitmaterial zu Blog-Posts (Prompts, Beispiele)
├── agents/         # Spezialisierte KI-Agenten-Definitionen
│   ├── ceo-agent/
│   ├── research-agent/
│   ├── operations-agent/
│   └── marketing-agent/
├── prompts/        # Wiederverwendbare Prompt-Bibliothek
│   ├── business/
│   ├── operations/
│   └── content/
├── examples/       # Echte Prompt + Output Beispiele
└── workflows/      # Multi-Agenten-Workflows für komplexe Aufgaben
```

---

## Schnellstart

**Option 1: Einzelnen Prompt nutzen**

1. Gehe zu [`prompts/`](./prompts/) und wähle eine Kategorie
2. Öffne den gewünschten Prompt (z.B. [`prompts/business/market-analysis.md`](./prompts/business/market-analysis.md))
3. Kopiere den Prompt, ersetze die `[PLATZHALTER]` mit deinen Daten
4. Füge ihn in Claude, ChatGPT oder ein anderes LLM ein

**Option 2: Agenten einrichten**

1. Gehe zu [`agents/`](./agents/) und wähle einen Agenten
2. Öffne `system-prompt.md` des Agenten
3. Passe die Variablen (`[UNTERNEHMENSNAME]`, `[BRANCHE]`, etc.) an
4. Richte den Agenten in deinem bevorzugten Tool ein (Claude Projects, ChatGPT Custom GPT, etc.)
5. Schau dir [`use-cases.md`](./agents/ceo-agent/use-cases.md) an für konkrete Beispiele

**Option 3: Workflow durchlaufen**

1. Gehe zu [`workflows/`](./workflows/)
2. Wähle einen passenden Workflow (z.B. [`new-business-launch.md`](./workflows/new-business-launch.md))
3. Folge den Phasen – jede Phase sagt dir welchen Agenten du nutzt und was du eingibst

---

## Roadmap

Was als nächstes kommt:

- **Multi-Agent-Koordination** – CEO-Agent delegiert automatisch an Spezialisten
- **MCP-Integration** – Agenten mit echten Tools verbinden (Web-Suche, Kalender, CRM)
- **Branchen-Templates** – Spezialisierte Agent-Sets für SaaS, E-Commerce, Dienstleistung
- **Agent-Evaluierung** – Framework um Agenten-Outputs zu bewerten und zu verbessern
- **Community Agents** – Agenten die die Community beisteuert (Finanzen, Recht, HR)
- **Orchestrierungs-Layer** – Technisches Framework für autonome Agent-Teams

---

## Posts & Ressourcen

Jeder Ordner unter [`posts/`](./posts/) begleitet einen veröffentlichten Blog-Post. Er enthält die Prompts und Beispiele aus dem Post – direkt nutzbar, ohne den Post nochmal zu lesen.

Neue Posts werden regelmäßig hinzugefügt. Um benachrichtigt zu werden: **Star das Repo**.

---

## Beitragen

Eigene Prompts, Agenten oder Beispiele beisteuern? Sehr willkommen. Lies [`CONTRIBUTING.md`](./CONTRIBUTING.md) für Richtlinien.

---

## Lizenz

MIT – nutze alles frei, auch kommerziell. Attribution freut uns.
