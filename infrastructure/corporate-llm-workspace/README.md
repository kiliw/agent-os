# Corporate LLM Workspace: Open Web UI auf Hetzner

Ein selbst gehosteter LLM-Workspace für dein Team – auf Basis von [Open Web UI](https://openwebui.com/) als Interface, [Caddy](https://caddyserver.com/) als Reverse Proxy mit automatischem HTTPS und [Requesty](https://app.requesty.ai/join?ref=c0a72759) als LLM-Router.

Ergebnis: Alle Mitarbeiter loggen sich über Microsoft SSO ein und haben sofort Zugriff auf die besten verfügbaren Modelle – ohne eigene API-Keys, ohne ChatGPT-Accounts.

---

## Was du bekommst

- **Open Web UI** – ChatGPT-ähnliche Oberfläche, selbst gehostet
- **Microsoft SSO** – Login mit bestehenden Firmen-Accounts (optional)
- **Caddy** – Automatisches HTTPS für deine Domain, kein Zertifikats-Management nötig
- **Watchtower** – Hält Open Web UI automatisch aktuell
- **Requesty** – LLM-Router: ein API-Key, alle Modelle (GPT-4o, Claude, Gemini, etc.)

---

## Voraussetzungen

- Hetzner Cloud Account
- Eine Domain mit Zugriff auf DNS-Einstellungen
- (Optional) Microsoft Entra / Azure AD für SSO

---

## Schritt 1: Hetzner Server erstellen

1. Gehe auf [hetzner.com](https://www.hetzner.com/cloud) und erstelle ein neues Projekt
2. Klicke auf **Server hinzufügen**
   - Standort: z. B. Nürnberg oder Falkenstein
   - Image: unter **Apps** → **Docker CE** auswählen
   - Typ: `CX22` (ab ~3,79 €/Monat) reicht für den Start, `CX42` für mehr Leistung
3. SSH-Key hinterlegen (empfohlen statt Root-Passwort)
4. **Kostenpflichtig bestellen** → IP-Adresse notieren

---

## Schritt 2: DNS konfigurieren

Bei deinem Domain-Anbieter eine Subdomain anlegen:

| Typ | Name | Wert |
|-----|------|------|
| A | `workspace` | `[Hetzner IP]` |

→ Erreichbar unter `workspace.deinedomain.de`

DNS-Propagierung kann einige Minuten dauern.

---

## Schritt 3: Microsoft SSO einrichten (optional)

Für Login mit Firmen-Accounts via Microsoft Entra:

1. Öffne das [Microsoft Entra Admin Center](https://entra.microsoft.com)
2. **App-Registrierungen** → **Neue Registrierung**
   - Plattform: **Web**
   - Redirect URI: `https://workspace.deinedomain.de/oauth/microsoft/callback`
3. Notiere dir:
   - **Anwendungs-ID** → `MICROSOFT_CLIENT_ID`
   - **Verzeichnis-ID** → `MICROSOFT_CLIENT_TENANT_ID`
4. Unter **Zertifikate und Geheimnisse** → neuen Client-Schlüssel erstellen → Wert kopieren → `MICROSOFT_CLIENT_SECRET`

---

## Schritt 4: Server einrichten

Per SSH einloggen:

```bash
ssh root@[HETZNER_IP]
```

Ordner anlegen:

```bash
mkdir -p ~/openwebui-caddy
cd ~/openwebui-caddy
```

Caddyfile erstellen (Domain ersetzen):

```bash
cat > Caddyfile <<'EOF'
workspace.deinedomain.de {
    reverse_proxy open-webui:8080
}
EOF
```

---

## Schritt 5: docker-compose.yml anlegen

Die Datei [`docker-compose.yml`](./docker-compose.yml) aus diesem Ordner auf den Server kopieren oder direkt erstellen:

```bash
nano docker-compose.yml
```

Platzhalter ersetzen:

| Platzhalter | Wert |
|-------------|------|
| `{DEINE.DOMAIN.DE}` | z. B. `workspace.deinedomain.de` |
| `{MICROSOFT_CLIENT_ID}` | aus Schritt 3 |
| `{MICROSOFT_CLIENT_SECRET}` | aus Schritt 3 |
| `{MICROSOFT_CLIENT_TENANT_ID}` | aus Schritt 3 |

---

## Schritt 6: Starten

```bash
docker compose pull
docker compose up -d
```

Danach im Browser `https://workspace.deinedomain.de` aufrufen → **Loslegen** → Microsoft-Login.

---

## Requesty als LLM-Router einbinden

Statt direkt OpenAI- oder Anthropic-API-Keys zu hinterlegen, nutze [Requesty](https://app.requesty.ai/join?ref=c0a72759) als Router:

1. Requesty-Account erstellen und API-Key generieren
2. In Open Web UI: **Einstellungen → Verbindungen → OpenAI API**
   - URL: `https://router.requesty.ai/v1`
   - API-Key: dein Requesty-Key
3. Alle verfügbaren Modelle (GPT-4o, Claude, Gemini, etc.) sind damit nutzbar

**Vorteil:** Ein zentraler API-Key für alle Mitarbeiter, Usage-Tracking pro Nutzer, einfaches Modell-Management.

---

## Dateien in diesem Ordner

| Datei | Beschreibung |
|-------|-------------|
| [`docker-compose.yml`](./docker-compose.yml) | Vollständige Docker-Konfiguration mit Platzhaltern |
| [`Caddyfile`](./Caddyfile) | Reverse-Proxy-Konfiguration (Template) |

---

*Basiert u. a. auf dem Tutorial von [Everlast AI](https://www.youtube.com/watch?v=uv0fL2nEtSI) – ein empfehlenswerter Kanal um bei KI allgemein up to date zu bleiben.*
