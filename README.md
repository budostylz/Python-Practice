# Data Structures

[Python 3.8.4rc1 documentation](https://docs.python.org/3/)



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