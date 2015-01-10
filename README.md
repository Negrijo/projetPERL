
# Projet perl 2014/2015 DA2I

## Binôme

- Vincent VISEUX
- David CHEVALLIER

## Résumé

Cochez (en mettant un X dans les [ ]) les fonctionnalités qui sont
implémentées dans votre projet.

  - [X] appel de commande (paramètres, détachement, etc)
  - [X] fichier de configuration
  - [X] gestion du port d'écoute
  - [X] vérification du format des requêtes HTTP/1.1 (RFC 7230, etc.)
  - [X] réponse toujours valide HTTP/1.1 (RFC 7230, etc.)
  - [X] code HTTP gérés
  - [X] type de fichiers respecté (html/png/texte)
  - [X] gestion des répertoires
  - [X] gestion de la page d'erreur
  - [X] gestion des logs
  - [X] gestion des clients en //
  - [ ] gestion du max de clients
  - [X] routes statiques
  - [X] routes statiques avec expression régulière
  - [ ] cgi statiques
  - [ ] cgi avec expression régulière
  - [ ] gestion des paramètres de cgi

Mettez ici la note que vous pensez mériter : 7

## Détail

Le serveur se lance et se stop proprement. Il affiche aussi son PID via la commande "status".
Il affiche partiellement les répertoires, c a d qu'il affiche bien l'arborescence du premier répertoire mais l'utilisateur ne peut pas se déplacer en cliquant sur les liens.
Il gère bien les erreurs pour ce que j'ai implementé (403, 404). Toutes les erreurs sont implémentées.
Il extrait bien les informations de configuration du fichier "comanche.conf".  
Il gère les types de fichiers demandés (html, png et texte). (Il parle HTTP).
Il ne gère pas le nombre de client demandé mais il en traite une infinité.
La gestion des logs est partielle puisque il ne prend en compte que les evenement "start".
Le serveur ne traite pas les CGI.

# Développement

## Implémentation

Le plus important a été la lecture du fichier de configuration puisque c'est grâce à lui que le serveur peut se lancer.
Comme le client le souhaite. Il est aussi important de pouvoir lancer le serveur proprement et de l'arrêter de la même
manière. Cela implique de bien stocker le pid du serveur dans un fichier texte.
Ensuite il faut bien répondre au client, parler HTTP et lui renvoyer la page HTML qu'il attend. (Si c'est une image, un texte ou 
du HTML ou même un répertoire). Il est aussi primordial de gérer plusieurs clients à la fois.

## Organisation

David => Fonction image.
Vincent => Le reste.

## Autres

Donnez ici toutes les autres informations qui vous paraissent importantes, puis supprimez cette ligne.
