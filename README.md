# Snoway API

**Snoway API est une API simple qui vous permet de trouver l'ancien nom d'un utilisateur dans la base de données de Snoway.**

## Installation

Pour installer Snoway API, vous pouvez utiliser :

```bash
# NodeJS
$ npm install snoway-api 

# Yarn
$ yarn add snoway-api

# Bun
$ bun snoway-api snoway-api 
```

## Utilisation

```javascript
const SnowayAPI = require('snoway-api');

// Initialisez Snoway API avec votre clé API
const snoway = new SnowayAPI('VOTRE_CLE_API');

// Exemple d'utilisation pour récupérer les prevnames d'un utilisateur
snoway.getNames('ID_UTILISATEUR').then(data => {
    console.log(data);
}).catch(error => {
    console.error(error);
});
```

## Documentation des méthodes

### `getNames(userID)`

Récupère les prevnames d'un utilisateur.

- `userID` : Identifiant de l'utilisateur pour lequel récupérer les prevnames.
- Retourne une promesse qui résout en un objet contenant les prevnames de l'utilisateur, ou `null` si aucune donnée n'est disponible.

### `getDisplay(userID)`

Récupère l'affichage précédent d'un utilisateur.

- `userID` : Identifiant de l'utilisateur pour lequel récupérer l'affichage précédent.
- Retourne une promesse qui résout en un objet contenant l'affichage précédent de l'utilisateur, ou `null` si aucune donnée n'est disponible.

### `allPrevnames(userID)`

Récupère tous les prevnames d'un utilisateur.

- `userID` : Identifiant de l'utilisateur pour lequel récupérer tous les prevnames.
- Retourne une promesse qui résout en un objet contenant tous les prevnames de l'utilisateur, ou `null` si aucune donnée n'est disponible.

### `ping()`

Effectue une requête ping à l'API.

- Retourne le ping de l'API.

### `count()`

Récupère le nombre de prevnames enregistrés dans l'API.

- Retourne une promesse qui résout en un objet contenant le nombre de prevnames enregistrés, ou `null` si aucune donnée n'est disponible.


## 💖 Contributors

*  [**1sown**](https://github.com/1sown)
*  [**22ayman**](https://github.com/9ayman)
