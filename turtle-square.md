# Le carré de la tortue

## Introduction @unplugged

Image qu'il y a une tortue virtuelle, représentée par une LED, et que tu peux contrôler avec des commandes. Dans ce tutoriel, nous allons apprendre à utiliser la tortue et dessiner un carré.

## Déplacer la tortue

La torrtue démarre au centre de l'écran et regarde vers le haut. Place un bloc ``||turtle:forward||`` pour la déplacer vers le haut.

```blocks
turtle.forward(1)
```

## Turning and moving

Place a ``||turtle:turnRight||`` to turn the turtle and place another ``||turtle:forward||`` block to make it move again.

```blocks
turtle.forward(1)
turtle.turnRight()
turtle.forward(1)
```

## Drawing a square

If you add enough ``||turtle:turnRight||`` and ``||turtle:forward||`` blocks, the turtle will eventually draw a square. 

You can move the blocks into a ``||input:on button pressed||`` to easily run the code again.

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

## "for" is for repetition

Did you notice the pattern of repeated blocks needed to draw a square? Try using a ``for`` loop to achieve the same effect.

```blocks
input.onButtonPressed(Button.A, function() {
    for(let index = 0; index <= 3; index++) {
        turtle.forward(1)
        turtle.turnRight()
    }
})
```

## Leaving a trail

The turtle holds a **pen** that can turn on LEDs. If you add the ``||turtle:pen||`` block, it will leave a trail as the turtle moves.

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
microturtle=github:Coco1780/pxt-microturtle#master
```
