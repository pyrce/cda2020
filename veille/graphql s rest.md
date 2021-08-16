# resupeme

## rest

L’élément central derrière REST est la ressource. Une API REST comprend un endpoint différent pour chaque ressource, 
avec des méthodes de requêtage HTTP différentes

GET /api/articles tous les articles

GET /api/articles/1 un article

post /api/articles insert un article

patch /api/articles/1 met a jours un article

delete /api/article/1 supprime un article

## Graphql

Comparé à REST, et son modèle très structuré basé sur les ressources, GraphQL apparait comme un langage de requête plus flexible, au-dessus d’une API.

GET /api?query={ article(id:"1") { title, content } }

Cette requête commande à l’API de lister un article ayant pour ID 1 et de retourner son titre et son contenu. Le même endpoint peut aussi être utilisé pour effectuer des actions au sein de l’API.

Celles-ci sont alors appelées mutations. Ce sont des méthodes pré-définies qui peuvent être appelées par le client

## GraphQL VS REST : le choix de GraphQL

 Dans notre exemple du blog, si vous souhaitez requêter un article  pour obtenir l’auteur, les tags et les commentaires, il vous faut au minimum 4 requêtes distinctes. Avec GraphQL, cela peut être effectué de façon plus programmatique, et permettre au client de requêter les seules informations souhaitées au fina

GraphQL est également un bon moyen pour minimiser les modifications liées à la montée de version – ce qui arrive quand les ressources et les schémas de données changent dans  une API REST

## GraphQL VS REST : le choix de REST

D’un autre côté, le plus gros avantage de REST sur GraphQL est la facilité avec laquelle les données peuvent être « cachées » et la transparence des actions effectuées sur l’API.
la requête est cohérente pour tous les clients