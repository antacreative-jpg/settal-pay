# SETTAL PAY V2.5.1 — plugin Figma + application web (FR · Wolof · English)

## Importer dans Figma (30 secondes)
1. Décompresser ce ZIP.
2. Figma Desktop → Plugins → Development → **Import plugin from manifest…** → `02_FIGMA_PLUGIN/manifest.json`
3. Plugins → Development → **SETTAL PAY V2.5.1 — Complete UI + Design System**.
   ⏱ La génération est plus longue qu'en V2.4 (≈ 160 écrans au lieu de 48) : attendre le message final, ne pas relancer.
4. Le message de fin donne le nombre d'écrans, de liens, de textes non traduits (doit être 0) et les éventuels avertissements. En cas de « ⚠ » ou « lien refusé », copier le message tel quel.
Ne jamais importer le HTML dans Figma : seul `manifest.json` sert à l'import. Le plugin n'utilise aucun réseau.

## Nouveautés V2.5
### 1. Bouton flottant « ✦ Impact & IA » (comme dans l'app web)
Présent sur tous les écrans à barre de navigation (Accueil, Scanner, Borne détectée, Carte, Historique, Classement, Défis, Boutique, Profil), y compris en mode sombre. Il ouvre l'écran **20 · Impact & IA**.

### 2. Écrans « complets » (toute la page de l'app web)
- **20 · Impact & IA** : désormais l'écran entier (1310 px de haut, défilant en mode présentation) : pastille « Données synchronisées », impact cumulé, métriques, Prévision IA avec sa description, Activité des dépôts (7 jours), **Qualité des données** (tableau Poids / Type matière / Horodatage), note de confidentialité, barre de navigation.
- **25 · Aperçu administrateur** : désormais l'écran entier (1350 px) : Pilotage prédictif + LIVE DEMO, Prévision collecte, Rapport RSE (+ bouton « Générer un rapport »), Supervision des bornes, note Anti-fraude, note de démonstration, accès au dashboard.
- **Mode sombre étendu** : en plus de Paramètres / Accueil / Impact / Profil, il existe maintenant des versions sombres de Scanner, Carte, Historique, Défis, Boutique et Classement (section « D »). Les onglets et le bouton flottant restent en sombre.

### 3. Langues : Français · Wolof · English, qui fonctionnent
- Le plugin génère **trois jeux d'écrans complets (FR, Wolof, English) tous sur la même page `03 — MOBILE APP`**, empilés les uns sous les autres, chacun avec ses écrans d'administration. (Figma ne permet pas les liens de prototype entre deux pages : c'est pour cela que tout est sur une seule page, sinon « Voir le dashboard » et les boutons de langue ne répondent pas.)
- **Paramètres → Langue** : cliquer sur 🇸🇳 Wolof ou 🇬🇧 English (mode présentation ▶) ouvre le même écran Paramètres dans la langue choisie ; la langue active est surlignée. L'écran « 26 · Langue » (Actif / Choisir) fonctionne de la même façon, et tout le prototype (navigation, toasts, admin, mode sombre) reste dans la langue choisie.
- Chaque écran d'une autre langue porte le suffixe `[WO]` ou `[EN]` ; points de départ de prototype supplémentaires (W1–W7, E1–E7), tous sur la page 03.
- Les anciennes pages `04`, `05` et `06` (si elles existent d'un lancement précédent) sont supprimées automatiquement.

### Application web (`01_APP_WEB/Settalpay_High_Level.html`)
- Écran Impact & IA, panneau administrateur, historique, bouton flottant, notes Confidentialité / Anti-fraude et **messages éphémères (toasts)** sont maintenant traduits en Wolof et en English (avant, seuls certains écrans changeaient).
- La langue choisie est mémorisée et rétablie au rechargement.

## ⚠ À faire valider
Les traductions **Wolof** ont été rédigées dans le vocabulaire déjà utilisé par l'app (buteel, dépôt, paye, xibaar, istuwaar…). Elles doivent être relues par un locuteur natif avant toute présentation officielle (notamment les phrases longues : confidentialité, anti-fraude, FAQ).

## Limites connues
- Dans Figma, la barre de navigation et le bouton flottant des écrans « complets » (Impact, Aperçu admin) sont placés en bas de la page et défilent avec elle (Figma ne permet pas de les fixer par script). Pour les fixer : sélectionner la barre → cocher « Fix position when scrolling ».
- Le lancement / onboarding existe dans les 3 langues, mais on change de langue depuis Paramètres (comme dans l'app web), pas depuis le lancement.
- Le fichier contient maintenant 4 pages : `00 COVER`, `01 DESIGN SYSTEM`, `02 COMPONENTS`, `03 MOBILE APP`.
- Les pages `00 COVER`, `01 DESIGN SYSTEM` et `02 COMPONENTS` restent en français (documentation de la charte).

## Rappel V2.4 (inchangé)
Prototype cliquable (mode présentation ▶) avec animations Smart Animate du scanner (écrans « 09 / 09b ») et de l'analyse IA (« 12a » à « 12d »), mode sombre corrigé (fond #06150A · surfaces #0D2114 / #12351F · texte #F3F7F2 · vert d'action #3D8652 · jaune #F3B706 réservé aux valeurs), logo PNG + logo vectoriel de secours.
