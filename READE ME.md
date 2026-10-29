# Explication Projet

```js
// 1. On importe le module natif de Node.js qui permet de lire
//    ce que l'utilisateur tape dans le terminal
const readline = require("node:readline");
// 2. On crée une interface de communication avec le terminal
//    - input  : on lit ce que l'utilisateur écrit (process.stdin)
//    - output : on écrit dans le terminal (process.stdout)
const rl = readline.createInterface({
   input: process.stdin,
   output: process.stdout,
});
/ 3. On pose une question à l'utilisateur
//    La fonction de callback (answer) => { ... } est exécutée
//    uniquement quand l'utilisateur appuie sur Entrée
rl.question("Entrez un nombre : ", (answer) => {
    // 4. On convertit la réponse (qui est toujours une chaîne de caractères)
    //    en un vrai nombre grâce à Number()
    const number = Number(answer);

    // 5. On affiche le nombre converti dans le terminal
    console.log("le nombre est:", number);

    // 6. On ferme proprement l'interface pour terminer le programme
    rl.close();
});
