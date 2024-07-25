# Global Variables

<p align="center">
<img src="/docs/assets/globalVariables.jpg">
</p>

Global variables sit outside of classes and functions, therefore they are not a good way to access data. They are rarely used in programming. However, we will be using them in this beginner program. 

Each variable is an integer and is used to change direction or place the car in forward or reverse. 

They are seen in the iamge above.

This allows for readability. for example

```py
    if speed >= FORWARD:
        # The car speed is greater than or equal to 1
        # but it also says: if the car is going forward...
    if speed <= REVERSE:
        # The car speed is less than or equal to 0 
        # or: if the car is going backwards...
```    
This allows other deverlopers to understand what your code does.

This applies to the LEft and Right variables.

```py
    if commands[i] == "LEFT":
        change-direction(LEFT)
        # if the command says to turn left - change direction to the left.

    if commands[i] == "RIGHT":
        change-direction(RIGHT)
        # if the command says to turn right - change direction to the right.
    
```

