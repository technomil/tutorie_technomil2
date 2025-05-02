## Initiation au servo moteur - la suite @unplugged
Programme le micro:bit pour que le servo-moteur s'active selon le bouton pressé.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime les blocs ``||basic:toujours||`` et  ``||basic:au démarrage||``  .
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.


## Étape 1

Glisse le bloc ``||input:lorsque le bouton A est pressé||``.


```blocks
input.onButtonPressed(Button.A, function () {

})

````
## Étape 2

Glisse le bloc ``||pins: régler position servo broche||``dans le bloc  ``||input:lorsque le bouton A est pressé||``.
#### Choisi la broche P1 et remplace 0 par 90.

``` blocks
input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 90)
    
})
```

## Étape 3

Glisse le bloc ``||input:lorsque le bouton A est pressé||``.
#### Remplace A par B

```blocks
input.onButtonPressed(Button.B, function () {

})

````
## Étape 4

Glisse le bloc ``||pins: régler position servo broche||``dans le bloc  ``||input:lorsque le bouton B est pressé||``.
#### Choisi la broche P1

``` blocks
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 0)
    
})
```


## Étape 5
Branche ton servo-moteur comme sur l'image (regarde dans ton cahier de tutoriel au besoin)
### Bravo! Tu as réussi!

``` blocks

input.onButtonPressed(Button.A, function () {
    pins.servoWritePin(AnalogPin.P1, 180)
})
input.onButtonPressed(Button.B, function () {
    pins.servoWritePin(AnalogPin.P1, 0)
})

```` 
