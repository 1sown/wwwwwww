# SnowayAPI

SnowayAPI est une bibliothèque JavaScript conçue pour interagir avec l'API Snoway. Elle fournit des méthodes pour récupérer différentes informations à partir de l'API Snoway.

## Installation

Pour installer SnowayAPI, vous pouvez utiliser npm :

```bash
npm install snoway-api
```

## Utilisation

```javascript
const SnowayAPI = require('snoway-api');

// Initialisez SnowayAPI avec votre clé API
const snoway = new SnowayAPI('VOTRE_CLE_API');

// Exemple d'utilisation pour récupérer les noms précédents d'un utilisateur
snoway.getNames('ID_UTILISATEUR').then(data => {
    console.log(data);
}).catch(error => {
    console.error(error);
});
```

## Documentation des méthodes

### `getNames(userID)`

Récupère les noms précédents d'un utilisateur.

- `userID` : Identifiant de l'utilisateur pour lequel récupérer les noms précédents.
- Retourne une promesse qui résout en un objet contenant les noms précédents de l'utilisateur, ou `null` si aucune donnée n'est disponible.

### `getDisplay(userID)`

Récupère l'affichage précédent d'un utilisateur.

- `userID` : Identifiant de l'utilisateur pour lequel récupérer l'affichage précédent.
- Retourne une promesse qui résout en un objet contenant l'affichage précédent de l'utilisateur, ou `null` si aucune donnée n'est disponible.

### `allPrevnames(userID)`

Récupère tous les noms précédents d'un utilisateur.

- `userID` : Identifiant de l'utilisateur pour lequel récupérer tous les noms précédents.
- Retourne une promesse qui résout en un objet contenant tous les noms précédents de l'utilisateur, ou `null` si aucune donnée n'est disponible.

### `ping()`

Effectue une requête ping à l'API pour vérifier la connectivité.

- Retourne une promesse qui résout en un objet contenant le résultat de la requête ping, ou `null` si aucune donnée n'est disponible.

### `count()`

Récupère le nombre de noms précédents enregistrés dans l'API.

- Retourne une promesse qui résout en un objet contenant le nombre de noms précédents enregistrés, ou `null` si aucune donnée n'est disponible.
