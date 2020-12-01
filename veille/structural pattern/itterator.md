# Description

Un iterateur parcours un conteneur et a acces a ses élements. Il découple les algorithmes du container, dans certain cas ils nes peuvent pas être découpler

Résouds les problèmes:

- Les élements d'un objet agregat doivent être parcourus sans exposer sa représentation

- Les nouvelles opérations de traversée doit être définie pour une agraggat d'objet sans changer son interface

Description de la solutions:

- Définir un objet séparer qui encapsule l'acces et la traversé d'un arggregat d'objet

- Les clients utilise un iterateur  pour acceder et traverser un aggregat sans connaitre sa représentation