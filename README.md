# Formation Begin-Javascript / Exercice Pokemon

## Instructions

Dans cet exercice, on va avoir des Pokemons qui ont des attaques. On va créer une class Attack qui va prendre en paramètre un Pokemon et une attack et qui va retourner un nouveau Pokemon avec les points de vie mis à jour.

Pour ça, on va créer 3 classes :

### **Pokemon** : représente un pokemon

Chaque Pokemon possède un nom, un émoji, une health et 3 attaques. Il prend toutes les propriétés dans le constructor.

Notre Pokemon a aussi les méthodes suivantes :

- **randomAttack** choisit une attaque aléatoirement et retourne l'attaque choisie.

- **logAttack** affiche dans la console la liste des attaques avec 1 2 3 et le nom de l'attaque.

- **logPokemon** affiche le pokemon avec son nom, sa vie, ses attaques.

- **getHealth** retourne la vie du pokemon avec des 🟥 pour chaque 10% de PV perdu et des 🟩 pour chaque 10% de PV restant.

### **Attack** : représente une attaque

Elle possède un nom, un power et une stabilité !

Elle possède comme méthodes :

- **performAttack** : il calcule le nombre de damage en fonction de la stabilité et du power de l'attaque. Il retourne le nombre de damage. Pour calculer l'attaque, on génère un nombre aléatoire entre 0 et la puissance, puis on le multiplie par la stabilité. Plus la stabilité est basse, plus l'attaque pourra être faible.

- **logAttack** : une fonction pour afficher l'attaque avec les différentes propriétés !

Voici quelques pokemons de base que j'ai créés, mais tu peux créer ceux que tu veux :

```
const pikachu = new Pokemon('Pikachu', '⚡️', 100, [
  new Attack('Thunderbolt', 30, 0.2),
  new Attack('Electro Ball', 20, 0.4),
  new Attack('Quick Attack', 10, 0.8),
]);

const bulbasaur = new Pokemon('Bulbasaur', '🍃', 110, [
  new Attack('Vine Whip', 25, 0.3),
  new Attack('Seed Bomb', 20, 0.5),
  new Attack('Tackle', 10, 0.8),
]);

const charmander = new Pokemon('Charmander', '🔥', 90, [
  new Attack('Flamethrower', 35, 0.2),
  new Attack('Ember', 25, 0.3),
  new Attack('Scratch', 15, 0.75),
]);
```

### **Game** : représente le jeu

Game va être la class qui va gérer tout le jeu. Cette partie, je vais te laisser la réfléchir. Je vais juste te décrire le déroulement du jeu :

- L'utilisateur est invité à choisir un nombre entre 1 et 3 qui représente le pokemon sélectionné
- Le script génère un nombre aléatoire entre 1 et 2 qui représente le pokemon adverse (qui ne peut pas être le même que celui du player)
- Le script affiche ensuite les deux pokemons avec leur vie respective
- Le script demande au player de choisir une attaque
- Le script génère une attaque aléatoire pour le pokemon adverse
- Le script affiche le nombre de damage pour chaque pokemon
- Le script attend 5 secondes pour faire une petite pause
- Le script réaffiche les deux pokemons avec leur vie respective
- Etc... jusqu'à ce que l'un des 2 pokemons ait une vie de 0.
- Le script affiche le gagnant
