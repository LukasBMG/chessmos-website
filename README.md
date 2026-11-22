# chessmos.de

Statische Webseite für Chessmos: Startseite, Support, Impressum, Datenschutz.
Kein Build-Schritt; der Inhalt dieses Ordners wird so wie er ist veröffentlicht.

| Seite | URL | Wofür |
|---|---|---|
| `index.html` | https://chessmos.de/ | Startseite (App Store: Marketing-URL) |
| `support/` | https://chessmos.de/support/ | App Store: Support-URL |
| `datenschutz/` | https://chessmos.de/datenschutz/ | App Store + `EXPO_PUBLIC_PRIVACY_URL` |
| `privacy/` | https://chessmos.de/privacy/ | leitet auf den englischen Teil weiter |
| `impressum/` | https://chessmos.de/impressum/ | Pflichtangaben nach § 5 DDG |

## Veröffentlichen (GitHub Pages)

1. Neues **öffentliches** Repo anlegen (z. B. `chessmos-website`) und den
   **Inhalt** dieses Ordners hochladen (inkl. `CNAME` und `.nojekyll`).
2. Repo → Settings → Pages: Source „Deploy from a branch“, `main` / `(root)`;
   Custom domain `chessmos.de`.
3. united-domains → DNS: A-Eintrag ohne Subdomain (Parkseite 89.31.143.90)
   löschen, dafür vier A-Einträge ohne Subdomain: 185.199.108.153,
   185.199.109.153, 185.199.110.153, 185.199.111.153. Den `*`-Eintrag löschen.
   CNAME `www` → `<github-name>.github.io`. Resend-Einträge (`send`, `rsend`,
   `resend._domainkey`, `_dmarc`) nicht anfassen.
4. Nach der Zertifikatsausstellung in Settings → Pages „Enforce HTTPS“ setzen.

Änderungen hier im App-Repo pflegen und danach ins Webseiten-Repo kopieren.
