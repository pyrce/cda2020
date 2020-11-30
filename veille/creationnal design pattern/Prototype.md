# Prototype

C'est utilisé quand l'objet est déterminé pas une instance prototipal, qui est cloné pour créer des objet

- Evite les sous classes dans le code client de l'application
- Evite le cout de création de l'objet 

Pour l'utiliser, créer une classe abstraite qui a une methoded clone() virtuelle

résout les problèmes:

- Comment on créer des objets spécifiques à l'execution ?
- Comment les classes dynamiques peuvent être instancié ?
