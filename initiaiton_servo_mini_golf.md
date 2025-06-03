## Initiation au servo moteur @unplugged
Programme le micro:bit pour que le servo-moteur s'active.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime le bloc ``||basic:toujours||`` .
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.



## Étape 1
Glisse le bloc ``||pins: régler position servo broche||`` dans le bloc ``||basic:au démarrage||``
#### Choisis P1 et remplace 180 par 0
`
``` blocks
pins.servoWritePin(AnalogPin.P1, 0)
```

## Étape 2

Glisse le bloc ``||input:lorsque le bouton A est pressé||``.
#### Remplace A par B

```blocks
input.onButtonPressed(Button.B, function () {

})

```
## Étape 3

Glisse le bloc ``||pins: régler position servo broche||``dans le bloc  ``||input:lorsque le bouton B est pressé||``.
#### Choisis la broche P1 et assure-toi qu'il est inscrit 180.

``` blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    
})
```

## Étape 4

Glisse le bloc ``||basic: pause|``sous le bloc  ``||pins: régler position servo broche||``.
#### Choisis la broche P1 et remplace 100 par 1000.

``` blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    basic.pause(1000)
    
})
```


## Étape 5

Glisse un autre bloc ``||pins: régler position servo broche||``dans le bloc  ``||input:lorsque le bouton B est pressé||``.
#### Choisis la broche P1 et modifie 180 par 0.

``` blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
    basic.pause(1000)
    pins.servoWritePin(AnalogPin.P1, 0)
})
```
## Étape 6
Branche ton servo-moteur comme sur l'image (regarde dans ton cahier de tutoriel au besoin)
### Bravo! Tu as réussi!



