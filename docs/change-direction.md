# Method: Change Direction (LEFT/RIGHT)

This method changes the direction of the car and is portrayed by a clock face.
If the command dictates a `RIGHT` turn the exectution will be made using the Global Variables and could look something like this `turn_steering_wheel(RIGHT)`.
Conditionals will need to be used to stop the integer from rising past 12 and sinking below 1.


<p align="center"> 
<img src="/docs/assets/clock.jpg" width="300">
</p>

```py
        # remember! this is inside a class
    def turn_steering_wheel(self, direction_change):

        #check is broken

        # self.direction += direction_change

        # if self.direction is 13 make it 1
        # if self.direction is 0 make it 12

```

