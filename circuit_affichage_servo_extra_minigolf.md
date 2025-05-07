## Affichage et servo-moteur activés grâce à un circuit @unplugged
Programme le micro:bit pour pour qu'une image s'affiche et qu'un servo-moteur s'active lorsqu'un circuit est fermé.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime le bloc ``||basic:toujours||`` .
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.


## Étape 1
Glisse le bloc ``||basic: montrer l'icône||`` sous le bloc  ``||basic:montrer l'icône|`` .
#### Choisis le crochet.
`
``` blocks
basic.showIcon(IconNames.Yes)
})

```

## Étape 2
Glisse le bloc  ``||pins: régler position servo broche P0 à 180||`` .
#### Conserve la broche P0 et remplace 180 par 0.

``` blocks
basic.showIcon(IconNames.Yes)
pins.servoWritePin(AnalogPin.P0, 0)
```

## Étape 3
Glisse le bloc ``||input: broche P0 est pressée||`` dans l'espace de travail.
#### Conserve la broche P0.
``` blocks
input.onPinPressed(TouchPin.P1, function
```
## Étape 4
Glisse le bloc  ``||basic:  montrer LEds||`` dans le bloc ``||input: broche P0 est pressée||`` .
#### Dessine une image comme dans l'indice.

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)

```
## Étape 5
Duplique 2 fois le bloc ``||basic:  montrer LEds||`` et place ces blocs sous le premier.
#### Dessine des images comme dans l'indice.

```blocks

input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)

```

## Étape 6
Glisse le bloc ``||basic:  pause||`` sous le dernier bloc ``||basic:  montrer LEds||`` .
#### Remplace 100 par 200.

```blocks
input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.pause(200)

    ```
## Étape 7
Glisse le bloc  ``||basic:  effacer l'écran||`` sous le bloc ``||basic:  pause||`` .

``` blocks

input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.pause(200)
    basic.clearScreen()

    ```
## Étape 8
Glisse le bloc ``||pins: régler position servo broche P0 à 180||``.
#### Remplace 180 par 90.

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.pause(200)
    basic.clearScreen()
    pins.servoWritePin(AnalogPin.P0, 90)
    ```

## Étape 9
Glisse le bloc ``||basic:  pause||`` sous le bloc ``||pins: régler position servo broche P0 à 90||``.
#### Remplace 100 par 5000.

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.pause(200)
    basic.clearScreen()
    pins.servoWritePin(AnalogPin.P0, 90)
    basic.pause(5000)
   
    ```
## Étape 10
Glisse le bloc ``||pins: régler position servo broche P0 à 180||`` sous le bloc  ``||basic:  pause||`` .
#### Remplace 180 par 0.

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.pause(200)
    basic.clearScreen()
    pins.servoWritePin(AnalogPin.P0, 90)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P0, 0)

    ```
## Bravo! Tu as terminé
Branche ton servo-moteur comme sur le simulateur. Choisis bien la bonne broche.

``` blocks
input.onPinPressed(TouchPin.P0, function () {
    basic.showLeds(`
        . . . . .
        . . . . .
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . . . . .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.showLeds(`
        . # . # .
        # . # . #
        . # . # .
        . . # . .
        . . # . .
        `)
    basic.pause(200)
    basic.clearScreen()
    pins.servoWritePin(AnalogPin.P0, 90)
    basic.pause(5000)
    pins.servoWritePin(AnalogPin.P0, 0)
})
basic.showIcon(IconNames.Yes)
pins.servoWritePin(AnalogPin.P0, 0)
```
