# Beitragen zu Agent OS

Danke für dein Interesse. Agent OS lebt davon, dass Praktiker ihre erprobten Prompts, Agenten-Konfigurationen und Erkenntnisse teilen. Jeder Beitrag macht das System nützlicher für alle.

---

## Was du beitragen kannst

### Prompts

Neue Prompts unter `prompts/` sind die wertvollste Beitragsform:

1. Fork das Repository
2. Erstelle eine neue Datei in der passenden Kategorie (`prompts/business/`, `prompts/operations/`, `prompts/content/`)
3. Nutze die Struktur aus [`posts/_template/prompts/example-prompt.md`](./posts/_template/prompts/example-prompt.md) als Vorlage
4. Stelle sicher dass der Prompt:
   - Sofort einsetzbar ist (nicht nur beschreibt was er tut)
   - Klare `[PLATZHALTER]` für anpassbare Teile hat
   - Einen Beispiel-Output enthält (anonymisiert)
   - Einen Hinweis enthält mit welchem Modell er getestet wurde
5. Erstelle einen Pull Request mit einer kurzen Beschreibung

### Agenten-Definitionen

Neue Agenten oder Verbesserungen bestehender Agenten:

1. Neue Agenten kommen in einen eigenen Ordner unter `agents/[agent-name]/`
2. Nutze [`agents/AGENT_TEMPLATE.md`](./agents/AGENT_TEMPLATE.md) als Vorlage
3. Jeder Agent braucht: `README.md`, `system-prompt.md`, `use-cases.md`
4. System-Prompts müssen generisch sein – keine unternehmensspezifischen Daten
5. Use Cases müssen konkret sein – kein "Man könnte X machen", sondern ein echter Beispiel-Input

### Beispiele

Echte Outputs zeigen was möglich ist:

1. Neue Beispiele unter `examples/[thema]/`
2. Jedes Beispiel braucht: `README.md`, `prompt-used.md`, `example-output.md`
3. Outputs müssen vollständig anonymisiert sein – keine echten Unternehmens-, Personen- oder Produktnamen

### Workflows

Neue Multi-Agenten-Workflows:

1. Neue Datei unter `workflows/[workflow-name].md`
2. Klare Phasen mit Agenten, Inputs, Outputs und Übergaben
3. Muss mit den vorhandenen Agenten funktionieren oder klar angeben welche neuen Agenten nötig wären

---

## Code of Conduct

Kurz und bündig:

- **Respektvoll** – Konstruktives Feedback, keine persönlichen Angriffe
- **Konkret** – Issues und PRs mit klarer Beschreibung des Problems oder der Verbesserung
- **Generisch** – Kein firmenspezifischer, privater oder vertraulicher Content
- **Ehrlich** – Wenn ein Prompt nicht funktioniert hat, sag es. Negative Erfahrungen sind genauso wertvoll

---

## Was NICHT ins Repo gehört

- **Firmenspezifische Daten** – Keine echten Kundendaten, Produktnamen, internen Prozesse
- **API-Keys oder Credentials** – Niemals, auch nicht in Kommentaren
- **Ungetestete Prompts** – Bitte jeden Prompt mindestens einmal mit einem echten Modell testen
- **Werbung oder Spam** – Keine Links zu kommerziellen Tools ohne direkte Relevanz
- **Große Binärdateien** – Keine PDFs, Bilder (außer wenn absolutely nötig), Datenbankdumps

Der Ordner `private/` ist in `.gitignore` – du kannst lokale, private Anpassungen dort speichern ohne Risiko eines versehentlichen Commits.

---

## Prozess

1. **Issue öffnen** – Für größere Änderungen erst als Issue diskutieren
2. **Fork & Branch** – Arbeite immer auf einem eigenen Branch (`feature/neuer-prompt-name`)
3. **Pull Request** – Kurze Beschreibung: Was, Warum, wie getestet
4. **Review** – Mindestens ein Maintainer schaut drüber
5. **Merge** – Bei Zustimmung wird gemerged

Bei Fragen: Öffne ein Issue mit dem Label `question`.
