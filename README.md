# VGA interactif

Une matière qui perçoit le geste au lieu de lui obéir.

Installation lumineuse low-tech : une carte FPGA DE0-Nano génère directement un signal VGA pour un projecteur, sans ordinateur. Seize points verts sur fond noir réagissent au geste du spectateur.

**Simulation en ligne :** https://niallscaife0.github.io/Interaction/

## La simulation

Modèle logiciel de l'installation, avec le même cadre que le matériel : image 640×480 à 60 Hz, 16 points, calculs en entiers (virgule fixe), sans fonction trigonométrique dans la boucle. Le code est écrit pour se traduire en C (microcontrôleur) et en VHDL (FPGA).

- **Vue spectateur** : quatre comportements (Repos, Trouble, Envol, Présence) et un pavé à deux axes, calme ↔ vif et épars ↔ uni.
- **Vue atelier** : réglages détaillés, décisions figées, boutons KEY0/KEY1, lecture des registres et débit du bus. Lien direct : [ouvrir l'atelier](https://niallscaife0.github.io/Interaction/#atelier).

## Matériel

- Carte Terasic DE0-Nano (FPGA Cyclone IV), programmée en VHDL sous Quartus
- Sortie VGA par les GPIO et une interface résistive
- Projecteur Epson EB-S11

## Contenu du dépôt

| Fichier | Rôle |
|---|---|
| `index.html` | Simulation interactive (page autonome, sans dépendance) |
| `README.md` | Cette présentation |

Projet mené dans le cadre du Master 1 en électronique à l'ISIB.
