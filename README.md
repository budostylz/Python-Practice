# Data Types and Operators

[Python 3.8.4rc1 documentation](https://docs.python.org/3/)

[Bitwise Operators](https://wiki.python.org/moin/BitwiseOperators)

[Order of Operations](http://mathforum.org/dr.math/faq/faq.order.operations.html)

[Reserved Words](https://pentangle.net/python/handbook/node52.html)

[Python Operators](https://www.programiz.com/python-programming/operators)

[Keywords](https://docs.python.org/3/reference/lexical_analysis.html#keywords)

[https://docs.python.org/3/tutorial/floatingpoint.html](https://docs.python.org/3/tutorial/floatingpoint.html)

[PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)

[linter-python-pep8 package](https://atom.io/packages/linter-python-pep8)

[Why is 80 characters the 'standard' limit for code width?](https://softwareengineering.stackexchange.com/questions/148677/why-is-80-characters-the-standard-limit-for-code-width)

[Errors and Exceptions](https://docs.python.org/3/tutorial/errors.html)

[How George Boole’s zeroes and ones changed the world](https://www.irishtimes.com/news/science/how-george-boole-s-zeroes-and-ones-changed-the-world-1.2014673)

[Format String Syntax](https://docs.python.org/3.6/library/string.html#format-string-syntax)

[String Methods](https://docs.python.org/3/library/stdtypes.html#string-methods)

[HackerRank](https://www.hackerrank.com/domains/python)

[codewars](https://www.codewars.com/users/sign_in)


![Binary](https://github.com/budostylz/Python-Practice/blob/Data_Types_and_Operators/binary.jpg)



```python
# Write an expression that calculates the average of 23, 32 and 64
# Place the expression in this print statement
print((23 + 32 + 64) / 3)
# 39.666666666666664

# Fill this in with an expression that calculates how many tiles are needed.
print( (9*7) + (5*7) )
#print('Total number of tiles in package ', 6 * 17)

# Fill this in with an expression that calculates how many tiles will be left over.
print( (6 * 17) - ( (9*7) + (5*7)) )


sf_population, sf_area = 864816, 231.89
rio_population, rio_area = 6453682, 486.5

san_francisco_pop_density = sf_population/sf_area
rio_de_janeiro_pop_density = rio_population/rio_area

# Write code that prints True if San Francisco is denser than Rio, and False otherwise
print(san_francisco_pop_density > rio_de_janeiro_pop_density)

# TODO: Fix this string!
ford_quote = 'Whether you think you can, or you think you can\'t--you\'re right.'

username = "Kinari"
timestamp = "04:50"
url = "http://petshop.com/pets/mammals/cats"

# TODO: print a log message using the variables above.
# The message should have the same format as this one:
# "Yogesh accessed the site http://petshop.com/pets/reptiles/pythons at 16:20."

message = username + " accessed the site " + url + " at " + timestamp + "."
print(message)

given_name = "William"
middle_names = "Bradley"
family_name = "Pitt"
full_name = given_name + " " +  middle_names + " " + family_name


name_length = len(given_name + middle_names + family_name) + 2#spaces


# Now we check to make sure that the name fits within the driving license character limit
# Nothing you need to do here
driving_license_character_limit = 28
print(name_length <= driving_license_character_limit)


mon_sales = "121"
tues_sales = "105"
wed_sales = "110"
thurs_sales = "98"
fri_sales = "95"


#TODO: Print a string with this format: This week's total sales: xxx
# You will probably need to write some lines of code before the print statement.

total_sales = str(int(mon_sales) + int(tues_sales) + int(wed_sales) + int(thurs_sales) + int(fri_sales))

message = "This week's total sales: " + str(total_sales)
print(message)





```
