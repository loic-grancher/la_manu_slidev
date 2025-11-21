---
layout: center
---
# Architecture générale
L’application repose sur une architecture logicielle de type *client-serveur*.  
 Cette architecture sépare la partie visible par l’utilisateur (le front-end) de la partie métier et des traitements de données (le back-end).

    #figure(
  image("/assets/diagram_client_server.png", width: 80%),
  caption: [
    Schéma d'architecture client-serveur 
  ],

 )



Le client, développé en *React* (libraririe front-end) avec *Vite* (asset bundler), communique avec le serveur *Node.js / Express* au moyen d’une *API RESTful*.  

Une api "REST" (REpresentational State Transfer) répond aux critères suivants:
-* Uniformité de l'interface*,  qui permet de facilement identifier les différentes ressources accessibles. Les réponses du serveurs présentent les données de manière structurée et cohérentes. Seule l'url et ses paramètres éventuels (hors authentification) sont nécessaires pour accéder aux données.
- *Séparation du client et du seveur*: l'api ne renvoie que des données et n'est pas affectée par le client. On doit pouvoir changer ce dernier sans que cela affecte le fonctionnement de l'API
- *Sateless*: chaque requête est indépendante et ne dépend par d'autres informations ou opérations effectuées précédemment. C'est l'application client qui gère tous les états.
-* Mise en cache*: une réponse peut être mise en cache (requêtes GET) ou non (requêtes POST)
- *Structure en couches*: l'API utilise un système de couches indépendantes 


 Dans notre cas, s'agissant d'une API JSON, elle opère un échange entre le client et le serveur via des requêtes HTTP (GET, POST, PUT, DELETE) et des réponses au format *JSON*.