## Fais jouer une mélodie grâce à un circuit @unplugged
Programme le micro: bit pour qu'une mélodie  joue lorsque le circuit est fermé. 
<img src="https://raw.githubusercontent.com/technomil/tutoriels_technomil/master/branchement%20boule.png" alt="Branchement Boule" width="300">
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer

Supprime le bloc`` || basic: toujours | ``.
#### Glisse - le vers la gauche, tu verras apparaître une poubelle

## Étape 1
Place le bloc`` || basic: montrer LEDs || `` dans le bloc`` || basic: au démarrage || ``
#### Dessine le chiffre 0

```blocks

basic.showLeds(`
    .# # #.
    .#.#.
    .#.#.
    .#.#.
    .# # #.
    `)

```


## Étape 2
Place le bloc`` | input: lorsque la broche est activé || ``
#### Choisis la broche P1.
```blocks

input.onPinPressed(TouchPin.P1, function () {
    
})
```

## Étape 3
Place le bloc`` || music: jouer tonalité || `` dans le bloc`` | input: lorsque la broche est activé || ``
#### Choisis la note de ton choix

```blocks
})
input.onPinPressed(TouchPin.P1, function () {
   
music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})

```
## Étape 4

Ajoute 4 blocs`` || music: jouer tonalité || `` dans le bloc`` | input: lorsque la broche est activé || ``
#### Choisis les notes et les durées de ton choix

```blocks

})input.onPinPressed(TouchPin.P1, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(349, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(220, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
})

```

## Étape 5
Connecte tes fils à pince crocodile comme sur l'image
<img src="https://raw.githubusercontent.com/technomil/tutoriels_technomil/master/branchement%20boule.png" alt="Branchement Boule" width="300">

## Bravo!
Tu as réussi à faire jouer une mélodie grâce à un circuit!


