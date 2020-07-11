# Control Flow

[Python 3.8.4rc1 documentation](https://docs.python.org/3/)

[Python Reference](https://www.w3schools.com/python/python_reference.asp)

[Python Style Guide](https://www.python.org/dev/peps/pep-0008/#tabs-or-spaces)


## Conditional Statements

```python

if phone_balance < 5:
    phone_balance += 10
    bank_balance -= 10

if season == 'spring':
    print('plant the garden!')
elif season == 'summer':
    print('water the garden!')
elif season == 'fall':
    print('harvest the garden!')
elif season == 'winter':
    print('stay indoors!')
else:
    print('unrecognized season')


points = 151

if points <= 50:
    result = "Congratulations! You won a wooden rabbit!"
elif points <= 150:
    result = "Oh dear, no prize this time."
elif points <= 180:
    result = "Congratulations! You won a wafer-thin mint!"
else:
    result = "Congratulations! You won a penguin!"

print(result)

# '''
# You decide you want to play a game where you are hiding 
# a number from someone.  Store this number in a variable 
# called 'answer'.  Another user provides a number called
# 'guess'.  By comparing guess to answer, you inform the user
# if their guess is too high or too low.

# Fill in the conditionals below to inform the user about how
# their guess compares to the answer.
# '''
answer = 5
guess = 6

if guess < answer:
    result = "Oops!  Your guess was too low."
elif guess > answer:
    result = "Oops!  Your guess was too high."
elif guess == answer:
    result = "Nice!  Your guess matched the answer!"

print(result)



# '''
# Depending on where an individual is from we need to tax them 
# appropriately.  The states of CA, MN, and 
# NY have taxes of 7.5%, 9.5%, and 8.9% respectively.
# Use this information to take the amount of a purchase and 
# the corresponding state to assure that they are taxed by the right
# amount.
# '''
state = 'MN'
purchase_amount = 1000

if state == 'CA':
    tax_amount = .075
    total_cost = purchase_amount*(1+tax_amount)
    result = "Since you're from {}, your total cost is {}.".format(state, total_cost)

elif state == 'MN':
    tax_amount = .095
    total_cost = purchase_amount*(1+tax_amount)
    result = "Since you're from {}, your total cost is {}.".format(state, total_cost)

elif state == 'NY':
    tax_amount = .089
    total_cost = purchase_amount*(1+tax_amount)
    result = "Since you're from {}, your total cost is {}.".format(state, total_cost)

print(result)


```

![truthy](https://github.com/budostylz/Python-Practice/blob/Control_Flow/truthy.PNG)


## Complex Boolean Expressions

```python

if 18.5 <= weight / height**2 < 25:
    print("BMI is considered 'normal'")

if is_raining and is_sunny:
    print("Is there a rainbow?")

if (not unsubscribed) and (location == "USA" or location == "CAN"):
    print("send email")



errors = 3
if errors:
    print("You have {} errors to fix!".format(errors))
else:
    print("No errors to fix!")

    points = 174



points = 174  # use this input when submitting your answer

# set prize to default value of None
prize = None

# use the value of points to assign prize to the correct prize name
if points <= 50:
    prize = "wooden rabbit"
elif 151 <= points <= 180:
    prize = "wafer-thin mint"
elif points >= 181:
    prize = "penguin"

# use the truth value of prize to assign result to the correct message
if prize:
    result = "Congratulations! You won a {}!".format(prize)
else:
    result = "Oh dear, no prize this time."

print(result)


```

## For Loops

```python

cities = ['new york city', 'mountain view', 'chicago', 'los angeles']
for city in cities:
    print(city)
print("Done!")

for i in range(3):
    print("Hello!")

#Hello
#Hello
#Hello

#range(start=0, stop, step=1)

    #The range() function takes three integer arguments, the first and third of which are optional:

    #The 'start' argument is the first number of the sequence. If unspecified, 'start' defaults to 0.
    #The 'stop' argument is 1 more than the last number of the sequence. This argument must be specified.
    #The 'step' argument is the difference between each number in the sequence. If unspecified, 'step' defaults to 1.

#Notes on using range():

    #If you specify one integer inside the parentheses withrange(), it's used as the value for 'stop,' and the defaults are used for the other two.
    #e.g. - range(4) returns 0, 1, 2, 3
    #If you specify two integers inside the parentheses withrange(), they're used for 'start' and 'stop,' and the default is used for 'step.'
    #e.g. - range(2, 6) returns 2, 3, 4, 5
    #Or you can specify all three integers for 'start', 'stop', and 'step.'
    #e.g. - range(1, 10, 2) returns 1, 3, 5, 7, 9


# Creating a new list
cities = ['new york city', 'mountain view', 'chicago', 'los angeles']
capitalized_cities = []

for city in cities:
    capitalized_cities.append(city.title())

# Update list
cities = ['new york city', 'mountain view', 'chicago', 'los angeles']

for index in range(len(cities)):
    cities[index] = cities[index].title()

# Write a for loop below that will print out every whole number that is a multiple of 5 and less than or equal to 30.
for i in range(5, 35, 5):
    print(i)

#5
#10
#15
#20
#25
#30


names = ["Joey Tribbiani", "Monica Geller", "Chandler Bing", "Phoebe Buffay"]
usernames = []

# write your for loop here
for username in names:
    username = username.replace(' ', '_').lower()
    usernames.append(username)

print(usernames)


usernames = ["Joey Tribbiani", "Monica Geller", "Chandler Bing", "Phoebe Buffay"]

# write your for loop here
for i in range(len(usernames)):
    usernames[i] = usernames[i].replace(' ', '_').lower()


print(usernames)


items = ['first string', 'second string']
html_str = "<ul>\n"          # The "\n" here is the end-of-line char, causing
                             # chars after this in html_str to be on next line

for item in items:
    html_str += "<li>{}</li>\n".format(item)
html_str += "</ul>"

print(html_str)

#<ul>
#<li>first string</li>
#<li>second string</li>
#</ul>

```
