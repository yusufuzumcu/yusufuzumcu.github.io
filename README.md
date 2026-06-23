# Portfolio Website — Yusuf Üzümcü

Statische zweisprachige (DE/EN) Portfolio-Seite. Eine `index.html`, ein Foto, sonst nichts.

## Lokal öffnen
Doppelklick auf `index.html` — oder ein lokaler Server für saubere Pfade:

```bash
python3 -m http.server 8000
# Browser: http://localhost:8000
```

## Mit Claude Code bearbeiten
```bash
cd "Portfolio_Website"
claude
```
Dann z. B.: *„Optimiere die Texte im Profil-Abschnitt, DE und EN, im Stil aus ../Voice_Profile_Yusuf_Uezuemcue.md."*
Wichtig: Jeder Text lebt doppelt — `data-de` und `data-en` am selben Element. Beide pflegen.

## Online stellen — GitHub Pages (empfohlen)

Voraussetzung: GitHub-Account + `git` installiert (Check: `git --version`).

1. **Repo auf github.com anlegen** (z. B. `portfolio`), leer, ohne README.
   Für eine saubere URL ohne Unterpfad: Repo `DEINUSERNAME.github.io` nennen.

2. **Lokal verbinden und pushen** (in diesem Ordner):
   ```bash
   git remote add origin https://github.com/DEINUSERNAME/portfolio.git
   git branch -M main
   git push -u origin main
   ```

3. **Pages aktivieren:** GitHub → Repo → *Settings* → *Pages* →
   *Build and deployment* → Source: **Deploy from a branch** →
   Branch: **main**, Ordner: **/ (root)** → *Save*.

4. Nach ca. 1 Minute live unter:
   `https://DEINUSERNAME.github.io/portfolio/`
   (bzw. `https://DEINUSERNAME.github.io/` beim Account-Repo-Namen).

5. **Änderungen veröffentlichen** — nach jeder Bearbeitung:
   ```bash
   git add -A && git commit -m "Texte aktualisiert" && git push
   ```
   Pages baut automatisch neu.

## Alternative — Vercel (Drag & Drop oder CLI)
- Einfachster Weg: Ordner auf https://vercel.com/new ziehen → fertig.
- Oder CLI: `npm i -g vercel` → im Ordner `vercel` ausführen und den Prompts folgen.

## Eigene Domain (optional)
Bei GitHub Pages: *Settings* → *Pages* → *Custom domain* eintragen und beim Domain-Anbieter
einen CNAME-Eintrag auf `DEINUSERNAME.github.io` setzen.
