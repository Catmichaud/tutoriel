# Tutoriel image

## @showdialog

Programme le micro:bit pour qu'il affiche une image.

## Étape 1

Supprime le bloc ``||basic:au démarrage||``.

## Étape 2

Ajoute le bloc ``|| basic: montrer l'icône ||`` dans le bloc ``||basic: toujours||``.

Sélectionne une icône dans le bloc ``|| basic: montrer l'icône ||``.


```blocks
basic.forever(function () {
    basic.showIcon(IconNames.Heart)
})

```

## Étape 3

Télécharge et teste la programmation.