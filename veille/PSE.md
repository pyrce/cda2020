# CVE-2021-22908

Buffer Overflow dans les profils de ressources de fichiers Windows dans 9.X permet à un utilisateur distant authentifié avec des privilèges de parcourir les partages SMB pour exécuter du code arbitraire en tant qu'utilisateur root. Depuis la version 9.1R3, cette autorisation n'est pas activée par défault.

## Technique

Le fonctionnement général d'un buffer overflow est de faire crasher un programme en écrivant dans un buffer plus de données qu'il ne peut en contenir (un buffer est un zone mémoire temporaire utilisée par une application), dans le but d'écraser des parties du code de l'application et d'injecter des données utiles pour exploiter le crash de l'application.

## Vulagrisation

le dépassement de mémoire permet  d'exécuter du code arbitraire sur la machine où tourne l'application vulnérable.
L'intérêt de ce type d'attaque est qu'il ne nécessite pas -le plus souvent- d'accès au système, ou dans le cas contraire, un accès restreint suffit.