## Affichage et servo-moteur activés grâce à un circuit avec un bloc de condition @unplugged
Programme le micro:bit pour pour qu'une image spécifique s'affiche lorsque le circuit est fermé et que le servo-moteur s'active ou qu'un autre image nous informe que le circuit est ouvert.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Étape 1
Glisse le bloc ``||basic: montrer l'icône||`` dans sous le bloc  ``||basic:au démarrage|`` .
#### Choisis le crochet.
`
``` blocks

basic.showIcon(IconNames.Yes)
})


```

## Étape 2
Glisse le bloc  ``||pins: régler position servo broche P0 à 180||`` .
#### Choisis P1 et remplace 180 par 0.

``` blocks
basic.showIcon(IconNames.Yes)
pins.servoWritePin(AnalogPin.P1, 0)
```

## Étape 3
Glisse le bloc `` || logic: Si vrai sinon|| `` dans le bloc  ``||basic:toujours||`` 

``` blocks
basic.forever(function () {
    if (true) {
    } else {
```
## Étape 4
Remplace le mot vrai par le bloc  ``||input: broche P1 est pressée||``
``` blocks
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        } else {
```
## Étape 5
Glisse 3 blocs ``||basic:  montrer l'icône||`` dans l'espace sous le si.
#### Utilise les mêmes icônes que dans l'indice.

```blocks
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        // Objet conducteur
        basic.showIcon(IconNames.Diamond)
        // Objet conducteur
        basic.showIcon(IconNames.Target)
        // Objet conducteur
        basic.showIcon(IconNames.SmallDiamond)

    } else {
```

## Étape 6
Glisse le bloc ``||pins:régler position servo broche P0 à 180 ||`` sous le dernier bloc ``||basic:  montrer l'icône||`` .
#### Choisis la broche P1 et remplace 180 par 90

``` blocks
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        // Objet conducteur
        basic.showIcon(IconNames.Diamond)
        // Objet conducteur
        basic.showIcon(IconNames.Target)
        // Objet conducteur
        basic.showIcon(IconNames.SmallDiamond)
        pins.servoWritePin(AnalogPin.P1, 90)
    } else {
    ```

## Étape 7
Glisse le bloc ``||basic:  pause||`` sous le bloc ``||pins:régler position servo broche P0 à 90 ||`` 
#### Remplace 100 par 5000.

```blocks
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        // Objet conducteur
        basic.showIcon(IconNames.Diamond)
        // Objet conducteur
        basic.showIcon(IconNames.Target)
        // Objet conducteur
        basic.showIcon(IconNames.SmallDiamond)
        pins.servoWritePin(AnalogPin.P1, 90)
        basic.pause(5000)
    } else {
    ```
## Étape 8
Glisse le bloc ``||pins:régler position servo broche P0 à 180 ||`` sous  le bloc ``||basic:  pause||`` .
#### Choisis la broche P1 et remplace 180 par 0.

``` blocks
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        // Objet conducteur
        basic.showIcon(IconNames.Diamond)
        // Objet conducteur
        basic.showIcon(IconNames.Target)
        // Objet conducteur
        basic.showIcon(IconNames.SmallDiamond)
        pins.servoWritePin(AnalogPin.P1, 90)
        basic.pause(5000)
        pins.servoWritePin(AnalogPin.P1, 0)
    } else {
    ```
## Étape 9
Glisse le bloc ``||basic:  montrer l'icône||`` dans l'espace sous le sinon.
#### Utilise le même icône que dans l'indice.

``` blocks
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        // Objet conducteur
        basic.showIcon(IconNames.Diamond)
        // Objet conducteur
        basic.showIcon(IconNames.Target)
        // Objet conducteur
        basic.showIcon(IconNames.SmallDiamond)
        pins.servoWritePin(AnalogPin.P1, 90)
        basic.pause(5000)
        pins.servoWritePin(AnalogPin.P1, 0)
    } else {
        // Objet isolant
        basic.showIcon(IconNames.No)
    ```

## Bravo! Tu as terminé
Connecte tes fils à pince crocodile comme sur l'image
<img src="https://raw.githubusercontent.com/technomil/tutoriels_technomil/master/branchement%20boule.png" alt="Branchement Boule" width="300">

``` blocks
basic.showIcon(IconNames.Yes)
pins.servoWritePin(AnalogPin.P1, 0)
basic.forever(function () {
    if (input.pinIsPressed(TouchPin.P1)) {
        // Objet conducteur
        basic.showIcon(IconNames.Diamond)
        // Objet conducteur
        basic.showIcon(IconNames.Target)
        // Objet conducteur
        basic.showIcon(IconNames.SmallDiamond)
        pins.servoWritePin(AnalogPin.P1, 90)
        basic.pause(5000)
        pins.servoWritePin(AnalogPin.P1, 0)
    } else {
        // Objet isolant
        basic.showIcon(IconNames.No)
    }
})

```
