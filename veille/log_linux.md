# logs linux

La journalisation ( historique des événements) est un moyen que les systèmes d’exploitation utilise pour enregistrer toutes les actions d’un événement qui a eu lieu (exécution d’un processus, activité réseau etc ), permettant ainsi de localiser plus rapidement les défaillance d’un système.

Les fichiers sont les suivants:

-/var/log/secure

-/var/log/maillog

-/var/log/cron

-/var/log/boot.log

-/var/log/messages

/var/log/secure :

Syslog stocke dans le fichier de log « secure » tous les messages liée à la sécurité y compris ceux de l’authentification.

/var/log/maillog:
Syslog stocke les message liée au messagerie.

/var/log/cron :
Contient tous les message liée au démarrage du système.

-/var/log/boot.log :
Contient tous les message liée au démarrage du système.

/var/log/messages :
La plupart des messages log sont enregistré dans le fichier /var/log/messages, sauf les type de messages qu’on a vu précédemment.

## logrotate

Logrotate permet de limiter la taille des fichiers journaux présents dans /var/log.

Pour chaque fichier journal, logrotate réalise 2 opérations simultanées :

- la rotation : il archive le fichier journal sous un autre nom et supprime la plus ancienne archive
- la compression : il compresse éventuellement le fichier journal avant de l'archiver

Exemple :

```shell
-rw-r----- 1 syslog adm 45432 2011-09-24 10:12 /var/log/syslog
-rw-r----- 1 syslog adm 44442 2011-09-21 19:45 /var/log/syslog.1
-rw-r----- 1 syslog adm 31536 2011-09-19 21:04 /var/log/syslog.2.gz
-rw-r----- 1 syslog adm 72503 2011-09-18 15:45 /var/log/syslog.3.gz
-rw-r----- 1 syslog adm 21218 2011-09-17 09:45 /var/log/syslog.4.gz
-rw-r----- 1 syslog adm 10859 2011-09-16 18:28 /var/log/syslog.5.gz
-rw-r----- 1 syslog adm 74381 2011-09-07 23:15 /var/log/syslog.6.gz
```

Pour lire efficacement  :

- on peut n'afficher que la fin du fichier:

```shell
tail -20 /var/log/messages
```

Ou bien chercher avec grep :

```shell
grep -r "mail@malekal.com" /var/log/*
```

## Chercher au moins 1 trace de vos attaques grâce aux logs concernant l'activité 'blog

/var/log/apache2/access.log

```shell
127.0.0.1 - - [19/Aug/2021:06:01:43 +0000] "GET /wp-content/uploads/2021/08/qpJzZBgBWM-e1629352888578.jpg?/x HTTP/1.0" 200 3290 "-" "-"
127.0.0.1 - - [19/Aug/2021:06:01:43 +0000] "GET /wp-content/uploads/2021/08/qpJzZBgBWM-e1629352888578.jpg?/x HTTP/1.0" 200 3290 "-" "-"
```

brute force wpscan

```shell
10.6.84.233 - - [19/Aug/2021:07:41:47 +0000] "POST /xmlrpc.php HTTP/1.1" 200 420 "http://blog.thm" "WPScan v3.8.18 (https://wpscan.com/wordpress-security-scanner)"
10.6.84.233 - - [19/Aug/2021:07:41:47 +0000] "POST /xmlrpc.php HTTP/1.1" 200 420 "http://blog.thm" "WPScan v3.8.18 (https://wpscan.com/wordpress-security-scanner)"
10.6.84.233 - - [19/Aug/2021:07:41:48 +0000] "POST /xmlrpc.php HTTP/1.1" 200 420 "http://blog.thm" "WPScan v3.8.18 (https://wpscan.com/wordpress-security-scanner)"
```