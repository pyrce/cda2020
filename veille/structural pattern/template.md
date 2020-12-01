# Definition

C'est une méthode dans une super classe qui défini le squelette d'une opération en terme d'étapes haut niveau. Ces étapes sont implémenté par des méthode d'aides dans la même classe.
Ce pattern a pour but de définir la structure global d'une opération tout en permettant aux sous classes de rafiner ou redefinir les méthodes.

Cette technique, très répandue dans les classes abstraites, permet de :

- fixer clairement des comportements standards qui devraient être partagés par toutes les sous-classes, même lorsque le détail des sous-opérations diffère ;
- factoriser du code qui serait redondant s'il se trouvait répété dans chaque sous-classe.

Avantages:

- Laisse les sous classe implémenter différents comportement

- Evite la duplicaton de code: le workflow géneral est dans las classe abstraite

- Controlle la spécialisation est permise.