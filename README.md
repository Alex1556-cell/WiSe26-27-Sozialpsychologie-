# WiSe26-27-Sozialpsychologie-

Präsentation einer empirischen Studie für das Vertiefungsseminar Sozialpsychologie (WiSe 26/27), erstellt mit **Quarto** (Reveal.js).

## Thema

> **Williams, E. F., & Gilovich, T. (2008).** *Do people really believe they are above average?* Journal of Experimental Social Psychology, 44(4), 1121–1128. https://doi.org/10.1016/j.jesp.2008.01.002

Untersucht wird, ob selbstwerterhöhende Trait-Selbsteinschätzungen (Above-Average-Effekt) echte Überzeugungen sind oder bewusst beschönigte Angaben – geprüft über ein **Exchangeability-Verfahren** (Wetten auf den eigenen Rang vs. auf eine Urne mit gematchter Gewinnwahrscheinlichkeit).

Aufbereitet für das Vertiefungsseminar **„Soziales Urteilen und Entscheiden"** (Lehrstuhl für Sozialpsychologie, LMU München) als Teil 1 des Modulportfolios (Präsentation, **max. 30 Minuten**).

**Inhaltlicher Aufbau der Folien**

1. Einleitung & theoretischer Hintergrund
2. Zentrale Forschungsfrage & Hypothesen
3. Methodik & Versuchsdesign (Stichprobe, Ablauf, Operationalisierung, Design-Logik)
4. Ergebnisse (mit Tabellen zu Hauptbefunden und Teststatistiken)
5. Diskussion, Limitationen & theoretische Implikationen

## Repository-Struktur

| Datei | Inhalt |
|:--|:--|
| `index.qmd` | Hauptpräsentation (Reveal.js), 32 Folien inkl. Abschnittsfolien |
| `custom.scss` | eigenes Theme: Farben, Typografie, Tabellen, Boxen, ASCII-Diagramme |
| `_quarto.yml` | Quarto-Projektkonfiguration (`type: website`) |
| `.github/workflows/publish.yml` | automatisches Rendern + Deploy auf GitHub Pages |
| `.gitignore` | ignoriert lokale Build-Artefakte (`.quarto/`, `_site/`) |

## Lokal rendern

Voraussetzung: [Quarto](https://quarto.org/)

```bash
quarto render       # erzeugt _site/index.html
quarto preview      # Live-Vorschau im Browser
```

## Zusammenarbeit

1. Inhalte direkt in `index.qmd` ergänzen oder über Pull Requests abstimmen.
2. Bei Push auf `main` rendert GitHub Actions die Präsentation automatisch und veröffentlicht sie über den `gh-pages`-Branch.

## Hinweise zum Export

- Die Folien laufen **nicht** mit `embed-resources: true`: Das Reveal-Plugin `chalkboard`
  (`chalkboard: true`) ist mit selbst-enthaltenen Ausgaben nicht kompatibel.
- Benötigt man eine **einzelne, in sich geschlossene HTML-Datei** (z. B. für den Upload in
  Moodle), rendert man einmalig ohne Chalkboard:

  ```bash
  quarto render index.qmd -M embed-resources:true -M chalkboard:false
  ```

## Noch anzupassen

- Namen der Kleingruppenmitglieder bzw. präsentierende Personen
- Datum der Seminarsitzung (bewusst nicht fest verdrahtet: Quarto stellt ein unparsebares
  `date`-Feld als „Invalid Date" dar)