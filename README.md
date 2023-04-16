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

## Moving all images from download folder into a new folder called New

import os
import shutil

# set the path to the Downloads folder on your Mac
downloads_path = os.path.expanduser("~/Downloads")

# set the path to the new folder on your desktop
new_folder_path = os.path.expanduser("~/Desktop/new")

# create the new folder if it doesn't already exist
if not os.path.exists(new_folder_path):
    os.mkdir(new_folder_path)

# loop through all the files in the Downloads folder
for filename in os.listdir(downloads_path):
    # check if the file is an image (JPG, PNG, GIF)
    if filename.endswith(('.jpg', '.jpeg', '.png', '.gif')):
        # set the path to the file in the Downloads folder
        file_path = os.path.join(downloads_path, filename)
        # set the path to the file in the new folder
        new_file_path = os.path.join(new_folder_path, filename)
        # move the file to the new folder
        shutil.move(file_path, new_file_path)

## Defining function and calling a function using 
If, elif and else functions; 

def school_age_calculator (age,name):
    if age < 5:
        print("enjoy the time!", name, "is only", age)
    elif age == 5:
        print("enjoy kinda", name)
    else:
        print("they grow fast")

school_age_calculator(5, "thomas")

How to get parameter back, or value back from a function:
Example what would be ya age in 10years?

def add_ten_to_age(age):
    new_age = age + 10
    return new_age

How_old_will_i_Be = add_ten_to_age(7)
print(How_old_will_i_Be, "years old")


## Creating loop while loop

x=0
while(x<5):
    print(x)
    x=x+1

## Creating 
For loop

for X in range(5,10):
    print(X)

days=["mond","tues", "wed"]
for d in days:
    print(d)

## this print mon only and stop, that break print .
days=["mond","tues", "wed"]
for d in days:
    if (d== "tues"):break
    print(d)

## this breaks tues only but start and continue by skipping tues only.
days=["mond","tues", "wed"]
for d in days:
    if (d== "tues"):continue
    print(d)

## calculator 

first = input("Fisrt: ")
second = input("Second: ")
sum =float(first) + float(second)
print(sum + str(sum) )

temperature = 9
if temperature > 30:
    print("it's is a hot day")
    print("drink plenty water")
elif temperature > 20:
    print('its a nice day')
elif temperature > 10:
    print("it is cold day")
else:
    print('its is cold')

## kg and lbs

weight = int(input("weight: "))
    unit = input('(K)g or (K)bps: ')
    if unit.upper() == "K":
        converted = weight/0.45
        print('weight in Lbs: + str(converted'))
    else:
        converted = weight * 0.45
        print('weight in Kgs: ' + str(converted))

## the imports file to start pandas tutorial 

from urllib.request import urlretrieve
italy_covid_url = 'https://gist.githubusercontent.com/aakashns/f6a004fa20c84fec53262f9a8bfee775/raw/f309558b1cf5103424cef58e2ecb8704dcd4d74c/italy-covid-daywise.csv'

urlretrieve(italy_covid_url, 'italy-covid-daywise.csv')
import pandas as pd
covid_df = pd.read_csv('italy-covid-daywise.csv')

## to retrieve specific row 
covid_df.loc[243]

## to retrieve column 
covid_df.at[243]
Or 
covid_df.new_names

## accessing multiple columns 
covid_df [‘name’, ‘work’]

## to access first and last rows
covid_df.head(5)
covid_df.tail(3)

## accessing row and column
covid_df[256, ‘new test’]

##acccessing row of ranges
covid_df.loc[200:400]


## Work;;;; 

total_cases = covid_df.new_cases.sum()
total_deaths = covid_df.new_deaths.sum()
print ({total_cases}, {total_deaths})



Q,
What is the overall death rate (ratio of reported death to reported cases

deaths_rate = covid_df.new_deaths.sum() / covid_df.new_cases.sum()
print('The overall death rate is {:.2f}%. ' .format(death_rate))

The overall death rate is 0.13%. 


## retrieving based on 
high_new_cases = covid_df[covid_df.new_cases >1000]

## sorting 
covid_df.sort_values('new_deaths', ascending=False).head(10)


## What is the age that 90% of the people are younger than?
#using percentile

import numpy

ages = [5,31,43,48,50,41,7,11,15,39,80,82,32,2,8,6,25,36,27,61,31]

x = numpy.percentile(ages, 90)

print(x)


## Create an array with 100000 random numbers, and display them using a histogram with 100 bars: 

import numpy
import matplotlib.pyplot as plt

x = numpy.random.uniform(0.0, 5.0, 250)

plt.hist(x, 5)
plt.show()

## A typical normal data distribution: using random.normal method

import numpy
import matplotlib.pyplot as plt

x = numpy.random.normal(5.0, 1.0, 100000)

plt.hist(x, 100)
plt.show()

## Use the scatter() method to draw a scatter plot diagram:
## What we can read from the diagram is that the two fastest cars 
## were both 2 years old, and the slowest car was 12 years old.

import matplotlib.pyplot as plt

x = [5,7,8,7,2,17,2,9,4,11,12,9,6]
y = [99,86,87,88,111,86,103,87,94,78,77,85,86]

plt.scatter(x, y)
plt.show()



