## Des servo-moteurs qui s'activent avec l'inclinaison @unplugged
Programme le micro:bit pour que le servo-moteur s'active selon l'inclinaison du micro:bit
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime les blocs ``||basic:toujours||`` et  ``||basic:au démarrage||``  .
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.


## Étape 1

Glisse le bloc ``||input:lorsque secouer||``.
#### Remplace secouer par incliner à droite
``` blocks

input.onGesture(Gesture.TiltRight, function () {
    

```
## Étape 2

Glisse le bloc ``||pins: régler position servo broche||``dans le bloc  ``||input:lorsque incliner à droite||``.
#### Choisis la broche P1 et assure-toi que le chiffre 180 soit inscrit.
``` blocks

input.onGesture(Gesture.TiltRight, function () {
    pins.servoWritePin(AnalogPin.P1, 180)



```

## Étape 3

Glisse le bloc ``||input:lorsque secouer||``.
#### Remplace secouer par incliner à gauche
``` blocks

input.onGesture(Gesture.TiltLeft, function () {
    

```

##Étape 4
Glisse le bloc ``||pins: régler position servo broche||``dans le bloc  ``||input:lorsque incliner à gauche||``.
#### Choisis la broche P1 et assure-toi que le chiffre 0 soit inscrit.
``` blocks

input.onGesture(Gesture.TiltLeft, function () {
    pins.servoWritePin(AnalogPin.P1, 0)



```

## Étape 5
Branche ton servo-moteur comme sur l'image (regarde dans ton cahier de tutoriel au besoin)
### Bravo! Tu as réussi! Peux-tu ajouter un autre bloc où le mouvement du micro:bit fait s'activer le servo-moteur?

``` blocks

input.onGesture(Gesture.TiltRight, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
})
input.onGesture(Gesture.TiltLeft, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
})


```
