# tp2_EDW2

# tp2_EDW2

## Liste des commandes Git utiles:

[source](https://www.le-fab-lab.com/git-depot-distant.html)

### Cloner un dépôt distant :

`git clone url_du_depot_distant dossier_local`

-   dossier_local est facultatif mais utile si vous souhaitez spécifier le nom du dossier dans lequel le projet cloné sera récupéré.

-   Par défaut il aura le même nom que sur le dépôt distant.
-   L'url du dépôt distant peut être une adresse http(s)://... mais aussi git.// , ssh ou encore ftp.
-   Suivant les cas des identifiants devront être fournis.

#### Afficher les dépôts distants enregistrés

`git remote`

-   En ajoutant l'option -v, les url distantes seront indiquées.

#### Ajouter un dépôt distant à prendre en compte pour votre projet :

` git remote add nom_local_du_dépôt_distant url`

-   Le nom_local... saisi vous permettra ensuite de faire référence plus facilement au dépôt.
-   Un dépôt cloné aura automatiquement le nom origin.

#### Supprimer la référence à un dépôt distant :

`git remote rm nom_local_du_dépôt_distant`

#### Obtenir des informations sur un dépôt distant

` git remote show nom_local_du_dépôt_distant`

#### Rafraîchir les données d'un dépôt distant (synchronisation)

` git fetch nom_local_du_dépôt_distant`

#### Rafraîchir les données de tous les dépôts distants

`git remote update`

-   Avec l'option --prune les branches disparues sur le dépôt distant sont aussi supprimées localement.

#### Récupérer et fusionner la branche principale (master) du dépôt distant avec celle créée localement lors d'un clonage

`git pull`

#### Pour récupérer le contenu d'une nouvelle branche distante :

-   Soit fusionner avec la branche locale sur laquelle on travaille :

`git merge nom_local_du_dépôt_distant/nouvelle_branche`

##### Ou créer une branche locale basée sur le contenu de la branche distante

`git checkout -b nouvelle_branche_locale nom_local_du_dépôt_distant/nouvelle_branche`

La nouvelle branche ainsi créée est une branche de suivi sur laquelle on peut lancer les commandes git push et git pull.

#### Comparer une branche distante et une branche locale

`git log nom_local_du_dépôt_distant/nom_branche_distante ^nom_branche_locale`

#### Comparer la branche actuelle avec une branche distante
