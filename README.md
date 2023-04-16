# Working-with-Python


## Building  rolling dice with Python.

import random

def roll_dice():
    print("Rolling the dice...")
    return random.randint(1, 6)

    print ("Welcome to my dice rolling stimulator!")
while True:
    input('press enter to roll the dice, or type quit to quit')
    dice_result = roll_dice()
    print("you are a", dice_result)
