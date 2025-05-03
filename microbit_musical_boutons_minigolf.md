## Micro:bit musical @unplugged
Utilise les boutons pour jouer de la musique.

##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime les blocs ``||basic:au démarrage||`` et ``||basic:au toujours||`` 
#### Glisse-les vers la gauche, tu verras apparaître une poubelle.


## Étape 1
Glisse le bloc ``||input:lorsque le bouton A est pressé||``.


```blocks
input.onButtonPressed(Button.A, function ()

```
## Étape 2
Glisse le bloc ``|| Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` dans le bloc `` || input: lorsque le bouton A est pressé || ``.
#### Modifie Middle C pour Middle G (sol)

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
```

## Étape 3
Glisse le bloc ``||input:lorsque le bouton A est pressé||``.
#### Modifie A pour B


```blocks
input.onButtonPressed(Button.B, function ()

```
## Étape 4
Glisse le bloc `` || Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` dans le bloc `` || input: lorsque le bouton B est pressé || ``.
#### Modifie Middle C pour Middle A (la)

```blocks
input.onButtonPressed(Button.B, function () {
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)

```

## Étape 5
Glisse le bloc ``||input:lorsque le bouton A est pressé||``.
#### Modifie A pour A+B


```blocks
input.onButtonPressed(Button.AB, function ()

```
## Étape 5
Glisse le bloc `` || Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` dans le bloc `` || input: lorsque le bouton B est pressé || ``.
#### Modifie Middle C pour Middle B (si)

```blocks
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(494, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)

```

## Terminé! 

Bravo! Tu as réussi! 
##### Es-tu capable de jouer le début de "Frère Jacques" en utilisant les 3 boutons programmés?


``` blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})
input.onButtonPressed(Button.AB, function () {
    music.play(music.tonePlayable(494, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})
input.onButtonPressed(Button.B, function () {
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})

```

