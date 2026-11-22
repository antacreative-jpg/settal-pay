# Déploiement Vercel — SETTAL PAY V2.5.1

Le site web est une application HTML/CSS/JavaScript statique.

## Configuration Vercel
Lors de l'importation du dépôt GitHub :
- Framework Preset : Other
- Root Directory : `SETTAL_PAY_V2_5_1/01_APP_WEB`
- Build Command : laisser vide
- Output Directory : laisser vide
- Install Command : laisser vide

Le fichier `index.html` est le point d'entrée du site.

## À propos de package.json
Aucun `package.json` n'est requis pour servir cette application statique. Les styles et scripts nécessaires sont intégrés dans le HTML ou chargés depuis des CDN.

## À vérifier après déploiement
- Ouvrir le site sur ordinateur et téléphone.
- Vérifier les images de profil : les fichiers `Anta.png` et `image-removebg-preview (82) (1).png` ne sont pas inclus dans l'archive d'origine.
- L'application actuelle est une démonstration front-end : les opérations, récompenses et données ne sont pas reliées à un backend de production.
