---
layout : center

---

## Json Web Token

<br/>

- Généré lors du login après vérification des l'utilisateur
- Chiffré via un "secret"
- Renvoyé avec la réponse lors du login vers le client
- Envoyé par le client lors des opérations vers l'API
- Stocké côté client : 
    - cookie http (plus sûr, moins flexible)
    - local storage (plus facile, sécurité plus faible)

<v-click>

## Middleware

<br/>


- Analyse toutes les requêtes entrantes côté serveur
- Tente de lire et décode le jeton JWT de la requête
- Si valide: autorise l'opération (sauf contrôle de rôle supplémentaire)
- Si échec => erreur

</v-click>