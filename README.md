# here – Datenschutzerklärung (Website)

Statische Seite für die Datenschutzerklärung der App „here". Wird per GitHub Pages gehostet
und auf eine eigene Subdomain gelegt (z. B. `datenschutz.deine-domain.de`).

## 1. Platzhalter ausfüllen
In `index.html` alle `[ECKIGEN PLATZHALTER]` ersetzen (Name/Firma, Anschrift, E-Mail).
Im Footer ggf. den Link zur AGB-Subdomain anpassen.

## 2. Subdomain eintragen
`CNAME.example` in **`CNAME`** umbenennen und den Inhalt durch deine echte Subdomain ersetzen, z. B.:
```
datenschutz.deine-domain.de
```

## 3. Als eigenes GitHub-Repo pushen
```bash
cd datenschutz
git init
git add .
git commit -m "Datenschutzerklärung here"
git branch -M main
git remote add origin https://github.com/<DEIN-USER>/here-datenschutz.git
git push -u origin main
```

## 4. GitHub Pages aktivieren
Repo → **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main / (root)** → Save.
Unter **Custom domain** deine Subdomain eintragen (falls noch nicht via CNAME-Datei gesetzt) und
„Enforce HTTPS" aktivieren (kann ein paar Minuten dauern).

## 5. DNS bei deinem Domain-Anbieter
Einen **CNAME-Record** anlegen:
```
Host/Name:  datenschutz
Ziel/Value: <DEIN-USER>.github.io
```
Nach DNS-Propagation ist die Seite unter `https://datenschutz.deine-domain.de` erreichbar.

## 6. In App Store Connect
Diese URL als **Privacy Policy URL** hinterlegen.
