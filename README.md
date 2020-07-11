# Data Structures

[Python 3.8.4rc1 documentation](https://docs.python.org/3/)

## List

```python

# Use list indexing to determine how many days are in a particular month based on the integer variable month, and store that value in the integer variable num_days. For example, if month is 8, num_days should be set to 31, since the eighth month, August, has 31 days.#

# Remember to account for zero-based indexing!

month = 8
days_in_month = [31,28,31,30,31,30,31,31,30,31,30,31]

# use list indexing to determine the number of days in month
num_days = days_in_month[month-1]

print(num_days)

# Select the three most recent dates from this list using list slicing notation. Hint: negative indexes work in slices!
eclipse_dates = ['June 21, 2001', 'December 4, 2002', 'November 23, 2003',
                 'March 29, 2006', 'August 1, 2008', 'July 22, 2009',
                 'July 11, 2010', 'November 13, 2012', 'March 20, 2015',
                 'March 9, 2016']
                 
                 
# TODO: Modify this line so it prints the last three elements of the list
print(eclipse_dates[-3:])

# What would the output of the following code be? (Treat the comma in the multiple choice answers as newlines.)
a = [1, 5, 8]
b = [2, 6, 9, 10]
c = [100, 200]

print(max([len(a), len(b), len(c)]))
print(min([len(a), len(b), len(c)]))

# What would the output of the following code be? (Treat the comma in the multiple choice answers as newlines.)
names = ["Carol", "Albert", "Ben", "Donna"]
print(" & ".join(sorted(names)))

# What would the output of the following code be? (Treat the commas in the multiple choice answers as newlines.)
names = ["Carol", "Albert", "Ben", "Donna"]
names.append("Eugenia")
print(sorted(names))

arr = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
print(arr[2:6])
print(arr[:3])
print(arr[4:])
print(arr[len(arr)-1])


```

## Tuples

```python
# Tuples
dimensions = 52, 40, 100
length, width, height = dimensions # Tuple Unpacking
print("The dimensions are {} x {} x {}".format(length, width, height))

length, width, height = 52, 40, 100
print("The dimensions are {} x {} x {}".format(length, width, height))

tuple_a = 1, 2
tuple_b = (1, 2)

print(tuple_a == tuple_b)
print(tuple_a[1])


```

## Sets

```python

# Sets
numbers = [1, 2, 6, 3, 1, 1, 6]
unique_nums = set(numbers)
print(unique_nums)


fruit = {"apple", "banana", "orange", "grapefruit"}  # define a set

print("watermelon" in fruit)  # check for element

fruit.add("watermelon")  # add an element
print(fruit)

print(fruit.pop())  # remove a random element
print(fruit)

```

## Dictionary

```python

# Dictionaries And Identity Operators
elements = {"hydrogen": 1, "helium": 2, "carbon": 6}

print(elements["helium"])  # print the value mapped to "helium"
elements["lithium"] = 3  # insert "lithium" with a value of 3 into the dictionary

n = elements.get("dilithium")
print(n is None)
print(n is not None)

# Define a Dictionary, population,
# that provides information
# on the world's largest cities.
# The key is the name of a city
# (a string), and the associated
# value is its population in
# millions of people.

#   Key     |   Value
# Shanghai  |   17.8
# Istanbul  |   13.3
# Karachi   |   13.0
# Mumbai    |   12.5

population = {
    "Shanghai": 17.8,
    "Istanbul": 13.3,
    "Karachi": 13.0,
    "Mumbai": 12.5
    
}

print(population)

#get with a Default Value
#Dictionaries have a related method that's also useful, get(). get() looks up values in a dictionary, but unlike looking up #values with square brackets, get() returns None (or a default value of your choice) if the key isn't found. If you expect #lookups to sometimes fail, get() might be a better tool than normal square bracket lookups.

elements.get('dilithium')
#None

elements['dilithium']
#KeyError: 'dilithium'

elements.get('kryptonite', 'There\'s no such element!')
"There's no such element!"


```

## Compound Data Structures

```python

elements = {"hydrogen": {"number": 1,
                         "weight": 1.00794,
                         "symbol": "H"},
              "helium": {"number": 2,
                         "weight": 4.002602,
                         "symbol": "He"}}


helium = elements["helium"]  # get the helium dictionary
hydrogen_weight = elements["hydrogen"]["weight"]  # get hydrogen's weight

oxygen = {"number":8,"weight":15.999,"symbol":"O"}  # create a new oxygen dictionary 
elements["oxygen"] = oxygen  # assign 'oxygen' as a key to the elements dictionary
print('elements = ', elements)



#Output

elements =  {"hydrogen": {"number": 1,
                          "weight": 1.00794,
                          "symbol": 'H'},
               "helium": {"number": 2,
                          "weight": 4.002602,
                          "symbol": "He"}, 
               "oxygen": {"number": 8, 
                          "weight": 15.999, 
                          "symbol": "O"}}

```
