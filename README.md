# B1 — Administration Poste Client

## Exercices
### Exercice Débutant n°2

1. ***Créer un fichier log.txt qui contient la liste des fichiers de /etc***

        cd /etc
    On va au dossier `etc`, à la racine du système.

        touch log.txt
    On crée un fichier (ici `log.txt`) dans le dossier actuel.
    
        ls > log.txt
    On liste (`ls`) les fichiers du dossier actuel — et on *transfère* directement cette liste (`>`) dans le fichier `log.txt`.

    ![Capture d'écran de l'étape 1](/Exercices/Débutant02/Screen1.png)

2. ***Ajoute dans ce fichier les 10 dernières lignes du fichier /var/log/syslog***

        tail /var/log/syslog >> log.txt
    On utilise `tail` pour afficher les dernières lignes (10 par défaut) du fichier `syslog` dans le dossier `/var/log` — et on *ajoute* directement cette liste (`>>`) dans le fichier `log.txt`, toujours dans le dossier `/etc` (comme on n'a pas changé de dossier avec `cd`).

    ![Capture d'écran de l'étape 2](/Exercices/Débutant02/Screen2.png)

3. ***Affichez moi seulement les lignes qui contiennent le mot « error »***

        grep 'error' log.txt
    On utilise `grep` pour rechercher les occurrences d'un mot (ici `error`) dans un fichier (ici notre `log.txt`). Toutefois, le hasard a voulu que notre log ne contienne pas d'erreurs. Nous allons donc, pour l'exemple exécuter...

        grep 'error' /var/log/syslog
    ...cette commande qui nous a affiché toutes les occurrences du mot `error` dans notre `syslog``

    ![Capture d'écran de l'étape 3](/Exercices/Débutant02/Screen3.png)
    
    > On aurait pu utiliser l'argument `-i` de `grep` pour avoir toutes les occurrences de tous les affichages du mot `error` (ex. `Error`)...

---

### Exercice Débutant n°3

1. ***Créer un fichier secret.txt dans ton répertoire***

        touch secret.txt
    On crée un fichier (ici `secret.txt`).

    ![Capture d'écran de l'étape 1](/Exercices/Débutant03/Screen1.png)

2. ***Change les permissions de ce répertoire pour qu’il soit accessible en lecture/écriture que pour le propriétaire***

        chmod 600 secret.txt
    On utilise la commande `chmod` pour modifier les permissions de notre fichier. `600` correspond aux permissions à attribuer : le premier chiffre donne les permissions de l'utilisateur actuel, le deuxième chiffre pour celles du groupe, et le troisième pour les autres.

    ![Capture d'écran de l'étape 2](/Exercices/Débutant03/Screen2.png)

3. ***Vérifie qu’un autre utilisateur ne peut pas voir son contenu***

        ls -alh secret.txt
    On utilise la commande `ls` (la même commande qui nous permet d'afficher le contenu d'un dossier) pour afficher les permissions de notre fichier.
    
    On voit `rw-` sur les premiers premiers caractères, ce qui signifie que l'on peut le lire et l'écrire (sans pouvoir l'exécuter !!). Sur les deux autres groupes de caractères on peut voir `---` et `---` ce qui signifie que les autres groupes et utilisateurs n'ont *aucun* accès au fichier.

    ![Capture d'écran de l'étape 3](/Exercices/Débutant03/Screen3.png)

----------
----------

### Exercice Intermédiaire n°1

1. ***Affichez la liste des processus et montrez-moi celui qui utilise le plus de ram***

        top
    On utilise cette commande pour afficher l'utilisation des ressources système, l'uptime, les tâches en cours d'exécution... un vrai gestionnaire de tâches en CLI.
    
    Pour afficher le processus qui utilise le plus de mémoire RAM, il faut trier les processus par utilisation de mémoire, on appuie donc sur la touche `M` (majuscule).
    
    Ainsi, on voit ici que le processus le plus gourmand en mémoire est `gnome-shell` (PID n°`1971`), avec 4,4% de consommation de mémoire.

    ![Capture d'écran de l'étape 1](/Exercices/Intermédiaire01/Screen1.png)

2. ***Utilisez la commande "nice" pour modifier la priorité d'un processus***

        renice -n 20 --pid 3304
    La commande `nice` sert à *lancer* un processus avec priorité. Ici on utilise la commande `renice` pour *modifier* la priorité d'un processus.

    On utilise le premier argument `-n` pour spécifier la priorité à donner au processus. Il s'agit d'une valeur entre `-20` et `20` :
    - `-20` correspond à la priorité la plus haute ;
    - `20`correspond à la priorité la plus basse ;
    - `0` correspond donc à la priorité de base...

    On utilise le deuxième argument `--pid` (ou `-p`) pour spécifier le processus sur lequel appliquer la priorité grâce à son PID.

    Ici, on applique la priorité la plus basse possible au processus possédant le PID `3304` (il s'agit ici de `firefox`, on le sait après l'avoir identifié grâce à la commande `top` utilisée précédemment).

    ![Capture d'écran de l'étape 2](/Exercices/Intermédiaire01/Screen2.png)

3. ***Terminez un processus grâce à son PID***

        kill 3304
    Enfin, on utilise la commande `kill` pour terminer, arrêter un processus. À la suite il suffit de taper le PID du processus (on reprend le PID `3304` qui correspond toujours à `firefox`, ouvert dans la VM). 
    
    Après exécution de la commande, l'application s'est fermée.

    ![Capture d'écran de l'étape 2](/Exercices/Intermédiaire01/Screen3.png)

---

### Exercice Intermédiaire n°2

1. ***Créer un script bash qui sauvegarde automatiquement le contenu de /home/user/Documents dans /home/user/backups***

        nano ~/backup.sh
    On commence par ouvrir dans l'éditeur de texte un nouveau fichier script (`.sh`) dans le dossier de départ de l'utilisateur (avec la commande `nano`). Le fichier sera créé à l'enregistrement.

    ![Capture d'écran de l'étape 1](/Exercices/Intermédiaire02/Screen1.png)
    Ensuite on inscrit ensuite les commandes suivantes dans le script.

        chmod +x ~/backup.sh
        bash ~/backup.sh
    Enfin, on rend le script exécutable, et on teste directement le script.

    ![2e capture d'écran de l'étape 1](/Exercices/Intermédiaire02/Screen1-1.png)

2. ***Exécute ce script tous les jours à 2h***

        crontab -e
    On modifie la crontab (le planificateur de tâches) de notre utilisateur, en y ajoutant ceci : `0 2 * * * /home/user/backup.sh`.
    
    Ici on indique l'heure d'exécution du scipt (tous les jours, 2h), et on spécifie le fichier.

        crontab -l
    On vérifie ici que la tâche est bien enregistrée.

    ![Capture d'écran de l'étape 2](/Exercices/Intermédiaire02/Screen2.png)

    Nous avons maintenant un script bash qui sauvegardera tous les jours à 2h le contenu du dossier Documents dans le dossier Backups.

---

### Exercice Intermédiaire n°3

1. ***Affiche les logs du service ssh sur les 24 dernières heures***

        sudo journalctl -u ssh --since "24 hours ago"
    On utilise la commande `grep` pour rechercher toutes les occurrences du mot `sshd` (processus en charge des opérations SSH) dans le fichier log concerné.

    ![Capture d'écran de l'étape 1](/Exercices/Intermédiaire03/Screen1.png)

2. ***Filtre les logs pour avoir que les connexions ratées***



3. ***Sauvegarde tout dans un fichier sshd_failed_logins.txt***

