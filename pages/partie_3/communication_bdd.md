---
layout: center
---
## Communication avec la base de données

La communication entre le **serveur** et la **base de données (ici PostgreSQL)** est assurée à l’aide de l’ORM (Object Relational Mapper) **Prisma**.  

- Simplifie les interactions avec la base via une abstraction entre le code JavaScript et le langage SQL.
- Sécurise les interactions en limitant à des opérations spécifiques
- Evite les bugs car chaque méthode utilisée peut déclencher une erreur avant l'envoie en BDD
- Permet la gestion des migrations (historique des différentes opérations appliquées à la base de données)

Les différents *services* du back-end appellent différentes fonctions Prisma pour effectuer les opérations de lecture, d’écriture, de mise à jour et de suppression de données (CRUD) pour chacunes des ressources de l'application (contrats, utilisateurs...). 

---
layout: center
---


## Modèles Prisma

**Modèle Prisma** : 
Entité de l'application/table de la base de données (sauf table de liaison)
Ils servent à Prisma pour définir les opérations possibles à réaliser sur la ressource concernée, mais aussi à PostgreSQL pour définir les différentes tables et colonnes à créer.

**Fichier schema.prisma** : 
- Les modèles sont définis dans ce fichier . 
- Sert aussi pour la configuration du client Prisma, permettant la connexion à différents types de base de données via des adapteurs.

**Prisma CLI:**
- permet d'exécuter différentes opérations depuis le terminal.
