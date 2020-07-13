# Advance Topics

[Python 3.8.4rc1 documentation](https://docs.python.org/3/)

[Python Reference](https://www.w3schools.com/python/python_reference.asp)

[Python Style Guide](https://www.python.org/dev/peps/pep-0008/#tabs-or-spaces)

[Iterators](https://docs.python.org/3/tutorial/classes.html#iterators)

[When should I use a generator and when a list in Python? [duplicate]](https://softwareengineering.stackexchange.com/questions/290231/when-should-i-use-a-generator-and-when-a-list-in-python/290235)

[How do you split a list into evenly sized chunks?](https://stackoverflow.com/questions/312443/how-do-you-split-a-list-into-evenly-sized-chunks)

![Generator Expressions](https://github.com/budostylz/Python-Practice/blob/Advance_Topics/generator_expression.PNG)

## Iterators And Generators


```python


"""

Iterators And Generators
Iterables are objects that can return one of their elements at a time, such as a list. Many of the built-in functions we’ve used so far, like 'enumerate,' return an iterator.

An iterator is an object that represents a stream of data. This is different from a list, which is also an iterable, but is not an iterator because it is not a stream of data.

Generators are a simple way to create iterators using functions. You can also define iterators using classes.

Here is an example of a generator function called my_range, which produces an iterator that is a stream of numbers from 0 to (x - 1).



"""

def my_range(x):
    i = 0
    while i < x:
        yield i
        i += 1


"""

Notice that instead of using the return keyword, it uses yield. This allows the function to return values one at a time, and start where it left off each time it’s called. This yield keyword is what differentiates a generator from a typical function.

Remember, since this returns an iterator, we can convert it to a list or iterate through it in a loop to view its contents. For example, this code:



"""

for x in my_range(5):
    print(x)

"""
Output
0
1
2
3
4
"""


lessons = ["Why Python Programming", "Data Types and Operators", "Control Flow", "Functions", "Scripting"]

def my_enumerate(iterable, start=0):
    count = start
    for element in iterable:
        yield count, element
        count += 1

for i, lesson in my_enumerate(lessons, 1):
    print("Lesson {}: {}".format(i, lesson))

"""
Output
Lesson 1: Why Python Programming
Lesson 2: Data Types and Operators
Lesson 3: Control Flow
Lesson 4: Functions
Lesson 5: Scripting
"""


def chunker(iterable, size):
    """Yield successive chunks from iterable of length size."""
    for i in range(0, len(iterable), size):
        yield iterable[i:i + size]

for chunk in chunker(range(25), 4):
    print(list(chunk))


"""

Output

[0, 1, 2, 3]
[4, 5, 6, 7]
[8, 9, 10, 11]
[12, 13, 14, 15]
[16, 17, 18, 19]
[20, 21, 22, 23]
[24]


"""


```

