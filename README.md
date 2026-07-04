# ARIA — Gestion de chantier

Tableau de bord de maîtrise d'œuvre pour le suivi de chantier (comptes rendus
de réunion, assistant IA sur les pièces écrites/CCTP, documents, planning).

Importé depuis le projet Claude Design `ARIA.dc.html` et décompacté en un
projet web statique autonome.

## Structure

- `index.html` — l'application (markup Claude Design `<x-dc>` avec directives
  réactives `sc-if` / `sc-for`), références d'assets pointant vers `assets/`.
- `assets/aria-runtime.js` — le runtime Claude Design qui rend les éléments
  `<x-dc>` et gère la réactivité.
- `assets/aria-logo.png` — logo ARIA.
- `assets/fonts/` — polices Tabler Icons (eot/woff2/woff/ttf).

Les ressources étaient encodées en base64 (et compressées en gzip) dans le
bundle d'origine ; elles ont été décodées/décompressées en fichiers réels.

## Lancer en local

Servir le dossier via un serveur statique (les `<script src>` ne se chargent
pas en `file://`) :

```bash
npx serve .
# ou
python -m http.server 8000
```

Puis ouvrir http://localhost:8000 (ou le port indiqué).
