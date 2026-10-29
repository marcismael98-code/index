# Explication du projet

Ce projet montre comment utiliser le module `readline` de Node.js pour demander une valeur à l'utilisateur dans le terminal et l'afficher après conversion en nombre.

## Code principal

```js
const readline = require("node:readline");

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
});

rl.question("Entrez un nombre : ", (answer) => {
  const number = Number(answer);
  console.log("Le nombre est :", number);
  rl.close();
});
```

## Explication

1. On importe le module `readline` de Node.js.
2. On crée une interface de communication avec le terminal.
3. On pose une question à l'utilisateur avec `rl.question()`.
4. La réponse est une chaîne de caractères ; on la convertit en nombre avec `Number()`.
5. On affiche le résultat dans le terminal.
6. On ferme proprement l'interface avec `rl.close()`.

## Comment lancer le projet

```bash
node index.js
```

Ensuite, entrez un nombre dans le terminal pour voir le résultat affiché.
