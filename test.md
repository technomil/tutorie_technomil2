``` blocks

input.onButtonPressed(Button.A, function () {
    servos.P0.setAngle(100)
})
input.onButtonPressed(Button.B, function () {
    servos.P0.setAngle(0)
})
servos.P0.setAngle(0)

``` 

