# Builder

Sépare la création d'un objet complexe de sa représentation.

## Probleme 

- comment une classe peut créer divers représentation d'un objet complex ?

- Comment une class qui contient la création d'objet complexe peut être simplifié ?

## Processus


- Encapsule la création et l'assemblage d'objet complexe dans un constructeur différent.

- Une classe délègue la création d'un objet à un constructeur séparé plutôt que de créer l'objet directement.

Avantage

- Permet de faire varié la représentation inter d'un objet

- Encapsule le code pour la création et la représentation

- Donne le controle sur les étapes de la création

Inconveniants 

- Oblige la cration dun contructeur séparer pour chage type d'objet
- Oblige la mutabilité de la classe
- l'injection de dépendance est moins supporté