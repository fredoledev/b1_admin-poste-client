# B1 — Administration Poste Client

## Examen
### Mission 1

On commence par utiliser `pwd` pour savoir où on est.

Ensuite on va utiliser la commande `ls` pour savoir dans quel dossier aller, et utiliser `cd` pour aller à l'emplacement désiré.
On réutilise `ls`et `cd` jusqu'à ce que l'on soit à destination.

![Capture d'écran de la mission 1 terminée](/Exam/Screen1.png)

### Mission 2

On utilise la commande `cd ..` 4x car le dossier cible se trouve 4 niveaux au-dessus dans l’arborescence (chaque `cd ..` permet de remonter d’un niveau vers le dossier parent...).

Ensuite on utilise `pwd` pour être sûr que l'on est retourné dans le bon dossier.

Enfin on réutilise `ls` et `cd` comme sur la mission précédente pour aller au dossier souhaité.

![Capture d'écran de la mission 2 terminée](/Exam/Screen2.png)

### Mission 3

On utilise la commande `cd` pour retourner au dossier de départ du jeu (comme indiqué).

Pour se rendre directement à la salle du trône on va également utiliser la commande `cd` en spécifiant le chemin d'accès complet depuis le dossier de départ.

![Capture d'écran de la mission 3 terminée](/Exam/Screen3.png)

### Mission 4

Comme au début de la précédente mission, on utilise la commande `cd` pour retourner au dossier de départ. On l'utilise également pour se rendre dans le dossier de la forêt.

On utilise la commande `mkdir` pour créer un dossier "Hut". On se rend dans ce dossier avec `cd` et on réutilise `mkdir` pour créer le fossier "Chest".

![Capture d'écran de la mission 4 terminée](/Exam/Screen4.png)

### Mission 5

Comme toujours on utilise `cd` pour retourner au dossier de départ puis au le dossier dans lequel nous allons faire des modifications.

On utilise la commande `rm` pour se débarrasser de toutes les araignées (on met le nom de chaque fichier à supprimer, en les séparant à chaque fois avec un espace, pour pouvoir tous les effacer en une seule commande.)

![Capture d'écran de la mission 5 terminée](/Exam/Screen5.png)

### Mission 6

On utilise `cd` une seule fois pour aller directement au dossier souhaité depuis le dossier de départ (simbolisé par le signe `~`).

On utilise ensuite la commande `mv` pour déplacer les trois pièces du dossier actuel vers le dossier souhaité (on indique donc les noms des trois fichiers séparés par des espaces, et le chemin du dossier de destination).

![Capture d'écran de la mission 6 terminée](/Exam/Screen6.png)

### Mission 7

On utilise `ls -A` pour afficher les pièces cachées.

On réutilise ensuite la même commande `mv` que la mission précédente pour les déplacer vers notre coffre (on utilise la touche Tab de notre clavier après avoir commencé à taper le nom d'une pièce pour qu'il s'auto-complète, afin d'aller plus vite).

![Capture d'écran de la mission 7 terminée](/Exam/Screen7.png)

### Mission 8

On réutilise `cd` de la même manière que pour la mission 6.

On utilise `rm *spider*` pour supprimer tout les fichiers contenant le mot `spider`.

![Capture d'écran de la mission 8 terminée](/Exam/Screen8.png)

### Mission 9

On refait la même chose que pour la précédente mission, en ajoutant un point avant `*spider*` pour que la wildcard trouve les fichiers cachés.

![Capture d'écran de la mission 9 terminée](/Exam/Screen9.png)

### Mission 10

On utilise `cd` pour aller dans le hall principal.

On utilise ensuite la commande `cp` de la même manière que `mv` pour *copier* les standards dans notre coffre.

![Capture d'écran de la mission 10 terminée](/Exam/Screen10.png)

### Mission 11

On réutilise la commande `cp` pour copier les tapisseries dans le coffre, en réutilisant les wildcards de la même manière que pour la mission 8.

![Capture d'écran de la mission 11 terminée](/Exam/Screen11.png)

### Mission 12

On utilise `cd` pour aller au premier étage.

On utilise ensuite `ls -l` pour lister les peintures avec les détails liés, notamment leur ancienneté.

`painting_fuGYyXDv` étant la peinture la plus ancienne, on utilise `cat` pour en contempler le contenu et on réutilise `cp` pour le copier dans le coffre.

![Capture d'écran de la mission 12 terminée](/Exam/Screen12.png)

### Mission 13

On utilise `cal 2028` pour afficher le calendrier pour l'année 2028. 

On peut voir que le 23 juillet 2028 sera un dimanche.

![Capture d'écran de la mission 13 terminée](/Exam/Screen13.png)

### Mission 14

On utilise la commande `alias` pour en quelque sorte créer un raccourci : désormais, au lieu de taper `ls -A`, il suffira de taper `la`.

![Capture d'écran de la mission 14 terminée](/Exam/Screen14.png)

### Mission 15

On utilise `cd` pour aller dans notre coffre, et on utilise la commande `nano` suivi du nom du fichier à créer. On écrit juste du texte dedans, on enregistre et on quitte...

![Capture d'écran de la mission 15 terminée](/Exam/Screen15.png)

### Mission 16

On réutilise la commande `alias` de la même manière que pendant la mission 14, pour aller éditer notre fichier journal dans notre coffre en tapant simplement `journal`...

![Capture d'écran de la mission 16 terminée](/Exam/Screen16.png)

### Mission 17

On utilise `cd` pour se rendre dans le domaine de la reine (on utilise tab après avoir tapé `.L` pour gagner du temps en autocomplétant le nom).

On utilise `rm` pour supprimer la reine : on utilise 2xTab pour afficher la liste des fichiers, on commence à taper le nom du fichier de la reine et on appuie sur Tab pour autocompléter son nom et finir de la supprimer.

![Capture d'écran de la mission 17 terminée](/Exam/Screen17-18.png)

### Mission 18 (CANCELLED)

### Mission 19

On exécute les trois `flarigo` en même temps que `gsh check` (en mettant `&` entre chaque commande) de sorte à ce que le pyrotechnicien voie les feux d'artifice...

![Capture d'écran de la mission 19 terminée](/Exam/Screen19.png)

### Mission 20

On essaie la commande `charmiglio` avec différentes combinaisons de lettres jusqu'à trouver la bonne... (si c'est la mauvaise on interrompt avec Control-C)

![Capture d'écran de la mission 20 terminée](/Exam/Screen20.png)

### Mission 21

On utilise `cd` pour aller au dossier de la pièce de cuivre et on le déplace dans le coffre avec `mv`...

![Capture d'écran de la mission 21 terminée](/Exam/Screen21.png)

### Mission 22

On utilise la commande `tree` pour afficher l'arborescence à partir du dossier actuel, et on parcourt cette arborescence pour trouver la pièce d'argent...

On se rend ensuite dans le dossier de la pièce avec `cd` et on déplace le fichier dans notre coffre avec `mv`...

![Capture d'écran de la mission 22 terminée](/Exam/Screen22.png)

### Mission 23

On utilise la commande `find` (avec l'argument `-iname` pour rendre la recherche insensible à la casse) pour chercher et trouver, dans le dossier actuel et tous ses sous dossiers, toutes les occurrences de `*gold*` (entre astérisques pour inclure les fichiers qui contiennent autre chose que juste "gold").

Maintenant que les deux chemins des deux pièces sont indiqués, il suffit de s'y rendre (`cd`) pour les déplacer dans notre coffre (`mv`)...

![Capture d'écran de la mission 23 terminée](/Exam/Screen23.png)

### Mission 24

On commence par regarder avec la commande `cat` le sommaire du grimoire. On voit que la recette qu'il nous faut est page 7. On réutilise la même commande pour regarder la page 7 : on remarque que la recette avec le titre sont uniquement sur les 6 premières lignes.

*Dans le dossier "cave" (avec le sorcier)* on utilise donc la commande `head` pour lire les 6 premières lignes (la recette avec le titre, et rien d'autre)...

![Capture d'écran de la mission 24 terminée](/Exam/Screen24.png)

### Mission 25

On réutilise `cat` pour retourner sur le sommaire du grimoire : la recette de la soupe est page 12.
On utilise à nouveau la même commande pour regarder le contenu de la page 12 : il nous faut uniquement les 9 dernières lignes (la recette *sans* le titre)...

Toujours dans le dossier "cave" on utilise cette fois-ci la commande `tail` pour lire les 9 dernières lignes (la recette sans le titre)...

![Capture d'écran de la mission 25 terminée](/Exam/Screen25.png)