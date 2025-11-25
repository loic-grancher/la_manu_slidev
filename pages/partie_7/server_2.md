---
layout : two-cols

---
Client:
<div class="px-4">

```js
// src/helpers/contractsHelpers.js
async function getContracts() {
  const response = await apiClient("contracts/", 
  { method: "GET" }
  );
  return response;
}
```
</div>

::right::

<v-click>


Serveur:
```js
// src/routes.js

//On crée les routes et on les exporte via une fonction
export default (router) => {
  ...
  router.use("/contracts", contract);
```


</v-click>
<v-click>


```js
// server.js
import routes from "./src/routes.js";

const app = express();
...
const router = Router(); 
...
// On passe notre router à notre fonction de création de routes
routes(router);
...
app.listen(port, () => {
  console.log(`listening on port http://localhost:${port}`);
});

```

</v-click>
