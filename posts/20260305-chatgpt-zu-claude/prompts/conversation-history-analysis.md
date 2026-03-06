# Prompt: ChatGPT-Gesprächshistorie analysieren & Wissensdatenbank aufbauen

## Metadaten

| Feld | Wert |
|------|------|
| **Zweck** | Komplette ChatGPT-Gesprächshistorie in eine strukturierte Wissensdatenbank für Claude umwandeln |
| **Modell** | Claude Opus 4 (empfohlen – wegen langer Kontext-Länge und Analyse-Tiefe) |
| **Input** | `chat.html` aus dem ChatGPT-Datenexport |
| **Output** | Kognitives Blueprint: Wer du bist, wie du denkst, woran du arbeitest |

---

## Der Prompt

```
ROLE

You are an expert at analyzing conversation history and extracting durable,
high-signal knowledge from it. Your job is to read through my complete ChatGPT
conversation history (in the chat.html file) and reconstruct it into a structured
knowledge base that captures who I am, how I think, what I'm working on, and how
I prefer to work -- so that Claude can hit the ground running in future
conversations without me re-explaining my context from scratch.

You are not summarizing. You are building a cognitive blueprint.

TASK

Analyze the full conversation history and produce a structured knowledge base
organized into the following sections:

1. Identity Profile
   - Core personality traits
   - Cognitive style and how I approach problems
   - Communication preferences
   - What motivates and drives me
   - Core values
   - Key strengths
   - Friction points and frustrations

2. Long-Term Vision & Goals
   - Goals I've stated explicitly
   - Goals implied by patterns in my behavior
   - Recurring ambitions
   - How my strategic direction has shifted over time

3. Active & Recurring Projects
   For each project, capture:
   - Name (or best inference)
   - Purpose and context
   - Current state
   - Open loops and unresolved decisions
   - Key decisions already made
   - Constraints and dependencies

4. Knowledge Domains & Expertise
   - Areas where I have deep competence
   - Areas where I'm actively learning
   - Tools and platforms I use regularly
   - Technical stack (if applicable)
   - Conceptual frameworks I gravitate toward

5. Decision-Making Patterns
   - Risk tolerance
   - Speed vs. precision tradeoffs
   - Iterative vs. perfectionist tendencies
   - Strategic vs. tactical bias
   - Whether I tend to compound efforts or restart frequently

6. Behavioral Patterns
   - Recurring themes or questions across conversations
   - Shifts in interest or focus over time
   - Signs of scaling ambition, burnout, curiosity spikes, or pivots

7. Constraints & Operating Conditions
   - Time constraints
   - Resource or budget limitations
   - Skill gaps I've acknowledged
   - Structural or environmental limits on what I can do

8. Preferred Output Style
   - Formatting preferences
   - Tone (casual vs. formal, concise vs. thorough)
   - Level of detail I typically want
   - How I like responses structured

9. Open Loops & Unfinished Threads
   - Ideas mentioned but never developed
   - Projects started and paused
   - Strategic questions I haven't resolved

10. Claude Persistent Memory Core
    Create a final compressed section titled "Claude Persistent Memory Core"
    that distills everything above into a dense, high-signal reference.
    This section should:
    - Be highly compressed — every sentence should carry weight
    - Capture only durable traits, active priorities, and recurring patterns
    - Contain zero filler or repetition
    - Be written as if it's the first thing Claude reads before any
      conversation with me

RULES

- Do not summarize chronologically — extract patterns, not timelines
- Do not restate full conversations
- Distill repetition into behavioral signals
- Infer implicit traits when the evidence is strong; label them as [inferred]
- Preserve nuance that affects long-term strategy or behavior
- Omit anything that's one-off, low-signal, or clearly outdated

OUTPUT FORMAT

Clean markdown with headings and bullet points. No JSON. No meta-commentary
about your process. No preamble. Just the knowledge base.
```

---

## Nutzungshinweise

**Schritt für Schritt:**

1. **ChatGPT-Export anfordern:** Einstellungen → Datenschutz → Daten exportieren → E-Mail abwarten → `chat.html` herunterladen
2. **Datei hochladen:** In Claude eine neue Konversation starten, `chat.html` als Datei anhängen
3. **Prompt einfügen:** Den Prompt oben kopieren und absenden
4. **Output sichern:** Das Ergebnis in ein Claude Project als Projektkontext einfügen – dann steht es in jeder neuen Konversation automatisch zur Verfügung

**Warum Claude Opus?**
Die `chat.html` kann sehr groß werden (mehrere MB). Claude Opus verarbeitet bis zu 200.000 Token Kontext und liefert bei komplexer Analyse-Aufgaben die tiefsten Ergebnisse.

**Was du zurückbekommst:**
Keine Zusammenfassung – ein kognitives Blueprint. Claude weiß danach wie du denkst, was dich antreibt, woran du arbeitest und wie du kommunizieren willst. Du musst deinen Kontext nie mehr von vorne erklären.
