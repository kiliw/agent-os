# Wettbewerbsanalyse – Prompt

## Metadaten

| Feld | Wert |
|------|------|
| **Zweck** | Strukturierte Wettbewerbsanalyse mit Positionierungsmap und Lücken |
| **Empfohlenes Modell** | Claude Sonnet 4.5+, GPT-4o (mit Web-Browsing für aktuelle Daten) |
| **Outputlänge** | 700–1200 Wörter |
| **Vorbereitung** | Liste bekannter Wettbewerber, eigene Positionierungshypothese |

---

## Der Prompt

```
Du bist ein erfahrener Wettbewerbsanalyst. Deine Aufgabe ist eine strukturierte
Wettbewerbsanalyse für folgenden Kontext:

Mein Unternehmen/Produkt: [EIGENES PRODUKT/UNTERNEHMEN beschreiben]
Meine Zielgruppe: [ZIELGRUPPE]
Bekannte Wettbewerber: [WETTBEWERBER LISTE, z.B. "Anbieter A, Anbieter B, Anbieter C"]
Meine Hypothese zur Differenzierung: [DIFFERENZIERUNGSHYPOTHESE oder "noch unklar"]

Erstelle folgende Analyse:

## 1. Wettbewerbslandschaft – Überblick
- Marktstruktur: Wie viele Anbieter? Fragmentiert oder dominiert von wenigen?
- Wettbewerbs-Typen: Kategorisiere die Konkurrenz (z.B. "Generalist", "Nischen-Spezialisten", "D2C-Pure-Player", "Stationäre Händler online gegangen")
- Intensität: Wie hart ist der Wettbewerb? (niedrig/mittel/hoch) + Begründung

## 2. Einzelanalyse Hauptwettbewerber
Für jeden bekannten Wettbewerber (und 1-2 weitere die du kennst):

### [WETTBEWERBER NAME]
- Positionierung (ein Satz):
- Zielgruppe:
- Preissegment: [günstig / mid / premium]
- Stärken (2-3):
- Schwächen (2-3):
- Geschätzte Marktstellung: [Marktführer / Challenger / Nischen-Spieler]

## 3. Positionierungsmap (als Text)
Beschreibe die Positionierungslandschaft auf zwei relevanten Achsen.
Wähle die zwei Dimensionen die in diesem Markt am wichtigsten differenzieren.

Achse 1: [DIMENSION 1, z.B. "Preis: niedrig ←→ hoch"]
Achse 2: [DIMENSION 2, z.B. "Service: Self-Service ←→ Full-Service"]

Beschreibe wo jeder Wettbewerber und ich auf dieser Map stehe.

## 4. Marktlücken und Chancen
- Welche Kundenbedürfnisse werden aktuell nicht gut bedient?
- Welche Preissegmente sind unterversorgt?
- Welche Zielgruppen werden vernachlässigt?
- Welche Kombination aus Preis und Service existiert noch nicht?

## 5. Differenzierungsoptionen für [EIGENES UNTERNEHMEN]
Basierend auf der Analyse:
- Option A: [Differenzierungsansatz + Begründung]
- Option B: [Differenzierungsansatz + Begründung]
- Option C: [Differenzierungsansatz + Begründung]
- Empfehlung: Welche Option siehst du als stärkste und warum?

## 6. Wettbewerbsrisiken
- Was passiert wenn Wettbewerber X seinen Preis senkt?
- Was passiert wenn ein gut finanzierter Player in den Markt eintritt?
- Welche "Moats" (Schutzgräben) sollte ich aufbauen?

Kennzeichne alle Angaben die du nicht sicher kennst mit "(Annahme)" oder "(Schätzung)".
```

---

## Platzhalter-Erklärung

| Platzhalter | Beschreibung | Beispiel |
|-------------|-------------|---------|
| `[EIGENES PRODUKT/UNTERNEHMEN]` | Was du anbietest | "Online-Shop für Premium-Heimbrauen-Starter-Kits, 199€, inkl. Video-Support" |
| `[ZIELGRUPPE]` | Wen du ansprechen willst | "Männer 30-45, Einsteiger ohne Vorkenntnisse, zahlungsbereit" |
| `[WETTBEWERBER LISTE]` | Bekannte Konkurrenten | "Braumarkt.de, Hopfen und mehr GmbH, MrMalt" |
| `[DIFFERENZIERUNGSHYPOTHESE]` | Deine Vermutung | "Wir sind die Einzigen mit Video-Begleitung" |

---

## Nutzungshinweise

**Tipp:** Bereite vor dem Prompt eine kurze Eigenrecherche vor:
- Schau dir die Websites der Hauptwettbewerber an
- Notiere Preispunkte und Marketing-Botschaften
- Lies 5-10 Kundenbewertungen auf Amazon/Google

Je mehr du dem Modell mitgibst, desto präziser die Analyse.

**Mit Web-Browsing:**
Wenn du ein Modell mit Web-Zugang nutzt: "Bitte recherchiere aktuelle Informationen zu [WETTBEWERBER] bevor du die Analyse erstellst."

**Follow-up:**
- "Analysiere die Schwachstelle von [WETTBEWERBER X] tiefer – wie könnte ich daraus eine Positionierung bauen?"
- "Entwerfe eine Positioning-Statement für mich auf Basis der Lücken die du identifiziert hast"
