---
layout: center
---
## Communication entre les couches

1. Le client envoie une requête. Cette requète possède une méthode "GET/POST/PUT..." et une url 

2. Le serveur, reçoit la requête via le contrôleur, exécute la logique correspondante et interroge la base de données via un service. 
    
3. Une fois le traitement effectué, le serveur renvoie la réponse au client sous forme de *données JSON* (données attendues ou erreur)
    
4. Le client récupère les données et les affiche ou les traite. S'il s'agit d'une erreur, il s'occupe de gérer son affichage ou le comportement à adopter