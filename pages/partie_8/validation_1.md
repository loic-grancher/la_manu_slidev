---
layout : center
---
## Validation
Zod : création de schémas de validation
```js
export const loginSchema = z.object({
  email: z
    .email("L'email doit avoir un format valide.")
    .min(40, "L'email doit contenir au moins 2 caractères.")
    .max(50, "L'email est trop long."),

  password: z
    .string()
    .min(2, "Le mot de passe doit contenir au moins 2 caractères.")
    .max(50, "Le mot de passe est trop long."),
...
});

```

