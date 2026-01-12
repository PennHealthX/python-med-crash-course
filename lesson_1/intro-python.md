# Introduction to Python Programming

Welcome to your first programming lesson! This guide will introduce you to Python in a friendly, approachable way. No prior coding experience needed.

## What is Coding?

Think of coding like giving instructions to a very literal friend. When you tell a friend to "make a sandwich," they understand all the implied steps because they have common sense and life experience. A computer, however, needs every single step spelled out explicitly:

1. Get two slices of bread
2. Open the peanut butter jar
3. Use a knife to spread peanut butter on one slice
4. And so on...

**Coding** (also called programming) is the process of writing these step-by-step instructions in a language that computers can understand. Just like humans speak different languages (English, Spanish, Mandarin), computers have programming languages. Python is one of the most popular and beginner-friendly programming languages.

### Why Python?

Python was designed to be readable and straightforward. Compare these two ways of saying the same thing:

**In plain English:** "Print the words 'Hello, World!' to the screen"

**In Python:** `print("Hello, World!")`

See? It's almost like English! This is why Python is perfect for beginners.

## Your First Program: Hello, World!

In the programming world, there's a tradition: the first program you write in any new language should display the text "Hello, World!" It's a simple way to verify that everything is working correctly.

### Writing Hello, World!

Here's your first Python program:

```python
print("Hello, World!")
```

That's it! Just one line. Let's break down what's happening:

- **`print()`** is a built-in function (a pre-written instruction) that displays text on the screen
- The **parentheses `()`** are where you put the information you want to print
- **`"Hello, World!"`** is the text you want to display (the quotation marks tell Python this is text, not code)

### Try It Yourself

When you run this code, you should see:
```
Hello, World!
```

You can change the text to anything you want:

```python
print("Welcome to Python!")
print("My name is Danny Devito")
print("I'm learning to code!")
```

Each `print()` statement will display its text on a new line.

## Understanding the Basics

### Comments: Notes to Yourself

Sometimes you want to write notes in your code to explain what you're doing. These notes are called **comments**, and Python ignores them when running your program. Use the `#` symbol:

```python
# This is a comment - Python will ignore this line
print("But Python will run this line!")

print("Hello!")  # You can also put comments at the end of lines
```

Comments are incredibly useful for explaining your thought process, especially when you come back to code later and wonder "what was I thinking here?"

### Variables: Storing Information

Imagine you have a box where you can store information and give it a label. In programming, these boxes are called **variables**.

```python
name = "Maria"
age = 25
is_student = True
```

Here's what's happening:
- **`name`** is a variable storing the text "Maria"
- **`age`** is a variable storing the number 25
- **`is_student`** is a variable storing True (a yes/no value)

The `=` sign doesn't mean "equals" like in math - it means "store this value in this variable."

You can use variables in your print statements:

```python
name = "Maria"
print("Hello, my name is")
print(name)
```

Or combine them more elegantly:

```python
name = "Maria"
print("Hello, my name is " + name)
```

### Types of Data

Python works with different types of data:

**1. Strings (Text)**
```python
greeting = "Hello, World!"
favorite_color = "blue"
```
Strings are always wrapped in quotation marks (either `"` or `'`).

**2. Numbers**
```python
age = 25              # Integer (whole number)
temperature = 98.6    # Float (decimal number)
```

**3. Booleans (True/False)**
```python
is_raining = True
is_sunny = False
```

**4. None (Nothing/Empty)**
```python
middle_name = None    # Used when there's no value
```

## Simple Math Operations

Python can do math just like a calculator:

```python
# Basic arithmetic
print(5 + 3)      # Addition: 8
print(10 - 4)     # Subtraction: 6
print(6 * 7)      # Multiplication: 42
print(15 / 3)     # Division: 5.0
print(10 // 3)    # Integer division (no decimals): 3
print(10 % 3)     # Remainder: 1
print(2 ** 3)     # Exponent (2 to the power of 3): 8
```

You can also do math with variables:

```python
apples = 5
oranges = 3
total_fruit = apples + oranges
print(total_fruit)  # Prints: 8
```

## Getting User Input

Want to make your program interactive? Use `input()` to ask the user questions:

```python
name = input("What is your name? ")
print("Nice to meet you, " + name + "!")
```

When you run this program:
1. It displays "What is your name? " and waits
2. The user types their name and presses Enter
3. The program stores their answer in the `name` variable
4. It prints a personalized greeting

### A Complete Example

Let's put everything together:

```python
# A simple greeting program
print("Welcome to the Python Greeter!")
print()  # This prints a blank line

# Get user information
name = input("What is your name? ")
age = input("How old are you? ")
favorite_color = input("What is your favorite color? ")

# Display a personalized message
print()
print("Hello, " + name + "!")
print("You are " + age + " years old.")
print("I also think " + favorite_color + " is a great color!")
```

## Practice Exercises

Try these on your own to reinforce what you've learned:

1. **Personal Introduction**: Write a program that prints 5 sentences about yourself.

2. **Simple Calculator**: Create variables for two numbers, then print their sum, difference, product, and quotient.

3. **Favorite Things**: Ask the user for their favorite food, movie, and book, then print a summary message.

4. **Temperature Converter**: Ask the user for a temperature in Fahrenheit, convert it to Celsius using the formula `(F - 32) * 5/9`, and display the result. (Hint: you'll need to convert the input to a number first!)

## Key Takeaways

- **Coding** is giving step-by-step instructions to a computer
- **Python** is a beginner-friendly programming language
- **`print()`** displays information on the screen
- **Variables** store data that you can use later
- **`input()`** lets you ask users for information
- **Comments** (using `#`) help you document your code

## What's Next?

In the next lesson, we'll learn about:
- Making decisions with if/else statements
- Repeating actions with loops
- Organizing code with functions
- Working with lists of data

Congratulations on writing your first Python programs! Every expert programmer started exactly where you are now.