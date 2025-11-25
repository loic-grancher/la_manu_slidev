---
layout: two-cols
---
<div class="p-2">

## Tests serveur

<br/>

- Jest 
- Tests séparés par fonctionnalité 
- Exécutés via script NPM

```js
test("loginSuccess", async () => {
    const loggedUser = await authService.login(
        "admin@demo.com", "password"
        );

    expect(loggedUser).toHaveProperty("token");
    expect(loggedUser.token).toBeDefined();
    expect(loggedUser.token.length)
    .toBeGreaterThanOrEqual(8);
});

```

</div>

::right::

<v-click>


<div class="p-2">

## Tests client

<br/>

- Vitest

```js
test('handleNameInitials returns correct initials', () => {
    expect(handleNameInitials("Henri Dupont")).toBe("HD");
    expect(handleNameInitials("Alice Berger")).toBe("AB");
    expect(handleNameInitials("")).toBe("?");
    expect(handleNameInitials(null)).toBe("?");
});
```

</div>

 </v-click>