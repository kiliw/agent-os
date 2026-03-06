# Posts – Begleitmaterial

Jeder Ordner hier begleitet einen veröffentlichten Blog-Post. Er enthält die Prompts, Agenten-Konfigurationen und Beispiele aus dem Post – direkt nutzbar, ohne den Post nochmal lesen zu müssen.

## Warum das?

Blog-Posts erklären das *Warum* und das *Wie*. Dieser Ordner liefert das *Was* – die konkreten Dateien die man sofort kopieren und einsetzen kann. So bleibt der Wert auch dann erhalten, wenn man den Post nicht mehr vor Augen hat.

## Struktur eines Post-Ordners

```
posts/
└── [post-slug]/
    ├── README.md           # Kurzbeschreibung, Link zum Post, Überblick
    └── prompts/
        ├── prompt-1.md     # Konkrete Prompts aus dem Post
        └── prompt-2.md
```

## Verfügbare Posts

*(Wird ergänzt wenn Posts veröffentlicht werden)*

| Post | Beschreibung | Ordner |
|------|-------------|--------|
| – | – | – |

## Neuen Post-Begleiter erstellen

Nutze den Template-Ordner [`_template/`](./_template/) als Ausgangspunkt. Kopiere ihn, benenne ihn nach dem Post-Slug (z.B. `wie-ich-meinen-research-agenten-gebaut-habe`), und ersetze alle Platzhalter.

## Hinweis

Post-Ordner sind bewusst schlank gehalten. Sie verweisen auf die zentrale Prompt-Bibliothek unter [`/prompts/`](../prompts/) wenn ein Prompt allgemein nützlich ist – und enthalten nur Post-spezifische Ergänzungen direkt.
