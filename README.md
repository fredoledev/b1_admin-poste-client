# B1 — Administration Poste Client
## Exercices
### Exercice Débutant n°2

1. ***Créer un fichier log.txt qui contient la liste des fichiers de /etc***

*     cd /etc
    On va au dossier `etc`, à la racine du système.

*     touch log.txt
    On crée un fichier (ici `log.txt`) dans le dossier actuel.
    
*     ls > log.txt
    On liste (`ls`) les fichiers du dossier actuel — et on *transfère* directement cette liste (`>`) dans le fichier `log.txt`.

    ![Capture d'écran de l'étape 1](/Screen1.png)

2. ***Ajoute dans ce fichier les 10 dernières lignes du fichier /var/log/syslog***

*     tail /var/log/syslog >> log.txt
    On utilise `tail` pour afficher les dernières lignes (10 par défaut) du fichier `syslog` dans le dossier `/var/log` — et on *ajoute* directement cette liste (`>>`) dans le fichier `log.txt`, toujours dans le dossier `/etc` (comme on n'a pas changé de dossier avec `cd`).

    ![Capture d'écran de l'étape 2](/Screen2.png)

3. ***Affichez moi seulement les lignes qui contiennent le mot « error »***

*     grep 'error' log.txt
    On utilise `grep` pour rechercher les occurrences d'un mot (ici `error`) dans un fichier (ici notre `log.txt`). Toutefois, le hasard a voulu que notre log ne contienne pas d'erreurs. Nous allons donc, pour l'exemple exécuter...

*     grep 'error' /var/log/syslog
    ...cette commande qui nous a affiché toutes les occurrences du mot `error` dans notre `syslog``

    ![Capture d'écran de l'étape 3](/Screen3.png)
    
    > On aurait pu utiliser l'argument `-i` de `grep` pour avoir toutes les occurrences de tous les affichages du mot `error` (ex. `Error`)...
