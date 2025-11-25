---
layout: image-left
image: /images/architecture_client.png
backgroundSize: contain

---
## Architecture frontend

- **components** :  composants réutilisables (cartes, boutons...)
- **helpers** :  fonctions utilitaires  pour communiquer avec le serveur. Pour envoyer et à recevoir des données via l’API
- **views** : Composants React spécialisés appelés par le routeur et associés à une URL unique. 
-  **assets**  ressources statiques nécessitant un traitement par Vite (les autres ressources statiques se trouvant dans /public)
-  **utils** contient différentes fonctions utilitaires pour l'application sans lien avec les entités de bas de données.

