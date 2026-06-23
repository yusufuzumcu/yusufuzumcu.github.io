# Portfolio-Website — Yusuf Üzümcü

## Was das ist
Persönliche Bewerbungs-/Portfolio-Website. Eine statische Single-Page-Site, gebaut als
**eine** `index.html` (HTML + CSS + JS inline) plus `assets/headshot.jpg`.
Kein Build-Step, kein Framework, keine Abhängigkeiten — Datei im Browser öffnen genügt.

Zweck: in Vorstellungsgesprächen die eigene Person präsentieren. Senior, ruhig, technisch.

## Struktur
- `index.html` — komplette Seite (Styles im `<style>`, Logik im `<script>` am Ende).
- `assets/headshot.jpg` — Bewerbungsfoto.

## Wichtige Eigenschaften (beim Bearbeiten erhalten)
- **Zweisprachig DE/EN.** Jeder sichtbare Text steht in zwei Attributen am selben Element:
  `data-de="…"` und `data-en="…"`. Der DE/EN-Umschalter oben rechts ruft `setLang(l)` auf,
  das pro Element `data-de` bzw. `data-en` in den Inhalt schreibt.
  → **Neuer/geänderter Text muss IMMER in beiden Attributen gepflegt werden.**
  Der initial im Element stehende Inhalt sollte mit `data-de` übereinstimmen (Default ist Deutsch).
- **Foto** wird relativ geladen (`assets/headshot.jpg`). Austausch: Datei ersetzen, Name gleich lassen.
- **Grafiken** sind reines Inline-SVG/CSS (Balken, Donut) — kein CDN, funktioniert offline.
  Balkendaten stehen im `<script>` im Array `bars`.
- Dark Theme über CSS-Variablen in `:root` (`--acc` = Bronze-Akzent, `--teal` = Zweitakzent).

## Tonalität beim Texten (sehr wichtig)
Texte im Stil von Yusuf. Vollständiges Voice Profile liegt eine Ebene höher:
`../Voice_Profile_Yusuf_Uezuemcue.md` — bei Textänderungen lesen.

Kurzfassung der harten Regeln:
- Substanz vor Schaum. Konkrete Zahlen, aktive Formulierungen, jedes Wort muss arbeiten.
- Nutzen fürs Unternehmen betonen.
- Verboten: „nichtsdestotrotz", „diesbezüglich", „hinsichtlich", „am Ende des Tages",
  „natürlich/klar" als Floskel, aufgesetzte Begeisterung, Überverkaufen, Luftschlösser.
- Keine veralteten Konjunktive, keine Standardfloskeln.
- Faktischer Kontext = diplomatischer, sachlicher Ton (kein mündlicher Schärfe-Modus).

## Lokal ansehen
`index.html` per Doppelklick öffnen, oder lokaler Server:
```
python3 -m http.server 8000   # dann http://localhost:8000
```

## Deployment
Statische Seite — überall hostbar. Schritt-für-Schritt siehe `README.md`.
Empfehlung: GitHub Pages (kostenlos, Git-basiert, passt zum Edit-im-Terminal-Workflow).

## Hinweis Datenschutz
Dieser Ordner enthält nur Website-Dateien und darf öffentlich gehostet werden.
Persönliche Unterlagen (CV, Zeugnisse, Voice Profile) liegen außerhalb dieses Ordners
und gehören **nicht** ins öffentliche Repo.
