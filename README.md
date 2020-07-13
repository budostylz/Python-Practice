# Functions

[Python 3.8.4rc1 documentation](https://docs.python.org/3/)

[Python Reference](https://www.w3schools.com/python/python_reference.asp)

[Python Style Guide](https://www.python.org/dev/peps/pep-0008/#tabs-or-spaces)

[PEP 257 -- Docstring Conventions](https://www.python.org/dev/peps/pep-0257/)

[Jack Diederich - HOWTO Write a Function - PyCon 2018](https://www.youtube.com/watch?v=rrBJVMyD-Gs&feature=youtu.be)

[Improve Your Python: 'yield' and Generators Explained](https://jeffknupp.com/blog/2013/04/07/improve-your-python-yield-and-generators-explained/)

## Defining Functions

```python

def cylinder_volume(height, radius):
    pi = 3.14159
    return height * pi * radius ** 2


cylinder_volume(10, 3) #call



# this prints something, but does not return anything
def show_plus_ten(num):
    print(num + 10)

# this returns something
def add_ten(num):
    return(num + 10)

print('Calling show_plus_ten...')
return_value_1 = show_plus_ten(5)
print('Done calling')
print('This function returned: {}'.format(return_value_1))

print('\nCalling add_ten...')
return_value_2 = add_ten(5)
print('Done calling')
print('This function returned: {}'.format(return_value_2))


#Output
#Calling show_plus_ten...
#15
#Done calling
#This function returned: None

#Calling add_ten...
#Done calling
#This function returned: 15

```

## Default Arguments

```python

# We can add default arguments in a function to have default values for parameters that are unspecified in a function call.

def cylinder_volume(height, radius=5):
    pi = 3.14159
    return height * pi * radius ** 2


cylinder_volume(10, 7)  # pass in arguments by position
cylinder_volume(height=10, radius=7)  # pass in arguments by name


def population_density(population, land_area):
    return population/land_area

# test cases for your function
test1 = population_density(10, 1)
expected_result1 = 10
print("expected result: {}, actual result: {}".format(expected_result1, test1))

test2 = population_density(864816, 121.4)
expected_result2 = 7123.6902801
print("expected result: {}, actual result: {}".format(expected_result2, test2))

#Output
#expected result: 10, actual result: 10.0
#expected result: 7123.6902801, actual result: 7123.690280065897

def readable_timedelta(days):
    # use integer division to get the number of weeks
    weeks = days // 7
    # use % to get the number of days that remain
    remainder = days % 7
    return "{} week(s) and {} day(s).".format(weeks, remainder)

# test your function
print(readable_timedelta(10))

# Output
#1 week(s) and 3 day(s).

```

## Variable Scope

```python

egg_count = 0

def buy_eggs():
    egg_count += 12 # purchase a dozen eggs

buy_eggs()

# Output
#UnboundLocalError

# Better Way
egg_count = 0

def buy_eggs(count):
    return count + 12  # purchase a dozen eggs

egg_count = buy_eggs(egg_count)



```
## Documentation

```python

# Single Line Docstring
def population_density(population, land_area):
    """Calculate the population density of an area. """
    return population / land_area

#Multi-Line Docstring
def population_density(population, land_area):
    """Calculate the population density of an area.

    INPUT:
    population: int. The population of that area
    land_area: int or float. This function is unit-agnostic, if you pass in values in terms
    of square km or square miles the function will return a density in those units.

    OUTPUT: 
    population_density: population / land_area. The population density of a particular area.
    """
    return population / land_area




```

## Lambda Expressions

```python

#Non-Lambda
def multiply(x, y):
    return x * y


## Lambda
multiply = lambda x, y: x * y

multiply(4, 7)


"""

Components of a Lambda Function
    1. The lambda keyword is used to indicate that this is a lambda expression.

    2. Following lambda are one or more arguments for the anonymous function separated by commas, followed by a colon :. Similar to functions, the way the arguments are named in a lambda expression is arbitrary.

    3. Last is an expression that is evaluated and returned in this function. This is a lot like an expression you might see as a return statement in a function.


    With this structure, lambda expressions aren’t ideal for complex functions, but can be very useful for short, simple functions.

"""






```


## Lambda with Map

```python

# Non-Lambda
numbers = [
              [34, 63, 88, 71, 29],
              [90, 78, 51, 27, 45],
              [63, 37, 85, 46, 22],
              [51, 22, 34, 11, 18]
           ]

def mean(num_list):
    return sum(num_list) / len(num_list)

averages = list(map(mean, numbers))
print(averages)

# Lambda
numbers = [
              [34, 63, 88, 71, 29],
              [90, 78, 51, 27, 45],
              [63, 37, 85, 46, 22],
              [51, 22, 34, 11, 18]
           ]

averages = list(map(lambda x: sum(x) / len(x), numbers))
print(averages)

#Output
[57.0, 58.2, 50.6, 27.2]



```


## Lambda with Filter

```python

# Non-Lambda
cities = ["New York City", "Los Angeles", "Chicago", "Mountain View", "Denver", "Boston"]

def is_short(name):
    return len(name) < 10

short_cities = list(filter(is_short, cities))
print(short_cities)

# Lambda
cities = ["New York City", "Los Angeles", "Chicago", "Mountain View", "Denver", "Boston"]

short_cities = list(filter(lambda x: len(x) < 10, cities))
print(short_cities)

['Chicago', 'Denver', 'Boston']


```