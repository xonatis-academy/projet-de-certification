# 1. Qu'est-ce que les methodes agiles ?
- règles
- mieux repondre aux besoins du client
- iteration
- communication

Les méthodes agiles sont comme des REGLES pour les développeurs et leur permettre de MIEUX REPONDRE AUX BESOINS DU CLIENT. Les méthodes agiles demandent de développer étapes par étapes (les étapes sont des ITERATIONS) et demandent d'améliorer la COMMUNICATION.

# 2. Avez-vous un exemple de methodes agiles ?
- scrum
- sprint 
- retrospective

Un exemple de methodes agiles est le SCRUM. Les itérations sont appelées les SPRINT. A la fin de chaque SPRINT, l'équipe fait une réunion. Cette réunion à la fin de chaque SPRINT est appelée une RETROSPECTIVE.

# 1. Qu'est-ce que l'HTML ?
- structure du site
- sans couleur

L'HTML est un langage permettant de décrire la structure du site. Il décrit ou se situent les textes et les images, mais il ne décrit pas les couleurs.

```
<div>
    <img src="https://site.com/img.jpg" />
</div>
```

# 1. Qu'est-ce que le CSS ?
- langage
- feuille de style
- aspect visuel

Le CSS est un LANGAGE pour développer des fichiers .css appelés FEUILLES DE STYLE. On a besoin du CSS pour ajouter des couleurs au site internet et controler son ASPECT VISUEL.

# 2. Comment écrit-on du CSS ?
- classe
- propriété
- valeur

On écrit du CSS en déclarant, la plus part du temps, des CLASSES avec des PROPRIETES et des VALEURS pour chaque PROPRIETE.
Par exemple, pour colorier une div en rouge on écrit :

```
.ma-classe-rouge {
    background-color: red;
}
```

Ici la classe est `ma-classe-rouge` et une propriété est `background-color` et la valeur de cette propriété est `red`.

On peut ensuite l'utiliser dans le HTML.

# 3. Comment utilise-t-on une classe CSS en HTML ?
- attribut
- class

Une fois que l'on a développé la classe en CSS, pour la lier à un élément dans le HTML avec l'ATTRIBUT CLASS

```
<div class="ma-classe-rouge"></div>
```

# 1. Qu'est-ce que l'injection de dépendance ?
- Mise a disposition automatique

L'injection de dépendance permet d'utiliser des composants/objets facilement. Dans le cas de Symfony, il suffit de lui dire ce dont on a besoin dans les paramètres dans la fonction et Symfony nous le donne. L'injection de dépendance est une MISE A DISPOSITION AUTOMATIQUE des objets.

# 2. Comment PHP peut-il se souvenir du visiteur du site ?
- session
- cookie

PHP peut se souvenir du visiteur par 2 méthodes : la SESSION ou les COOKIES.
La SESSION contient les informations du visiteurs et est stocké sur le serveur. Les COOKIES contiennent les informations du visiteurs et sont stockés sur l'ordinateur du visiteur.

# 3. Qu'est-ce que la session ?
- souvenirs du visiteur stockés sur le serveur

On utilise la session pour stocker les informations du visiteur. La session stocke les informations sur le serveur, donc c'est sécurisé. La session contient donc les SOUVENIRS DU VISITEUR SUR LE SERVEUR. En PHP, la session est accessible par la variable $_SESSION.

# 4. Qu'est-ce que les cookies ?
- souvenirs du visiteur stockés sur l'ordinateur du visiteur

On utilise les cookies pour stocker les informations du visiteur. Les cookies stockent les informations sur l'ordinateur du visiteur, donc ce n'est PAS sécurisé. Les cookies contiennent donc les SOUVENIRS DU VISITEUR SUR L'ORDINATEUR DU VISITEUR. En PHP, la session est accessible par la variable $_COOKIE.
