# Workflow-Design – Prompt

## Metadaten

| Feld | Wert |
|------|------|
| **Zweck** | Strukturierten Workflow mit Verantwortlichkeiten und Tools aus einer Aufgabenbeschreibung designen |
| **Empfohlenes Modell** | Claude Sonnet 4.5+, GPT-4o |
| **Outputlänge** | 500–900 Wörter |
| **Vorbereitung** | Aufgabe oder Ziel klar beschreiben, beteiligte Rollen und Tools kennen |

---

## Der Prompt

```
Du bist ein erfahrener Workflow-Designer mit Fokus auf schlanke, skalierbare Prozesse.

Designe einen strukturierten Workflow für folgende Aufgabe/Ziel:

AUFGABE/ZIEL:
[AUFGABE – Was soll durch den Workflow erreicht werden?]

KONTEXT:
- Beteiligte Rollen/Personen: [ROLLEN, z.B. "Gründer, Freelance-Texter, Kund:in"]
- Verfügbare Tools: [TOOLS, z.B. "Notion, Slack, Calendly, Google Docs, Mailchimp"]
- Häufigkeit: [HÄUFIGKEIT, z.B. "Wöchentlich", "Pro Kundenprojekt", "Bei Bedarf"]
- Besondere Anforderungen: [z.B. "Asynchron möglich", "Max. 2h Zeitaufwand", "Skalierbar auf 50 Kunden"]

Erstelle folgendes:

## 1. Workflow-Übersicht
Ein visueller Ablauf als Text-Diagramm:
[INPUT] → [Phase 1] → [Entscheidungspunkt?] → [Phase 2a / Phase 2b] → [OUTPUT]

## 2. Detaillierter Workflow

Für jede Phase:

### Phase [N]: [PHASENAME]
- **Trigger:** Was startet diese Phase?
- **Verantwortlich:** Wer führt sie durch?
- **Aktivitäten:**
  1. [Schritt 1]
  2. [Schritt 2]
- **Tools:** Welche Tools werden genutzt?
- **Output:** Was ist das Ergebnis dieser Phase?
- **Übergabe an:** Wer/was kommt als nächstes?
- **Zeitaufwand:** Geschätzte Dauer

## 3. Entscheidungspunkte
Wo gibt es "Wenn X dann Y"-Verzweigungen?

| Situation | Wenn JA | Wenn NEIN |
|-----------|---------|-----------|
| [Entscheidung 1] | → | → |
| [Entscheidung 2] | → | → |

## 4. Metriken & Erfolgskontrolle
- Wie misst man ob der Workflow funktioniert?
- [KPI 1: z.B. "Durchlaufzeit < 3 Tage"]
- [KPI 2: z.B. "Fehlerquote < 5%"]
- Wann sollte der Workflow überarbeitet werden?

## 5. Optimierungspotenziale
- Was kann automatisiert werden?
- Wo entstehen typischerweise Verzögerungen?
- Was kann weggelassen werden ohne den Output zu verschlechtern?

Kennzeichne Annahmen mit "(Annahme)". Wenn du alternative Workflow-Designs siehst, erwähne die beste Alternative kurz.
```

---

## Platzhalter-Erklärung

| Platzhalter | Beschreibung | Beispiel |
|-------------|-------------|---------|
| `[AUFGABE]` | Was erreicht werden soll | "Onboarding eines neuen Freelance-Texters in unser Content-System" |
| `[ROLLEN]` | Wer beteiligt ist | "Gründer (Auftraggeber), Freelancer (Ausführender), ggf. Kund:in (Abnehmer)" |
| `[TOOLS]` | Verfügbare Software | "Notion (Aufgaben), Loom (Video-Erklärungen), Slack (Kommunikation), Drive (Dateien)" |
| `[HÄUFIGKEIT]` | Wie oft läuft der Workflow | "Einmalig pro neuem Freelancer" |

---

## Nutzungshinweise

**Wann diesen Prompt nutzen:**
- Neue Zusammenarbeit mit Freelancern oder Mitarbeitern strukturieren
- Wiederkehrendes Projekt (z.B. jeden Monat ein Blog-Post) systematisieren
- Kundenprojekte standardisieren
- Interne Prozesse vor der Automatisierung dokumentieren

**Tipp:** Wenn du den Workflow schon grob im Kopf hast, skizziere ihn zuerst selbst in 5 Stichpunkten. Dann gibt dem Modell diese Skizze als Basis – das Ergebnis ist präziser.

**Follow-up:**
- "Wie würde dieser Workflow aussehen wenn ich ihn auf 10x Volumen skaliere?"
- "Welche Schritte in diesem Workflow könnten durch [TOOL] automatisiert werden?"
- "Erstelle ein Onboarding-Dokument für eine neue Person die diesen Workflow übernimmt"

---

## Beispiel-Output (Auszug)

**Aufgabe:** Wöchentlicher Content-Produktions-Workflow für Blog + Social Media

**Workflow-Übersicht:**
```
[Thema-Idee] → [Briefing schreiben] → [Freelancer beauftragt?]
                                              ↓ Ja              ↓ Nein (Selbst schreiben)
                                    [Briefing senden]     [Draft direkt]
                                              ↓
                                    [Draft erhalten]
                                              ↓
                                    [Review & Freigabe] → [Überarbeitung nötig?]
                                                                ↓ Nein
                                                       [Veröffentlichung + Social]
                                                                ↓
                                                          [Newsletter-Teaser]
                                                                ↓
                                                           [OUTPUT: Publiziert]
```
