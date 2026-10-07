# zeiterfassung-at

## Zweck
Reine Weiterleitung: `zeiterfassung.herzjesugym.at` → `https://zeiterfassung.herzjesugym.com` (Pfad, Query und Anker bleiben erhalten).
Die eigentliche App liegt im privaten Repo `Dendak/zeiterfassung-quelle`, gebaut im öffentlichen Repo `Dendak/zeiterfassung` (Branch `gh-pages`).

## Stack
Statisches HTML, kein Build. Weiterleitung per `location.replace` (JS) mit `<meta http-equiv="refresh">` als Fallback.

## Struktur
- `index.html` – Weiterleitung
- `404.html` – identisch zu `index.html`, damit auch Unterpfade weitergeleitet werden
- `CNAME` – `zeiterfassung.herzjesugym.at`
- `README.md`

## Befehle
Keine. Zum lokalen Testen reicht es, `index.html` im Browser zu öffnen.

## Deployment
GitHub Pages (Legacy-Build) aus Branch `main`, Ordner `/`. **Jeder Push auf `main` geht sofort live.**

## Vorsicht
- `index.html` und `404.html` müssen inhaltlich gleich bleiben.
- `CNAME` nicht löschen oder ändern (wurde schon einmal gelöscht und neu angelegt). Sonst geht die Domain verloren.
- Ziel-Domain ändert sich → in beiden HTML-Dateien jeweils an drei Stellen anpassen (canonical, script, meta refresh).

## Notizen
Offene Punkte und Verlauf: [docs/POZNAMKY.md](docs/POZNAMKY.md)
