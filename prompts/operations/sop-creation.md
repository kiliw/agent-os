# SOP-Erstellung – Prompt

## Metadaten

| Feld | Wert |
|------|------|
| **Zweck** | Professionelle Standard Operating Procedure aus einer Prozessbeschreibung erstellen |
| **Empfohlenes Modell** | Claude Sonnet 4.5+, GPT-4o |
| **Outputlänge** | 400–800 Wörter |
| **Vorbereitung** | Prozess in Stichpunkten oder Freitext beschreiben können |

---

## Der Prompt

```
Du bist ein erfahrener Operations-Manager mit Expertise in Prozessdokumentation.

Erstelle eine professionelle Standard Operating Procedure (SOP) für folgenden Prozess:

PROZESSBESCHREIBUNG:
[PROZESS – beschreibe in Stichpunkten oder Freitext was passiert. Sei so detailliert wie möglich.]

KONTEXT:
- Unternehmen/Team: [UNTERNEHMEN/TEAMGRÖSSE, z.B. "E-Commerce, Solo-Betrieb"]
- Häufigkeit: [HÄUFIGKEIT, z.B. "Täglich", "Bei jeder Bestellung", "Wöchentlich"]
- Verantwortliche Person(en): [VERANTWORTLICHE, z.B. "Shop-Betreiber", "Lagermitarbeiter", "Marketing-Verantwortliche"]
- Tools/Systeme im Einsatz: [TOOLS, z.B. "Shopify, DHL-Geschäftskunden-Portal, Outlook"]
- Besondere Anforderungen: [ANFORDERUNGEN, z.B. "Muss DSGVO-konform sein", "Muss von Aushilfen durchführbar sein"]

Erstelle die SOP in folgendem Format:

---

# SOP: [PROZESSNAME]

**Version:** 1.0
**Erstellt:** [Datum]
**Verantwortlich:** [Rolle]
**Überprüfung:** [Empfohlenes Review-Intervall]

## Zweck
[Warum existiert dieser Prozess? Welches Ziel erreicht er?]

## Geltungsbereich
[Wann und für wen gilt diese SOP?]

## Voraussetzungen
- [Was muss vorhanden/vorbereitet sein bevor man startet?]
- [Tool-Zugänge, Materialien, Informationen]

## Prozessschritte

| Schritt | Aktion | Verantwortlich | Tool/System | Ergebnis |
|---------|--------|----------------|-------------|---------|
| 1 | | | | |
| 2 | | | | |
| ... | | | | |

## Ausnahmen & Fehlerbehandlung

| Situation | Was tun? | Eskalation an |
|-----------|----------|--------------|
| [Typische Ausnahme 1] | | |
| [Typische Ausnahme 2] | | |

## Qualitätskontrolle
- Woran erkennt man dass der Prozess korrekt abgeschlossen wurde?
- [Erfolgskriterium 1]
- [Erfolgskriterium 2]

## Checkliste (zum Abhaken)
- [ ] [Kritischer Schritt 1]
- [ ] [Kritischer Schritt 2]
- [ ] [Kritischer Schritt 3]

## Verknüpfte Prozesse
- [Welcher Prozess kommt davor?]
- [Welcher Prozess kommt danach?]

---

Hinweise für mich:
1. Wenn die Prozessbeschreibung Lücken hat, mache Annahmen und kennzeichne sie mit "(Annahme – bitte prüfen)"
2. Wenn du Verbesserungen am Prozess erkennst, füge sie als "Optimierungshinweis" am Ende ein
3. Die SOP soll so klar sein, dass eine Person ohne Vorerfahrung sie durchführen kann
```

---

## Platzhalter-Erklärung

| Platzhalter | Beschreibung | Beispiel |
|-------------|-------------|---------|
| `[PROZESS]` | Was passiert | "Bestellung eingeht → Zahlung prüfen → Ware packen → Versandetikett drucken → Paket übergeben → Tracking an Kunden" |
| `[HÄUFIGKEIT]` | Wie oft | "Bei jeder Bestellung, ca. 5-10x täglich" |
| `[TOOLS]` | Verwendete Software | "Shopify, DHL-Portal, Drucker-App" |

---

## Nutzungshinweise

**Bestes Vorgehen:**
1. Beschreibe den Prozess erstmal so wie er *ist* (nicht wie er sein sollte)
2. Lass die SOP generieren
3. Prüfe auf Lücken und Annahmen
4. Iteriere mit: "Schritt 3 ist falsch – tatsächlich passiert folgendes: ..."

**Follow-up:**
- "Erstelle auf Basis dieser SOP eine vereinfachte Checkliste für den Alltag"
- "Wo siehst du Automatisierungspotenzial in diesem Prozess?"
- "Übersetze diese SOP in eine Version für eine Aushilfskraft ohne Vorkenntnisse"

---

## Beispiel-Output (Auszug)

**Prozess:** Bestellabwicklung für einen kleinen E-Commerce-Shop

```markdown
# SOP: Bestellabwicklung – Täglich

**Version:** 1.0 | **Verantwortlich:** Shop-Betreiber | **Überprüfung:** Quartalsweise

## Prozessschritte

| Schritt | Aktion | Tool | Ergebnis |
|---------|--------|------|---------|
| 1 | Shopify öffnen, neue Bestellungen prüfen | Shopify Admin | Liste offener Bestellungen |
| 2 | Zahlungsstatus prüfen (nur "Bezahlt" weiterbearbeiten) | Shopify | Bestätigung Zahlung eingegangen |
| 3 | Bestellte Artikel aus Lager entnehmen, mit Bestellliste abhaken | Physisch + Bestellliste | Ware bereit |
| 4 | Ware sicher verpacken, Rechnung beilegen | Verpackungsmaterial | Versandfertiges Paket |
| 5 | Versandetikett im DHL-Portal erstellen und drucken | DHL Geschäftskunden-Portal | Etikett + Tracking-Nummer |
```
