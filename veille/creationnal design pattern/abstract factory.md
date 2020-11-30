# Abstarct factory

Permet l'encapsualtion d'un group de factory qui on un theme commun sans préciser la classe. Ce patterne sépare l'implémentation de l'objet de son utilisation générale.

### Probleme 

- Comment une application est indépédante de comment les objets sont crées ?

- Comment une classe est indépendante des objets requis sont crées ?

- Comment créer une famille d'objet dépandant ou liés ?

### utilisation

l'abstract factory ne retournant qu'un pointeur abstrait, le code client ne connait pas et n'ai pas géné par le type de l'objet créé. En revanche, le type de l'objet est défini dans la factory (par exemple, dans un fichier). Le code client ne traite qu'avec le type abstrait.
