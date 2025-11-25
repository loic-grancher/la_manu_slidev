---
layout : two-cols
---


<div class="p-2"> 

## Validation client

<br/>


 - Via React Hook Form. grâce à un adaptateur

```js
  const form = useForm({
    resolver: zodResolver(contractCreateSchema),
});
```

 - Vérifie les données avant leur envoi
 - Bloque la requête si non conforme et affiche les erreurs

</div>


::right::

<v-click>

<div class="p-2"> 

## Validation serveur

<br/>

- Via la fonction safeParse dans le contrôleur

```js
    const parsedData = loginSchema.safeParse({ 
      email, password 
    });
```

- Continue les opération si valide
- Sinon renvoie une erreur

</div>

</v-click>
