# Workflow: Neues Unternehmen gründen

Ein strukturierter Workflow der einen Gründer von der Idee bis zum ersten Go-to-Market begleitet. Vier Phasen, vier Agenten, klare Übergaben.

**Gesamtdauer:** 2–5 Tage (je nach Tiefe)
**Benötigte Agenten:** Research-Agent, CEO-Agent, Operations-Agent, Marketing-Agent

---

## Übersicht

```
PHASE 1          PHASE 2          PHASE 3          PHASE 4
Research    →    Strategie   →   Operations  →    Marketing
─────────────    ─────────────   ────────────      ─────────────
Marktanalyse     Positionierung  Grundprozesse     Go-to-Market
Wettbewerb       OKRs            SOPs              Launch-Plan
Segmente         Business Model  Tools-Setup       Content-Start
   ↓                 ↓               ↓                 ↓
Findings-Doc    Strategie-Doc   Operations-Doc    GTM-Doc
```

---

## Phase 1: Research (Research-Agent)

**Ziel:** Den Markt verstehen bevor strategische Entscheidungen getroffen werden

**Dauer:** 4–8 Stunden (Prompt + Review + Iteration)

**Input:**
- Deine Geschäftsidee in 3-5 Sätzen
- Bekannte Wettbewerber (auch nur 2-3)
- Deine Kernhypothese über den Markt

**Prompt für Research-Agent:**
```
Ich plane [GESCHÄFTSIDEE]. Führe für mich folgende Analysen durch:

1. Marktanalyse: Nutze die Struktur aus [market-analysis.md] für meinen Markt: [MARKT]
2. Wettbewerbsanalyse: Analysiere [BEKANNTE WETTBEWERBER] plus welche du noch kennst
3. Kundensegmente: Identifiziere die 3-4 attraktivsten Segmente für mein Konzept
4. Kernfrage: Ist meine Hypothese "[DEINE HYPOTHESE]" korrekt?

Sei kritisch. Wenn die Hypothese falsch ist, sag es.
```

**Erwarteter Output:** "Findings-Dokument" mit:
- Marktgröße und -wachstum
- Wettbewerbslandschaft und Lücken
- 3-4 Kundensegmente mit Profilen
- Bewertung der Kernhypothese

**Übergabe an Phase 2:** Kopiere das Findings-Dokument vollständig. Es wird der CEO-Agent-Input.

---

## Phase 2: Strategie (CEO-Agent)

**Ziel:** Auf Basis der Research-Findings eine klare Strategie und Positionierung entwickeln

**Dauer:** 2–4 Stunden

**Input:**
- Das vollständige Findings-Dokument aus Phase 1
- Deine persönlichen Rahmenbedingungen (Kapital, Zeit, Team)
- Deine persönlichen Stärken und Schwächen

**Prompt für CEO-Agent:**
```
Basierend auf dieser Marktanalyse [FINDINGS-DOKUMENT EINFÜGEN]:

1. Positionierung: Welches Segment soll ich primär adressieren und warum?
   Entwickle eine klare Positionierungsaussage.

2. Business Model: Welches Geschäftsmodell empfiehlst du? Entwickle das Canvas.

3. Jahresziele (OKRs): Formuliere 3 Objectives mit je 2-3 Key Results für Jahr 1.

4. Kritische Annahmen: Was muss wahr sein damit das funktioniert? (Top 5)

5. Priorität: Was sind die 3 wichtigsten Aktionen in den ersten 30 Tagen?

Meine Rahmenbedingungen: [KAPITAL, ZEIT/WOCHE, TEAM]
Meine Stärken: [STÄRKEN]
Meine Schwächen: [SCHWÄCHEN]
```

**Erwarteter Output:** "Strategie-Dokument" mit:
- Positionierungsaussage
- Business Model Canvas
- Jahresziele (OKRs)
- 30-Tage-Prioritätsliste

**Übergabe an Phase 3:** Strategie-Dokument + Priorisierte 30-Tage-Aktionen

---

## Phase 3: Operations (Operations-Agent)

**Ziel:** Die grundlegenden operativen Strukturen für den Start aufbauen

**Dauer:** 3–5 Stunden

**Input:**
- Die 30-Tage-Prioritätsliste aus Phase 2
- Dein Tech-Stack / verfügbare Tools
- Erste geplante Prozesse (Fulfillment, Kundenservice, etc.)

