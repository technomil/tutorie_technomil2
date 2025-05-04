## Initiation au servo moteur @unplugged
Programme le micro:bit pour pour qu'une image s'affiche et qu'un servo-moteur s'active lorsqu'un circuit est fermé.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime le bloc ``||basic:toujours||`` .
#### Glisse-le vers la gauche, tu verras apparaître une poubelle.


## Étape 1
Glisse le bloc ``||basic: montrer l'icône||`` dans le bloc  ``||basic:toujours||`` 
#### Choisis le crochet
`
``` blocks
basic.showIcon(IconNames.Yes)
})

```
## Étape 2
Glisse le bloc  ``||servos: règle l'angle du servo moteur P0 à 90||`` 

``` blocks
basic.showIcon(IconNames.Yes)
servos.P1.setAngle(0)
```