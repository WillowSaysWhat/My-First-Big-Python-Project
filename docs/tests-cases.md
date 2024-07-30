# Test Cases

Here some commnads to paste into the simulation.txt file to check that your program has the necessary error handling implemented.

## Top Speed
This will test whether the car can accelerate over 80km/h.
The output should tell the user that the car cannot exceed top speed
` The car is at max speed`
```

FORWARD
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE

```

## Top Speed - Reverse
Now we will test whether the reverse top speed can be exceeded. If you have implemented the correct handling, the output should tell the user that -15km/h has been reached. `The car is at min speed`

```

REVERSE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
ACCELERATE
BRAKE
BRAKE
BRAKE
```

## Clockwise and anti-clockwise
Let's check to see if you have implemented the clock direction.
The direction variable should display as 12 and then make the changes below.

```
RIGHT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
LEFT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT
RIGHT

```

## Car is Broken

The car breaks when the car is in motion and the gear is changed in the opposite direction. for example, if the car is traveling forward and the car is placed in reverse, `BOOM! The car is broken!`

```

FORWARD
ACCELERATE
ACCELERATE
ACCELERATE
REVERSE

```

```
REVERSE
ACCELERATE
ACCELERATE
ACCELERATE
FORWARD

```
## Car is already stopped

This test will check whether the car will slip past `STOPPED` when too many `BRAKE` commands are issued.

```

FORWARD
ACCELERATE
ACCELERATE
BRAKE
BRAKE
BRAKE
BRAKE
BRAKE

```