**Prompt für Operations-Agent:**
```
Ich starte [UNTERNEHMENSNAME]. Basierend auf diesen Prioritäten [30-TAGE-LISTE]:

1. Welche Prozesse brauche ich vom ersten Tag an? Erstelle eine Prioritätsliste.

2. Erstelle eine SOP für [WICHTIGSTEN KERNPROZESS, z.B. "Bestellabwicklung"].

3. Empfehle mir einen minimalen Tech-Stack für den Start.
   Meine Budgetobergrenze: [BUDGET/MONAT]
   Bekannte Anforderungen: [ANFORDERUNGEN]

4. Onboarding-Checkliste: Was muss ich in Woche 1 aufsetzen (Tools, Accounts, Prozesse)?

5. Wann sollte ich was delegieren? Zeig mir einen Delegations-Plan für die ersten 6 Monate.
```

**Erwarteter Output:** "Operations-Dokument" mit:
- Kernprozess-Priorisierung
- Erste SOP
- Tech-Stack-Empfehlung
- Woche-1-Checkliste
- Delegationsplan

**Übergabe an Phase 4:** Operations-Dokument + Strategie-Dokument (Positionierung und Zielgruppe)

---

## Phase 4: Marketing & Go-to-Market (Marketing-Agent)

**Ziel:** Einen konkreten Go-to-Market-Plan entwickeln der die Strategie in Maßnahmen übersetzt

**Dauer:** 3–5 Stunden

**Input:**
- Positionierungsaussage aus Phase 2
- Kundensegmente aus Phase 1
- Verfügbare Marketing-Ressourcen (Budget, Zeit, Kanäle)

**Prompt für Marketing-Agent:**
```
Ich starte [UNTERNEHMENSNAME] mit folgender Positionierung:
[POSITIONIERUNGSAUSSAGE AUS PHASE 2]

Zielgruppe: [PRIMÄRSEGMENT AUS PHASE 1]
Marketing-Budget: [BUDGET/MONAT]
Verfügbare Zeit für Marketing: [STUNDEN/WOCHE]
Meine Kanal-Stärken: [WO BIST DU SCHON AKTIV / WAS KANNST DU]

Entwickle:
1. Messaging-Hierarchie: Hauptversprechen + 3 Kernbotschaften + Proof Points
2. Kanal-Strategie: Welche 2-3 Kanäle für den Start? Warum?
3. Content-Plan: Ersten Monat detailliert, danach Monat 2-3 als Überblick
4. Launch-Kommunikation: Wie kommunizierst du den Start?
5. Lead-Magnet: Was könnte ich kostenfrei anbieten um E-Mail-Adressen zu gewinnen?
6. Erste 3 Texte: Landing-Page-Hero, 1 LinkedIn-Post, 1 E-Mail an potenzielle Erstkunden
```

**Erwarteter Output:** "GTM-Dokument" mit:
- Messaging-Architektur
- Kanal-Strategie mit Begründung
- Content-Kalender Monat 1
- Fertige Texte (Landing Page, Social, E-Mail)

---

## Abschluss: Zusammenführung

Nach Phase 4 hast du vier Dokumente:
1. Findings-Dokument (Research)
2. Strategie-Dokument (CEO)
3. Operations-Dokument (Ops)
4. GTM-Dokument (Marketing)

**Letzter Schritt – CEO-Agent Synthese:**
```
Hier sind meine vier Planungsdokumente nach dem Gründungsworkflow:

[ALLE VIER DOKUMENTE EINFÜGEN]

Zusammenfassung für mich:
1. Bin ich bereit zu starten? Was fehlt noch?
2. Was sind die 5 wichtigsten Aktionen in Woche 1?
3. Was ist die kritischste Annahme die ich in Monat 1 testen muss?
4. Was würdest du mir als erstes von der Liste streichen?
```

---

## Checkliste: Bin ich bereit?

- [ ] Findings-Dokument fertiggestellt und reviewed
- [ ] Positionierung klar und in einem Satz formulierbar
- [ ] Business Model verstanden (wie verdiene ich Geld?)
- [ ] OKRs für Jahr 1 formuliert
- [ ] Kernprozess-SOP erstellt
- [ ] Tech-Stack entschieden und aufgesetzt
- [ ] Landing Page live (oder bereit)
- [ ] Erste Marketing-Texte fertig
- [ ] Woche-1-Plan klar
- [ ] Kritische Annahme identifiziert + Test-Plan dafür
