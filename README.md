# Custom Functions and Plotting in Python

## Additional Resources

- [Python Documentation on Defining Functions](https://docs.python.org/3/tutorial/controlflow.html#defining-functions)

## Assignment

## Python Custom Functions

The core Python library and optional modules contain a huge number of useful functions. However, as you write more specialized code, you will inevitably need/want to use a function that doesn't yet exist. Thankfully, Python and other programming languages make it easy to write your own custom functions. Any time you find yourself writing the same block of code repeatedly, you should instead put this code in a new function that can be called whenever needed. Writing your own functions makes your code shorter, more readable, more reliable, and easier to debug. The general syntax for defining a custom function looks like this

```
def myNewFunction():
    """ A text description of my function goes here."""
    
    print("Executing a custom function!")
```

The `def` keyword tells Python that we're defining a new function. That is followed by the name of our function (in this case, `myNewFunction`). The function name is then _always_ followed by parentheses - `()`. For simple functions, nothing needs to go inside the parentheses. These are then followed by a colon - `:`.

The next line should be indented and a text string should be provided inside sets of three double quotation marks - `"""`. This text is known as the _docstring_ and provides users, other programmers, or, more likely, you at some later time, with useful information about the function. Executing `help(myNewFunction)` in the Python interpreter will cause the _docstring_ to be printed for the user.

The rest of code relevant to your function should appear on subsequent indented lines after the _docstring_. Simple functions may only have 1 or 2 lines. More complicated functions may have 10s to 100s of lines. However, if the function gets much longer than that, it's probably an indication that you need to break the code up into more functions of a manageable size.

Custom functions are executed just like any core Python function. Simply type the function's name, followed by parentheses.

`myNewFunction()`

### Function Arguments

To make functions more flexible, they can be written to accept arguments. To do this, simply include a new variable name inside the parentheses when defining the function. Note that this variable name _only has meaning within the function's code_. More formally, we say that the scope of the variable is limited to the function.

```
def myFuncWithArg(userProvidedWord):
    """This example function shows how to accept and use arguments."""
    
    print("I am printing the word: %s" % userProvidedWord)

myFuncWithArg("test")
myFuncWithArg("tigers")
```

Note in the example above how we used the new variable name in the function's code, while the value of this variable changed depending on what string the user provided each time they executed the function.

Functions can take more than one argument, as long as they are specified in the function definition.

```
def complexMathThing(numOne,numTwo,numThree):
    """A complicated mathematical operation with three numbers."""

    print( pow(numOne, numTwo) - numThree )
    
complexMathThing(4,5,2)
```

### Return Statements

In the example above, the function accomplished a task (printing something to the screen), but nothing produced by this function could be saved in a variable to be used later. If we want a function to produce a value (integer, float, string, ...) that can be saved in a variable, we need to include a `return` statement. This statement defines what value a function will produce.

Here, we redefine the function above to `return` the same value that it printed before.

```
def complexMathThing(numOne,numTwo,numThree):
    """A complicated mathematical operation with three numbers."""

    return pow(numOne, numTwo) - numThree

myVar = complexMathThing(4,5,2)
```

By adding a `return` statement, we can save a value produced by the function `complexMathThing()` in a variable (in this case, `myVar`)for future use.

```
print(myVar)
myVar * 3
```

### Optional Arguments



