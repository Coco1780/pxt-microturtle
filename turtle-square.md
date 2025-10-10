# Le carré de la tortue

## Introduction @unplugged

Imagine qu'il y a une tortue virtuelle, représentée par une LED, et que tu peux contrôler avec des blocs. Dans ce tutoriel, nous allons apprendre à utiliser la tortue et dessiner un carré.

## Déplacer la tortue

La tortue démarre au centre de l'écran et regarde vers le haut. Place un bloc ``||turtle:avancer||`` pour la déplacer vers le haut.

```blocks
turtle.forward(1)
```

## Turning and moving

Place un bloc ``||turtle:tourner à droite||`` pour tourner la tortue et place un autre bloc ``||turtle:avancer||`` pour qu'elle bouge de nouveau.

```blocks
turtle.forward(1)
turtle.turnRight()
turtle.forward(1)
```

## Dessiner un carré

Si tu ajoute assez de blocs ``||turtle:tourner à droite||`` et ``||turtle:avancer||``, la tortue peut dessiner un carré. 

Tu peux déplacer les blocs à l'intérieur de ``||input:lorsque le bouton est pressé||`` pour facilement relancer le code.

```blocks
input.onButtonPressed(Button.A, function() {
    turtle.forward(1)
    turtle.turnRight()
    turtle.forward(1)
    turtle.turnRight()
    turtle.forward(1)
    turtle.turnRight()
    turtle.forward(1)
    turtle.turnRight()
})
```

## Répeter avec "pour"

Est-ce que tu as remarqué que, pour dessiner un carré, les mêmes blocs se répètent ? Essaies d'utiliser la boucle ``pour`` afin d'obtenir le même résultat.

```blocks
input.onButtonPressed(Button.A, function() {
    for(let index = 0; index <= 3; index++) {
        turtle.forward(1)
        turtle.turnRight()
    }
})
```

## Laisser une trace

La tortue tient un **crayon** qui peut allumer les LEDs. Si tu ajoute le bloc ``||turtle:crayon||``, cela va laisser une trace sur le chemin de la tortue.

```blocks
input.onButtonPressed(Button.A, function() {
    turtle.pen(TurtlePenMode.Down)
    for(let index = 0; index <= 3; index++) {
        turtle.forward(1)
        turtle.turnRight()
    }
})
```

```package
tortue=github:Coco1780/pxt-microturtle#master
```