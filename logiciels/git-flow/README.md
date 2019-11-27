# Cheatsheet Git-Flow

Git-flow est un ensemble d'extensions git permettant des opérations complexe de manière simplifié sur un dépôt afin d'appliquer le modèle de branches de Vincent Driessen.

**_Cet aide-mémoire montre l'utilisation et les effets des opérations Git-flow_**

## Initialisation

_Git-flow doit être initialisé (comme git) afin de personnaliser la configuration de notre projet._

Afin de commencez à l'utiliser, il faut l'initialiser dans un dépôt git existant avec la commande suivante :

`git flow init`

Il faudra alors répondre à quelques questions concernant les conventions de nommage pour nos branches.

**_Il est recommandé d'utiliser les valeurs par défaut !_**

## Fonctionnalités (Features)

* Développe des nouvelles fonctionnalités pour notre prochaine version
* Existe généralement uniquement dans les dépôts des développeurs

### Commencer une fonctionnalité

_Le développement d'une fonctionnalité commence à partir de la branche 'develop'_

On la démarre donc avec la commande :

`git flow feature start MYFEATURE`

Cette commande crée une nouvelle branche de fonctionnalité basée sur `develop` et fait un switch automatique sur la nouvelle branche.

### Terminer une fonctionnalité

_Terminer le développement d'une fonctionnalité effectue les opérations suivantes :_

* Fusionne `MYFEATURE` dans `develop`
* Supprime la branche `MYFEATURE`
* Switch sur la branche `develop`

La commande est :

`git flow feature finish MYFEATURE`

### Publier une fonctionnalité

Si jamais vous développez une fonctionnalité en collaboration alors publiez la sur le serveur distant afin qu'elle puisse être utilisée par d'autres utilisaeurs grâce à la commande suivante :

`git flow feature publish MYFEATURE`

