# Project Instructions

You have been assigned the task of completing a car simulator for a design strategy firm.

The previous employee has written some of the [boilerplate](#the-boilerplate-code) code and you are asked to comtinue to implement the sim using this code. Copy it into your `.py` file.

The sim will request commands from a text file located in your project. Please create a text file named `simulation.txt` next to your `.py` file and copy the [commands](#the-commands-for-simulationtxt) into `simulation.txt.`

### The Car

The car must follow these principles:

* `ACCELERATE` will speed the car up +5
* `BRAKE` will slow the car down -5
* `FORWARD` places the car in D or Drive
* `REVERSE` places the car in R or Reverse
* `RIGHT` turns the car clockwise
* `LEFT` turns the car anti-clockwise

### Braking Parameters

The car will -5 when braking in `FORWARD` and +5 when braking in `REVERSE`. The car cannot brake past zero (0) regardless of the commands given after it reaches zero. The read out could let the user know that the car has stopped

` "The car is already stopped!"`

### Accelerating Parameters

The car will +5 when accelerating in `FORWARD` and -5 when accelerating in `REVERSE.` The cars' top speed is 80km/h and 15km/h in `REVERSE.`

Like a real car, the sim must be at 0km/h to safely change from `D` to `R` and vise vera. If the sim commmand requests a change from `FORWARD` to `REVERSE` while the car is travelling at speed, the car will `BOOM!` break.

### Gear Change Parameters

The sim must change gears for the user. It is your decision when to check, but gear changes occur as follows.

`0 - 10 = first`    `10 - 20 = second`  `20 - 30 = third`   `30 - 40 = fourth`  `45 + = fifth`

Don't pressure yourself to have perfectly ratioed gears. Just focus on them changing close to the desired speed.

### Turn Steering Parameters

As this is a console-based project, the direction of travel is depicted by a 12-hour clock. The car starts at 12 and if it turns left it will noavigate a single increment on the clock to 11. If it turns right from 12 it will increment to 1.

<p align="center">
<img src="/docs/assets/clock.jpg" width="300">
</p>

### Console Output Parameters

The text-based output should look similar to this:

```txt
Braking...
Speed = 45 Gear = 5 Direction = 1

Accelerating...
Speed = 50 Gear = 5 Direction = 1

Turning...
Speed = 50 Gear = 5 Direction = 12

Braking...
Speed = 45 Gear = 5 Direction = 12

Braking...
Changing Gear...
Speed = 40 Gear = 4 Direction = 12

Reverse...
BOOM!
Car is Broken!
Car is Broken!
```





## The Boilerplate code
copy and paste this code into your editor/IDE.

```py
import time
# global variables.
RIGHT = 1
LEFT = -1
FORWARD = 1
REVERSE = 0

class Car:
    def __init__(self):
        self.speed = 0
        self.gear = 1
        self.direction = 0
        self.broken = False 
        self.simulation = []
        self.simulation_loaded = False

   def accelerate(self):
       pass

   def brake(self):
       pass

   def turn_steering_wheel(self, direction_change):
       pass

  def change_gear(self, selected_gear = FORWARD):
      pass

  def display_stats(self):
      pass

  def load_simulation(self, filename):
      pass
      
  def run_simulation(self):
      pass

if __name__ == '__main__':
    my_car = Car()
    my_car.load_simulation("simulation.txt")
    my_car.run_simulation()

```

# The Commands for simulation.txt

```
FORWARD
ACCELERATE
RIGHT
ACCELERATE
RIGHT
ACCELERATE
RIGHT
ACCELERATE
LEFT
ACCELERATE
LEFT
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
REVERSE
ACCELERATE

```
