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


Creating loop while loop

x=0
while(x<5):
    print(x)
    x=x+1

Creating 
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


Work;;;; 

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
