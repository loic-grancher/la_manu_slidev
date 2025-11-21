---
layout : image-right
image: /images/architecture_server.png
backgroundSize: contain
---
## Architecture serveur

- *Routes* : définissent les "endpoints" REST (les url qui constituent les points d'entrée de l'application)  et associent chaque chemin à ses middlewares et au contrôleur correspondant. 

- *Controllers* :  reçoivent les requêtes, valident les données, appellent le service correspondant à la tâche à accomplir et renvoient une réponse structurée.

- *Middlewares* : fonctions exécutées automatiquement avant/entre/après certains contrôleurs définis. Ils  gèrent des tâches telles que l'authentification ou les autorisations à certaines fonctionnalités ou ressources.



---

- *Services* :
  - gèrent le cœur de la logique métier et ils 
  - interagissent avec la base de données et/ou des API externes
  - appellent des librairies ou d'autres fonctionnalités,
  - gèrent les transactions en base de données

- *fichier server.js* : le "point d’entrée de l’application".Il  initialise et configure Express, charge les variables d’environnement, configure les middlewares globaux (CORS, parse JSON, logs), monte les routes, établit la connexion à la base et lance l’écoute du serveur. Lors de la mise en production, c'est lui que notre processus nodejs exécutera pour lancer le fonctionnement de l'API.
