## Fais jouer "Au clair de la lune" à ton micro:bit! @unplugged
Programme le Micro:bit pour qu'une mélodie joue lorsqu'un bouton est pressé.
##### En tout temps, clique sur l'ampoule pour avoir un indice.

## Avant de commencer
Supprime les blocs ``||basic:au démarrage||`` et ``||basic:toujours||``
#### Glisse-les vers la gauche, tu verras apparaître une poubelle

## Étape 1
Glisse le bloc`` || input: lorsque le bouton A est pressé || ``

```blocks
input.onButtonPressed(Button.A, function ()

```
## Étape 2
Glisse le bloc`` || Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` dans le bloc `` || input: lorsque le bouton A est pressé || ``.

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(262, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
```
## Étape 3
Clique sur "Middle C" (Do) et choisis la touche du piano "Middle G" (Sol). 

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
```

## Étape 4
Duplique 2 fois le bloc `` || Music: jouer tonalité Middle G pour 1 temps jusqu'à la fin||`` sous le premier bloc musical afin que ton Micro:bit joue "Sol-Sol-Sol".
#### Observe l'indice au besoin
###### Pour dupliquer, clique avec le bouton droit de la souris et choisis "Reproduire".

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
```

## Étape 5
Ajoute un autre bloc `` || Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` sous les 3 premiers.
#### Modifie Middle C (Do) pour Middle A (La).

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
```

## Étape 6
Ajoute un autre bloc `` || Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` sous les autres.
#### Modifie Middle C (Do) pour Middle B (Si) et le chiffre 1 pour le chiffre 2.

```blocks
input.onButtonPressed(Button.A, function () {
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(494, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
    })
```

## Étape 7
Ajoute un dernier bloc `` || Music: jouer tonalité Middle C pour 1 temps jusqu'à la fin||`` sous les autres.
#### Modifie Middle C (Do) pour Low A (La) et 1 pour 2.

```blocks
input.onButtonPressed(Button.A, function () {
music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(392, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Whole)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(494, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
    music.play(music.tonePlayable(440, music.beat(BeatFraction.Double)), music.PlaybackMode.UntilDone)
})
```

## Voilà! Tu as réussi!
### Télécharge la programmation dans ton Micro:bit et pèse sur le bouton A.
Amuse-toi à essayer de créer la suite de la chanson "Au clair de la lune". Les 5 prochaines notes sont: Sol-Si-La-La-Sol.

