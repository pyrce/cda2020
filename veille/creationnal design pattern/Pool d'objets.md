## Pool d'objets

Utilise un ensemble d'objet initialisé prêt a être réutilisé, plutôt que de les créer et les détruire. Un client demande un objet au pool et effectue des opérations sur l'objet. Une fois fini l'objet retourne dans le pool d'objets. Dans certain cas, ce pattern améliore les performences.

Lors de sa création, le développeur doit s'assure que l'objet retourne dans le bon état pour la prochaine utilisation, auxuelle cas il retourna une exeption.
