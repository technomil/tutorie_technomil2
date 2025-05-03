## Danseur endiablé! @unplugged
Programme le micro:bit pour qu'un danseur s'anime lorsque tu pèses sur un bouton
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime les blocs ``||basic:au démarrage||`` et ``||basic:au toujours||`` 
#### Glisse-les vers la gauche, tu verras apparaître une poubelle


## Étape 1
Glisse le bloc ``||input:lorsque le bouton A est pressé||``.


```blocks
input.onButtonPressed(Button.A, function ()

```
## Étape 2
Ajoute le bloc ``||loops:répéter||`` dans le bloc  ``||input:lorsque le bouton A est pressé||``.
#### Conserve le chiffre 4.
 ```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
 

```
## Étape 2

Ajoute le bloc ``||basic:montrez LEDs||`` dans le bloc ``||loops:répéter||``.
#### Dessine le corps du danseur.

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        basic.showLeds(`
            # . # . .
            # # # # #
            . . # . #
            . . # # .
            . # . # .
            `)


```

## Étape 3

Duplique le bloc ``||basic:montrez LEDs||`` (bouton droit de la souris - reproduire).
#### Modifie la position des bras du danseur

```blocks
input.onButtonPressed(Button.A, function () {
    for (let index = 0; index < 4; index++) {
        basic.showLeds(`
            # . # . .
            # # # # #
            . . # . #
            . . # # .
            . # . # .
            `)
        basic.showLeds(`
            . . # . #
            # # # # #
            # . # . .
            . . # # #
            . # . . .
            `)
    }
})


```

## Terminé! 

Bravo! Tu as réussi! 
##### Tu peux t'amuser à ajouter des mouvements en dupliquant et en modifiant le bloc "Montrez LEDs"