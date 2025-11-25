---
layout : two-cols

---
Controllers:
<div class="px-4">


```js
// src/controllers/contract/index.js
const router = Router();
...
//Si l'url est simplement /contract, on appelle la fonction getAll
router.get("/", authMiddleware, getAll);
```

```js
// src/controllers/contract/getAll.js
export default async (req, res) => {
  try {
    //Gestion des paramètres de requete (simplifé)
    const limit = parseInt(req.query.limit) || 10;

    //Appel du service
    const contracts = await contractService.getAll(limit);

    //Envoi de la réponse standardisée
    ApiResponse.success(res, contracts);
    
  } catch (error) {
  //Envoi de l'erreur standardisée
    return ApiResponse.error(res, error);
  }
};

```
</div>

::right::

Service:
```js
// contractService.js
const getAll = async (limit = 10) => {
  try {
    const contracts = await prisma.contract.findMany({
      take: limit,
      include: {
        ...
        interventions: true
      },

      orderBy: {
        startDate: "desc",
      },
    });
    
    return contracts ;
    
  } catch (error) {
    console.error(error);
    throw error;
  }
};

```
