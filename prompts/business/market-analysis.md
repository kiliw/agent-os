# Marktanalyse-Prompt

## Metadaten

| Feld | Wert |
|------|------|
| **Zweck** | Strukturierte Marktanalyse für eine Branche oder Nische |
| **Empfohlenes Modell** | Claude Sonnet 4.5+, GPT-4o, oder Gemini 1.5 Pro |
| **Outputlänge** | 800–1500 Wörter |
| **Vorbereitung** | Branche/Nische kennen, geografischen Fokus definieren |

---

## Der Prompt

```
Du bist ein erfahrener Marktanalyst mit Fokus auf [BRANCHE/NISCHE].

Erstelle eine strukturierte Marktanalyse für:
- Markt/Branche: [MARKT/BRANCHE, z.B. "Heimbrauen-Hobbymarkt in Deutschland"]
- Geografischer Fokus: [GEOGRAFISCHER FOKUS, z.B. "Deutschland", "DACH", "Europa"]
- Zeitraum: [ZEITRAUM, z.B. "2024–2026", "aktuelle Situation"]
- Kontext: Ich bin [DEINE ROLLE, z.B. "Gründer eines Online-Shops für Heimbrauen-Ausrüstung"] und brauche diese Analyse für [ZWECK, z.B. "Entscheidung ob ich in den Markt eintreten soll"].

Strukturiere deine Analyse so:

## 1. Marktüberblick
- Marktgröße heute (TAM – Total Addressable Market): Schätze in Euro und Käufer-Anzahl
- Marktgröße meines erreichbaren Segments (SAM – Serviceable Addressable Market)
- Realistische Marktgröße für ein neues Unternehmen (SOM – Serviceable Obtainable Market)
- Wachstumsrate: Wächst der Markt? Wie schnell?
- Marktreife: Emerging / Wachstum / Reife / Rückgang

## 2. Markttreiber und -hemmer
- 3-4 Haupttreiber: Was lässt den Markt wachsen?
- 2-3 Hemmer: Was bremst das Wachstum?
- Externe Faktoren: Regulierung, Makrotrends, Technologie

## 3. Kundensegmente
- Identifiziere 3-4 Hauptsegmente mit:
  - Demographischem Profil
  - Kaufmotivation
  - Geschätzter Größe
  - Zahlungsbereitschaft (niedrig/mittel/hoch)

## 4. Wettbewerbslandschaft
- Marktstruktur: Fragmentiert oder konzentriert? Gibt es einen Marktführer?
- Haupttypen von Wettbewerbern (nicht Einzelne – Kategorien)
- Wesentliche Differenzierungsdimensionen im Markt (Preis? Service? Spezialisierung?)

## 5. Chancen und Risiken
- 3 größte Chancen für einen Neueinsteiger
- 3 größte Risiken
- Nicht-offensichtliche Erkenntnis: Was übersehen die meisten?

## 6. Fazit
- 3 Sätze: Ist dieser Markt attraktiv? Für wen? Unter welchen Bedingungen?

Kennzeichne Schätzungen mit "(Schätzung)" und benenne Quelltypen die du empfiehlst um diese zu verifizieren.
```

---

## Platzhalter-Erklärung

| Platzhalter | Beschreibung | Beispiel |
|-------------|-------------|---------|
| `[BRANCHE/NISCHE]` | Dein Markt | "Heimbrauen", "B2B SaaS HR-Tools", "Nachhaltige Kinderkleidung" |
| `[MARKT/BRANCHE]` | Vollständige Beschreibung | "Online-Markt für Premium-Heimbrauen-Ausrüstung in Deutschland" |
| `[GEOGRAFISCHER FOKUS]` | Geografie | "Deutschland", "DACH-Region", "EU" |
| `[ZEITRAUM]` | Analysezeitraum | "2024–2025", "nächste 3 Jahre" |
| `[DEINE ROLLE]` | Dein Kontext | "Gründer", "Investor", "Produktmanager" |
| `[ZWECK]` | Warum du die Analyse brauchst | "Markteintritts-Entscheidung", "Investor-Pitch-Vorbereitung" |

---

## Nutzungshinweise

**Für bessere Ergebnisse:**
- Gib so viel Kontext wie möglich über deinen spezifischen Fokus
- Wenn du bereits eigene Hypothesen hast, füge sie hinzu: "Ich glaube dass Segment X besonders attraktiv ist – prüfe das"
- Kombiniere mit dem [`competitor-research.md`](./competitor-research.md)-Prompt für eine vollständige Situationsanalyse

**Wichtige Einschränkung:**
Das KI-Modell hat keine Echtzeit-Marktdaten. Zahlen sind Schätzungen auf Basis des Trainingswissens. Für Investor-Pitches oder wichtige Entscheidungen: verifiziere Schlüsselzahlen mit Statista, IBISWorld, Destatis oder Branchenverbänden.

**Follow-up-Prompts:**
- "Vertiefe Segment [X] – ich glaube das ist mein Primärmarkt"
- "Welche konkreten Quellen empfiehlst du um die Marktgröße zu verifizieren?"
- "Was wären die wichtigsten Fragen für Kundeninterviews in diesem Markt?"

---

## Beispiel-Output (anonymisiert)

**Input:** Heimbrauen-Ausrüstung Deutschland, 2024

**Executive Summary:**

Der deutsche Heimbrauen-Markt ist ein Nischenmarkt mit ca. 400.000–600.000 aktiven Hobby-Brauern. Das Marktvolumen für Ausrüstung und Zutaten liegt schätzungsweise bei 80–120 Mio. Euro (Schätzung). Der Markt wächst moderat (5–8% p.a. Schätzung) getrieben durch den allgemeinen DIY-Trend und steigendes Interesse an handwerklichen Lebensmitteln. Der Online-Anteil ist noch relativ niedrig – Chance für fokussierte Anbieter.

**Markttreiber:** DIY-Trend, Craft-Beer-Kultur als Inspirationsquelle, Suchvolumen für "Bier brauen" +40% in 3 Jahren (Schätzung basierend auf Trend-Indikatoren)...

*[Vollständiger Output: ca. 1.200 Wörter]*
