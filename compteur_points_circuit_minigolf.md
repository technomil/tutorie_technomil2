## Crée un compteur de points
Programme ton micro:bit pour que les points augmentent lorsque le circuit est activé.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Étape 1
Clique sur ``||variables: variable||``
#### Clique ensuite sur créer une variable et donne-lui le nom "points".


##Étape 2
Glisse le bloc ``||variables:définir points à||`` dans le bloc ``||basic:au démarrage|``.

```blocks

let point = 0
point = 0

})

```
## Étape 3

Glisse le bloc ``||basic:montrer nombre||`` dans le bloc ``||basic:toujours||`` 


``` blocks

let point = 0
point = 0
basic.forever(function () {
    basic.showNumber()
})


```

## Étape 4
Glisse le bloc ``||variables:points||`` dans le bloc  ``||basic:montrer nombre||`` 


```blocks
let point = 0
point = 0
basic.forever(function () {
    basic.showNumber(point)
})
```

## Étape 5

Glisse le bloc ``||input:lorsque la broche P0 est activée||``.

```blocks
input.onPinPressed(TouchPin.P0, function () {
   
```


## Étape 6
Glisse le bloc ``||variables:modifier points de||`` dans le bloc ``||input:lorsque la broche P0 est activée||``.
#### Assure-toi qu'il soit bien écrit 1 dans le bloc ``||variables:modifier points de||``.
```blocks
input.onPinPressed(TouchPin.P0, function () {
    point += 1
})
   
```

## Étape 7
Glisse le bloc ``||input:lorsque le bouton A est pressé||``.

```blocks
input.onButtonPressed(Button.A, function () {
   
```

## Étape 8
Glisse le bloc ``||variables:définir point à||`` dans le bloc ``||input:lorsque le bouton A est pressé||``.
#### Assure-toi qu'il soit bien écrit 0 dans le bloc ``||variables:définir point à||``.
``` blocks

input.onButtonPressed(Button.A, function () {
    point = 0
})
```

## Étape
Branche ton servo-moteur comme sur le simulateur. Assure-toi de choisir la bonne broche!
### Bravo! Tu as réussi!

``` blocks

input.onPinPressed(TouchPin.P0, function () {
    point += 1
})
input.onButtonPressed(Button.A, function () {
    point = 0
})
let point = 0
point = 0
basic.forever(function () {
    basic.showNumber(point)
})


```