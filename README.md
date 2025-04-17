# Documentation du module `Rai.js`

Ce module fournit des fonctions utiles pour travailler avec un canevas HTML5. Il permet de créer un canevas, de dessiner dessus, de gérer des couleurs, des images et de vider le canevas. 

## Fonctionnement général

Le module `Rai.js` est encapsulé dans une fonction immédiatement invoquée (IIFE) et est accessible via l'objet global `rai` dans votre application. Il expose plusieurs méthodes pour interagir avec un canevas.

## Méthodes

### `createCanvas(width, height)`
Crée un canevas avec les dimensions spécifiées et l'ajoute à la page HTML.

#### Paramètres :
- `width` : La largeur du canevas (en pixels).
- `height` : La hauteur du canevas (en pixels).

#### Exemple :
createCanvas(800, 600);

### `background(r, g, b)`
Change la couleur de fond du canevas.

#### Paramètres :
- `r` : La composante rouge de la couleur (0-255).
- `g` : La composante verte de la couleur (0-255). Si non fourni, la valeur de `r` sera utilisée.
- `b` : La composante bleue de la couleur (0-255). Si non fourni, la valeur de `r` sera utilisée.

#### Exemple :
background(255, 0, 0);  // Fond rouge

### `fill(r, g, b)`
Définit la couleur de remplissage pour les dessins futurs sur le canevas.

#### Paramètres :
- `r` : La composante rouge de la couleur (0-255).
- `g` : La composante verte de la couleur (0-255). Si non fourni, la valeur de `r` sera utilisée.
- `b` : La composante bleue de la couleur (0-255). Si non fourni, la valeur de `r` sera utilisée.

#### Exemple :
fill(0, 255, 0);  // Couleur de remplissage verte

### `rect(x, y, w, h)`
Dessine un rectangle rempli avec la couleur de remplissage actuelle.

#### Paramètres :
- `x` : La position x du coin supérieur gauche du rectangle (en pixels).
- `y` : La position y du coin supérieur gauche du rectangle (en pixels).
- `w` : La largeur du rectangle (en pixels).
- `h` : La hauteur du rectangle (en pixels).

#### Exemple :
rect(50, 50, 100, 100);  // Dessine un carré de 100x100 à (50, 50)

### `image(src, x, y, width, height)`
Affiche une image à une position spécifique avec une taille donnée.

#### Paramètres :
- `src` : Le chemin de l'image à afficher.
- `x` : La position x où l'image doit être placée.
- `y` : La position y où l'image doit être placée.
- `width` : La largeur de l'image (en pixels).
- `height` : La hauteur de l'image (en pixels).

#### Exemple :
image('image.png', 100, 100, 50, 50);  // Affiche une image de 50x50 à (100, 100)

#### Paramètres :
- `src` : Le chemin de l'image à afficher.
- `x` : La position x où l'image doit être placée.
- `y` : La position y où l'image doit être placée.
- `width` : La largeur de l'image (en pixels).
- `height` : La hauteur de l'image (en pixels).

#### Exemple :
image('image.png', 100, 100, 50, 50);  // Affiche une image en boucle à (100, 100)

## Exemple d'utilisation

Voici un exemple simple montrant l'utilisation de plusieurs fonctions du module `rai` :

createCanvas(800, 600);
background(0, 0, 255);  // Fond bleu
fill(255, 0, 0);  // Remplissage rouge
rect(50, 50, 100, 100);  // Dessine un carré rouge
image('sprite.png', 200, 200, 50, 50);  // Affiche une image

## Remarques
- Les images sont chargées de manière asynchrone. elle utiliseent `onload` pour garantir qu'elles sont bien affichées une fois complètement chargées.
- La taille du canevas et du contexte (`ctx`) sont stockées dans des variables globales accessibles via `window`.

## Auteurs

- Ce module a été développé Raikou 320, [github](https://github.com/Raikou320).
