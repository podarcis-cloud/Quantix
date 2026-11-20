# QUANTIX — ÉTAT R462 (20 nov. 2026) — complète ETAT-R460.md
Dernier build poussé : **R462** (commit f934d52, main). Tampon : `grep -o 'build R[0-9]*' index.html`.

## R461
« Recommencer » après le final : révèle Fluides et ouvre la constellation (animation d'éveil de la 12ᵉ étoile) au lieu du niveau 1.

## R462 · évasion des créatures de Fluides
- Nouveau `assets/js/qxcrea.js` (223 Ko, chargé à la demande par engine.js à l'ouverture de la constellation quand Fluides est révélé).
- Séquence ~32 s sur la vraie constellation : la bulle Fluides est percée, 8 créatures sortent une ou deux à la fois, longent les liens, entrent dans les bulles des mondes et les colonisent (poussière d'étoiles, membranes, compteur « Colonisés n/11 », bouton « Passer »). Joue une fois ; sauvegarde `crea:1` ; ensuite état final léger (lueur cyan, petite créature par bulle).
- Coupe-circuit : localStorage `qxcrea`='0'. Qualité adaptative (>8 ms/image), reduced-motion = version abrégée.
- Correctif : la mémoire `qxconst_vu` est complétée à 12 mondes (la 12ᵉ étoile ne s'éveillait pas sur vraie sauvegarde).
- Vérifié Chromium 390×844 : scénario complet, rechargement, Passer, coupe-circuit, migration, non-régression (niveau 1, monde 6, 12/12 solutions Fluides). Non testé : iPhone réel, anglais à l'écran, onglet caché.

## Pool de créatures (artefacts, non intégrés au jeu)
Étage 1 Cellule, Filament · Étage 2 Systole, Culbute, Chœur · Étage 3 Cortège, Volte, Braise. Banc v5 : https://claude.ai/artifact/JNfbmQUXH2TZLLZ5E6s83f · Évasion v4 : https://claude.ai/artifact/TZfNBUnJUq96CQBWhPgNic · Index des artefacts : https://claude.ai/artifact/QWvFteZ12oeyPdVBZrCHxJ
Monde parallèle : actions des créatures sur la particule (dévier, retarder, recracher, handicaps, aides) validées dans le principe ; prochain pas = mode « physique » dans le banc.

## JOURNAL (à ajouter)
- 2026-11-20 R461 : Recommencer → constellation avec révélation.
- 2026-11-20 R462 : évasion des créatures sur la constellation (qxcrea.js), état final colonisé ; Chromium OK, iPhone non testé ; poussé f934d52.
