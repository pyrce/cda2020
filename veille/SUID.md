# SUID

UNIX, “papa” de linux, a été conçu dès le départ comme un système d'exploitation multi-utilisateurs, et pas seulement multi-tâches. Il a donc fallu penser à protéger les fichiers de chaque utilisateur ainsi que ceux du système pour, par exemple, en empécher la lecture, la modification ou la destruction par les utilisateurs non autorisés

Example de droit:

- Droit d'ecriture sur un fichier sur lequel je n'ai aucun droit d'écriture
- Changer le proprietaire d'un fichier
- la copie d'un fichier conserve t'il les droits
- Copie de fichier n'importe où

Les droits concernent:

- les fichiers
- les répertoires
- les liens symboliques
- les péripheriques

Ils possèdent les droits suivant : lecture , ecriture, execution, droits spéciaux. Cela concerne, le proproetaire, son groupe utilisateur et les autres. A noté qu'il existe des droits avancés : les ACL.

Sur les fichiers les droits sont noté soit par des lettres (r,w,x) soit par des chiffres (0 à 7)

Les utilisateurs normaux ont un SUID >100 >60000. Les utilisaterus système ont SUID >1000, 0 etant celui de root.

Example: 

```bash
drwxr-xr-x 2 ludovic users 4096 avr 24 19:10 theme actuel gnome
-rw-r–r– 1 ludovic users 11518 jui 19 01:58 tuxdetourer.png
```