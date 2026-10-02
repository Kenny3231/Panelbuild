# Panelbuild

Création d'un panneau d'affichage LED : passage d'une matrice WS2812 8×32 (pas de 10 mm)
à un écran HUB75 128×64 (4 panneaux 64×32 au pas de 2,5 mm), piloté par un ESP32-S3-N16R8,
avec un cadre imprimé sur une Bambu Lab P2S.

## Site du projet

Ouvre [`docs/index.html`](docs/index.html) dans un navigateur, ou publie-le avec GitHub Pages.

### Activer GitHub Pages

1. Le dépôt doit être **public**. Avec un compte GitHub gratuit, Pages ne fonctionne pas sur
   un dépôt privé. Pour le rendre public : Settings → General → Danger Zone →
   Change visibility.
2. Settings → Pages → Build and deployment → Source : **Deploy from a branch**.
3. Branche : `claude/led-panel-esp32-upgrade-u7gdrj` (ou `main` après fusion), dossier
   **`/docs`**, puis Save.
4. Après une à deux minutes, le site est en ligne sur
   `https://kenny3231.github.io/Panelbuild/`.

Le site contient :

- une simulation animée des panneaux et une comparaison avant/après à l'échelle ;
- le choix des panneaux (P2, P2.5, P3…) et les puces compatibles avec l'ESP32 ;
- les références de panneaux 64×32 (Waveshare, Adafruit, AliExpress) ;
- trois configurations (128×32, 128×64 au pas de 2,5 mm, 128×64 au pas de 4 mm) avec leur budget ;
- les alimentations conseillées (Mean Well GST60A05, LRS-50/100/150F/200-5) ;
- une liste de matériel interactive avec les prix relevés le 2 octobre 2026 ;
- le schéma de câblage en serpentin 2×2 et le brochage pour l'ESP32-S3-N16R8 ;
- le cadre imprimé en 2 moitiés, le diffuseur et la grille de pixels ;
- les options logicielles (WLED, Arduino, ESPHome) et les pièges à éviter.

## Configuration recommandée

| | |
|---|---|
| Panneaux | 4× P2.5 64×32 HUB75 indoor, scan 1/16 (Muen sur AliExpress ou Waveshare RGB-Matrix-P2.5-64x32) |
| Résolution | 128×64 = 8 192 pixels, 320×160 mm |
| Contrôleur | ESP32-S3-N16R8 (déjà en stock) |
| Alimentation | Mean Well LRS-100-5 (5 V 18 A) |
| Logiciel | WLED 16.0.1+, binaire `ESP32-S3_16MB_opi_HUB75.bin` |
| Budget | ≈ 155 € avec l'alimentation, hors ESP32 |
