# Corporate LLM Workspace für dein Team

> **LinkedIn Post:** [Link einfügen]
> **Thema:** Infrastruktur · LLM-Zugang für Teams
> **Vollständige Anleitung + Config-Dateien:** [`infrastructure/corporate-llm-workspace/`](../../infrastructure/corporate-llm-workspace/)

## Was ist das?

Eine Schritt-für-Schritt-Anleitung um deinem Team einen eigenen, zentralen LLM-Workspace einzurichten – selbst gehostet, mit Microsoft SSO und Zugriff auf alle großen Modelle über einen einzigen API-Key.

**Die Kernidee:** Kein Mitarbeiter braucht einen eigenen ChatGPT-Account oder API-Key. Alle loggen sich mit dem Firmen-Account ein, du steuerst Zugriff und Kosten zentral.

---

## Das Carousel (6 Folien)

### Folie 1 – Hook
**Dein Team nutzt ChatGPT mit 10 verschiedenen Accounts?**

So richtest du in einer Stunde einen zentralen LLM-Workspace ein – selbst gehostet, mit Microsoft-Login, allen Modellen.

---

### Folie 2 – Der Stack
**Was du brauchst:**

- **Hetzner Server** – ab 3,79 €/Monat, läuft in Deutschland
- **Open Web UI** – die Oberfläche (wie ChatGPT, nur deine)
- **Caddy** – automatisches HTTPS, kein Zertifikats-Stress
- **Requesty** – ein API-Key für GPT-4o, Claude, Gemini, alles

---

### Folie 3 – Schritt 1 & 2
**Server + Domain**

1. Hetzner Cloud → Server hinzufügen → **Docker CE** als Image
2. Typ: CX22 reicht für den Start (~3,79 €/Monat)
3. DNS: A-Record mit Server-IP → `workspace.deinedomain.de`

---

### Folie 4 – Schritt 3 (optional)
**Microsoft SSO einrichten**

Mitarbeiter loggen sich mit dem Firmen-Account ein:

1. Microsoft Entra → App-Registrierung → Redirect URI eintragen
2. Client ID, Tenant ID und Client Secret kopieren
3. In die `docker-compose.yml` eintragen → fertig

---

### Folie 5 – Schritt 4 & 5
**Server konfigurieren & starten**

```bash
ssh root@[IP]
mkdir -p ~/openwebui-caddy && cd ~/openwebui-caddy
# Caddyfile + docker-compose.yml aus dem GitHub-Repo kopieren
docker compose pull && docker compose up -d
```

→ Alles läuft. Browser öffnen, einloggen.

---

### Folie 6 – Requesty einbinden
**Ein API-Key für alle Modelle**

In Open Web UI: Einstellungen → Verbindungen → OpenAI API
- URL: `https://router.requesty.ai/v1`
- Key: dein [Requesty](https://app.requesty.ai/join?ref=c0a72759)-Key

Jetzt können alle Mitarbeiter zwischen GPT-4o, Claude, Gemini und mehr wählen – du siehst in Requesty wer was nutzt.

---

## Dateien & Setup-Anleitung

Die vollständige technische Dokumentation mit `docker-compose.yml` und `Caddyfile` liegt in:

**[`/infrastructure/corporate-llm-workspace/`](../../infrastructure/corporate-llm-workspace/)**

Dort findest du:
- Die komplette Schritt-für-Schritt-Anleitung
- `docker-compose.yml` mit allen Platzhaltern
- `Caddyfile` als Template
