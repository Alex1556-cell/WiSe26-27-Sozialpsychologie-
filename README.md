# WiSe26-27-Sozialpsychologie-

Erstellung der PPT-/Präsentationsfolien für das Seminar in Sozialpsychologie WiSe26/27 mit **Quarto**.

## Repository-Struktur

- `index.qmd` – Hauptpräsentation (Reveal.js)
- `_quarto.yml` – Quarto-Projektkonfiguration
- `.github/workflows/publish.yml` – automatisches Rendern + Deploy auf GitHub Pages
- `.gitignore` – ignoriert lokale Build-Artefakte (`.quarto/`, `_site/`)

## Zusammenarbeit

1. Inhalte direkt in `index.qmd` ergänzen oder über Pull Requests abstimmen.
2. Bei Push auf `main` oder `master` rendert GitHub Actions die Präsentation automatisch.
3. Veröffentlichung läuft über den `gh-pages`-Branch.

## Lokal testen (optional)

Voraussetzung: [Quarto](https://quarto.org/)

```bash
quarto render
quarto preview
```
