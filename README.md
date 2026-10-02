# Panelbuild

Création d'un panneau d'affichage LED : passage d'une matrice WS2812 8×32 (pas de 10 mm)
à un écran HUB75 128×128 au pas de 2,5 mm, piloté par un ESP32-S3-N16R8, avec un cadre
imprimé sur une Bambu Lab P2S.

## Site du projet

Ouvre [`docs/index.html`](docs/index.html) dans un navigateur. Pour le publier avec
GitHub Pages, choisis la source « branche principale, dossier `/docs` ».

Le site contient :

- une simulation animée des panneaux et une comparaison avant/après à l'échelle ;
- le choix des panneaux (P2, P2.5, P3…) et les puces compatibles avec l'ESP32 ;
- trois configurations (256×64, 128×128, 256×128) avec leur budget ;
- une liste de matériel interactive avec les prix relevés le 2 octobre 2026 ;
- le schéma de câblage en serpentin 2×2 et le brochage pour l'ESP32-S3-N16R8 ;
- le dimensionnement de l'alimentation ;
- le cadre imprimé en 4 quarts, le diffuseur et la grille de pixels ;
- les options logicielles (WLED, Arduino, ESPHome) et les pièges à éviter.

## Configuration recommandée

| | |
|---|---|
| Panneaux | 4× P2.5 64×64 HUB75E, scan 1/32, puce compatible (ICN2037, FM6126A…) |
| Résolution | 128×128 = 16 384 pixels, 320×320 mm |
| Contrôleur | ESP32-S3-N16R8 (déjà en stock) |
| Alimentation | 5 V ≥ 20 A (Mean Well LRS-150F-5) |
| Logiciel | WLED 16.0.1+, binaire `ESP32-S3_16MB_opi_HUB75.bin` |
| Budget | ≈ 160 € hors ESP32 et alimentation |
