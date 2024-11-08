# Tutoriel veilleuse

## @showdialog

Transforme le micro:bit en veilleuse.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Crée une ``||variables: variable||`` et donne-lui le nom ``||variables:Lumière||``.

Ajoute le bloc ``||variables: définir Lumière||`` dans le bloc ``||basic: toujours||``.

```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = 0
})

```

## Étape 3

Remplace la valeur ``||variables: 0||`` du bloc ``||variables: définir Lumière ||`` par le bloc ``||input: niveau d'intensité lumineuse||``. 


```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = input.lightLevel()
})

```

## Étape 4

Ajoute le bloc ``|| logic: si vrai alors sinon ||`` sous le bloc ``|| variables: définir Lumière ||``.

```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = input.lightLevel()
    if (true) {
    	
    } else {
    	
    }
})

```

## Étape 5

Remplace la valeur ``|| logic: vrai ||`` du bloc ``|| logic: si vrai alors sinon ||`` par le bloc ``|| logic: 0 < 0||``. 

```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = input.lightLevel()
    if (0 < 0) {
    	
    } else {
    	
    }
})

```

## Étape 6

Remplace la valeur ``|| logic: 0 ||`` à la gauche du bloc ``|| logic: 0 < 0||`` par le bloc ``|| variables: Lumière||``. 

Remplace la valeur ``|| logic: 0 ||`` à la droite du bloc ``|| logic: 0 < 0||`` par la valeur ``|| logic: 40 ||``.

Lorsque le niveau d'intensité lumieuse est sous 40 dans une pièce, il fait généralement sombre! 

```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = input.lightLevel()
    if (Lumière < 40) {
    	
    } else {
    	
    }
})

```

## Étape 7

Ajoute le bloc ``|| basic: Montrer LEDs ||`` sous le bloc ``|| logic: si ||``.

Remplis les 25 cases pour activer toutes les LEDs du micro:bit.

```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = input.lightLevel()
    if (Lumière < 40) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
    	
    }
})

```

## Étape 8

Ajoute le bloc ``|| basic: montrer LEDs ||`` sous le bloc ``|| logic: sinon ||``.

Active seulement la LED centrale du micro:bit.

```blocks

let Lumière = 0
basic.forever(function () {
    Lumière = input.lightLevel()
    if (Lumière < 40) {
        basic.showLeds(`
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            # # # # #
            `)
    } else {
        basic.showLeds(`
            . . . . .
            . . . . .
            . . # . .
            . . . . .
            . . . . .
            `)
    }
})

```

## Étape 9

Télécharge et teste la programmation.

## Étape 10

Manipule le micro:bit. Ferme les lumières au besoin... 

Que remarques-tu ? 