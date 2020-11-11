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
