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

## What's Covered

This notebook will go over:
- print statements
- variables
- comments
- user input
- if statements
- for loops
- while loops
- functions

## Your First Program: Hello, World!

In the programming world, there's a tradition: the first program you write in any new language should display the text "Hello, World!" It's a simple way to verify that everything is working correctly.

### Writing Hello, World!

Here's your first Python program:

```python
print("Hello, World!")
```

**Output:**
```
Hello, World!
```

That's it! Just one line. Let's break down what's happening:

- **`print()`** is a built-in function (a pre-written instruction) that displays text on the screen
- The **parentheses `()`** are where you put the information you want to print
- **`"Hello, World!"`** is the text you want to display (the quotation marks tell Python this is text, not code)

### Try It Yourself

You can change the text to anything you want:

```python
print("Welcome to Python!")
print("My name is Danny Devito")
print("I'm learning to code!")
```

**Output:**
```
Welcome to Python!
My name is Danny Devito
I'm learning to code!
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

**Output:**
```
But Python will run this line!
Hello!
```

Comments are incredibly useful for explaining your thought process, especially when you come back to code later and wonder "what was I thinking here?"

### Variables: Storing Information

Imagine you have a box where you can store information and give it a label. In programming, these boxes are called **variables**.

```python
name = "Maria"
age = 25
is_student = True

print(name)
print(age)
print(is_student)
```

**Output:**
```
Maria
25
True
```

Here's what's happening:
- **`name`** is a variable storing the text "Maria"
- **`age`** is a variable storing the number 25
- **`is_student`** is a variable storing True (a yes/no value)

The `=` sign doesn't mean "equals" like in math - it means "store this value in this variable."

You can use variables in your print statements:

```python
name = "Maria"
print("Hello, my name is " + name)
```

**Output:**
```
Hello, my name is Maria
```

### Types of Data

Python works with different types of data:

**1. Strings (Text)**

```python
greeting = "Hello, World!"
favorite_color = "blue"
print(greeting)
print(favorite_color)
```

**Output:**
```
Hello, World!
blue
```

Strings are always wrapped in quotation marks (either `"` or `'`).

**2. Numbers**

```python
age = 25              # Integer (whole number)
temperature = 98.6    # Float (decimal number)
print(age)
print(temperature)
```

**Output:**
```
25
98.6
```

**3. Booleans (True/False)**

```python
is_raining = True
is_sunny = False
print(is_raining)
print(is_sunny)
```

**Output:**
```
True
False
```

**4. None (Nothing/Empty)**

```python
middle_name = None    # Used when there's no value
print(middle_name)
```

**Output:**
```
None
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

**Output:**
```
8
6
42
5.0
3
1
8
```

You can also do math with variables:

```python
apples = 5
oranges = 3
total_fruit = apples + oranges
print(total_fruit)  # Prints: 8
```

**Output:**
```
8
```

## Getting User Input

Want to make your program interactive? Use `input()` to ask the user questions:

```python
name = input("What is your name? ")
print("Nice to meet you, " + name + "!")
```

**Example interaction:**
```
What is your name? Alice
Nice to meet you, Alice!
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

**Example interaction:**
```
Welcome to the Python Greeter!

What is your name? Alice
How old are you? 25
What is your favorite color? blue

Hello, Alice!
You are 25 years old.
I also think blue is a great color!
```

## Key Takeaways (Part 1)

- **Coding** is giving step-by-step instructions to a computer
- **Python** is a beginner-friendly programming language
- **`print()`** displays information on the screen
- **Variables** store data that you can use later
- **`input()`** lets you ask users for information
- **Comments** (using `#`) help you document your code

## Conditions and If-Statements

Sometimes, we only want to execute certain blocks of code if a condition is true. The basic format is as follows:

```
if [condition]:
    do something...
```

[condition] can take many forms. Commonly, it's a comparison between 2 variables.

### Comparison Operators

These operators let you compare values:

- `==` : equal to
- `!=` : not equal to
- `>` : greater than
- `<` : less than
- `>=` : greater than or equal to
- `<=` : less than or equal to

**Important:** Notice the **indentation** (spaces) before the print statements! In Python, indentation is crucial - it tells Python which lines belong inside the if statement.

```python
age = 20

if age >= 18:
    print("You are an adult!")
    print("You can vote!")

# This always runs, regardless of the if statement
print("Program complete")
```

**Output:**
```
You are an adult!
You can vote!
Program complete
```

```python
temperature = 75

if temperature > 80:
    print("It's hot outside!")

if temperature == 75:
    print("Perfect temperature!")

if temperature < 32:
    print("It's freezing!")
```

**Output:**
```
Perfect temperature!
```

The if condition can also just be a variable by itself. So, instead of writing:

```
var = True
if var == True:
    do something...
```

You can instead write
```
if var:
    do something...
```

This gets into the concept of truthy vs falsy values in Python. If you're interested in learning more, you can check out this [article](https://www.geeksforgeeks.org/python/truthy-vs-falsy-values-in-python/).

### If-Else: Handling Both Cases

What if you want to do one thing if a condition is true, and something different if it's false? Use `else`:

```python
age = 15

if age >= 18:
    print("You can vote!")
else:
    print("You're too young to vote yet.")
    print("You need to wait", 18 - age, "more years.")
```

**Output:**
```
You're too young to vote yet.
You need to wait 3 more years.
```

### If-Elif-Else: Multiple Conditions

When you have more than two possibilities, use `elif` (short for "else if"):

```python
grade = 85

if grade >= 90:
    print("You got an A!")
elif grade >= 80:
    print("You got a B!")
elif grade >= 70:
    print("You got a C!")
elif grade >= 60:
    print("You got a D.")
else:
    print("You got an F. Study harder!")
```

**Output:**
```
You got a B!
```

### Combining Conditions

You can check multiple conditions at once using `and` and `or`:

- `and` : both conditions must be true
- `or` : at least one condition must be true
- `not` : reverses a condition

```python
age = 25
has_license = True

# Using 'and' - both must be true
if age >= 16 and has_license:
    print("You can drive!")

# Using 'or' - at least one must be true
is_weekend = True
is_holiday = False

if is_weekend or is_holiday:
    print("You don't have to work today!")

# Using 'not'
is_raining = False
if not is_raining:
    print("It's a nice day - go outside!")
```

**Output:**
```
You can drive!
You don't have to work today!
It's a nice day - go outside!
```

## Repeating Actions: For Loops

Imagine you need to print "Hello" 100 times. You could write `print("Hello")` 100 times... or you could use a **loop** to do it automatically! Loops let you repeat code multiple times.

### For Loops: Repeating a Specific Number of Times

The `range()` function is commonly used with for loops to repeat something a specific number of times:

```python
# Print numbers 0 through 4
for i in range(5):
    print("Number:", i)

print("Loop finished!")
```

**Output:**
```
Number: 0
Number: 1
Number: 2
Number: 3
Number: 4
Loop finished!
```

**Note:** `range(5)` creates numbers from 0 to 4 (not 5!). Python starts counting from 0.

### Range with Start and Stop Values

You can specify where to start and stop:

```python
# Print numbers 1 through 10
for i in range(1, 11):
    print(i)

# Print even numbers from 0 to 10
for i in range(0, 11, 2):  # Third number is the "step"
    print(i)
```

**Output:**
```
1
2
3
4
5
6
7
8
9
10
0
2
4
6
8
10
```

### Looping Through Lists

Lists are collections of items. You can loop through each item:

```python
# Create a list of fruits
fruits = ["apple", "banana", "orange", "grape"]

# Loop through each fruit
for fruit in fruits:
    print("I like", fruit)

# Another example with numbers
numbers = [10, 20, 30, 40, 50]
for num in numbers:
    print(num * 2)  # Print each number doubled
```

**Output:**
```
I like apple
I like banana
I like orange
I like grape
20
40
60
80
100
```

### Practical Example: Calculating a Sum

```python
# Calculate the sum of numbers 1 to 10
total = 0

for i in range(1, 11):
    total = total + i
    print("After adding", i, "total is:", total)

print("Final sum:", total)
```

**Output:**
```
After adding 1 total is: 1
After adding 2 total is: 3
After adding 3 total is: 6
After adding 4 total is: 10
After adding 5 total is: 15
After adding 6 total is: 21
After adding 7 total is: 28
After adding 8 total is: 36
After adding 9 total is: 45
After adding 10 total is: 55
Final sum: 55
```

## While Loops: Repeating Until a Condition is Met

A **while loop** keeps running as long as a condition is true. It's like saying "keep doing this until something changes."

### Basic While Loop

```python
# Count from 1 to 5
count = 1

while count <= 5:
    print("Count is:", count)
    count = count + 1  # Very important! This changes the condition

print("Loop finished!")
```

**Output:**
```
Count is: 1
Count is: 2
Count is: 3
Count is: 4
Count is: 5
Loop finished!
```

**Warning:** If you forget to change the condition (like incrementing `count`), you'll create an **infinite loop** - the loop will never stop! Always make sure your loop has a way to end.

### When to Use While vs For Loops

- Use **for loops** when you know how many times to repeat
- Use **while loops** when you repeat until something happens

### Practical Example: Password Checker

```python
correct_password = "python123"
password = ""

# Keep asking until they get it right
while password != correct_password:
    password = input("Enter the password: ")
    if password != correct_password:
        print("Wrong password! Try again.")

print("Access granted!")
```

**Example interaction:**
```
Enter the password: hello
Wrong password! Try again.
Enter the password: test
Wrong password! Try again.
Enter the password: python123
Access granted!
```

### Using Break and Continue

Sometimes you need more control over your loops:

- `break` - exits the loop immediately
- `continue` - skips to the next iteration

```python
# Example using break - stop when we find what we're looking for
numbers = [1, 3, 5, 7, 10, 12, 14]

for num in numbers:
    if num % 2 == 0:  # If the number is even
        print("Found an even number:", num)
        break  # Stop the loop

print()

# Example using continue - skip certain items
for i in range(1, 11):
    if i % 2 == 0:  # If the number is even
        continue  # Skip to next iteration
    print(i)  # Only odd numbers get printed
```

**Output:**
```
Found an even number: 10

1
3
5
7
9
```

## Functions: Reusable Code Blocks

So far, we've been writing code that runs from top to bottom. But what if you want to use the same code multiple times? That's where **functions** come in!

A **function** is a reusable block of code that performs a specific task. Think of it like a recipe - you write it once, then you can use it whenever you need it.

### Creating Your First Function

Here's the basic structure of a function:

```python
def function_name():
    # Code goes here
    print("This is a function!")
```

Let's create a simple greeting function:

```python
# Define a function
def say_hello():
    print("Hello!")
    print("Welcome to Python functions!")

# Call the function (use it)
say_hello()

print()

# You can call it multiple times
say_hello()
say_hello()
```

**Output:**
```
Hello!
Welcome to Python functions!

Hello!
Welcome to Python functions!
Hello!
Welcome to Python functions!
```

### Functions with Parameters

Functions become much more useful when they can accept **parameters** (also called **arguments**). Parameters are values you pass into the function so it can work with different data.

Think of parameters like ingredients you give to a recipe - the recipe (function) stays the same, but you can use different ingredients each time.

```python
# Function with one parameter
def greet(name):
    print(f"Hello, {name}!")

# Call with different arguments
greet("Alice")
greet("Bob")
greet("Charlie")

print()

# Function with multiple parameters
def introduce(name, age):
    print(f"Hi, I'm {name} and I'm {age} years old.")

introduce("Maria", 25)
introduce("John", 30)
```

**Output:**
```
Hello, Alice!
Hello, Bob!
Hello, Charlie!

Hi, I'm Maria and I'm 25 years old.
Hi, I'm John and I'm 30 years old.
```

### Positional vs Keyword Arguments

There are two ways to pass values to function parameters:

1. **Positional arguments** - values are matched by position (order matters)
2. **Keyword arguments** - values are matched by name (order doesn't matter)

Keyword arguments use the format `parameter_name=value`, like `func(var=1)`.

```python
def create_profile(name, age, city):
    print(f"Name: {name}")
    print(f"Age: {age}")
    print(f"City: {city}")
    print()

# Using positional arguments - ORDER MATTERS!
create_profile("Alice", 25, "Boston")

# Using keyword arguments - order doesn't matter!
create_profile(name="Bob", age=30, city="Seattle")
create_profile(city="Austin", name="Charlie", age=28)  # Different order!

# You can mix both, but positional must come first
create_profile("Diana", age=22, city="Portland")
```

**Output:**
```
Name: Alice
Age: 25
City: Boston

Name: Bob
Age: 30
City: Seattle

Name: Charlie
Age: 28
City: Austin

Name: Diana
Age: 22
City: Portland
```

### Default Parameter Values

You can give parameters **default values** that are used if no argument is provided. This makes some parameters optional!

Default parameters must come after required parameters.

```python
def greet_with_title(name, title="Friend"):
    print(f"Hello, {title} {name}!")

# Using the default value for 'title'
greet_with_title("Alice")

# Providing a custom title (positional)
greet_with_title("Smith", "Dr.")

# Providing a custom title (keyword argument)
greet_with_title("Johnson", title="Professor")
greet_with_title(name="Brown", title="Captain")

print()

# Example with multiple defaults
def order_coffee(size="medium", milk=False, sugar=0):
    print(f"Order: {size} coffee")
    if milk:
        print("  - with milk")
    if sugar > 0:
        print(f"  - with {sugar} sugar(s)")
    print()

# Use all defaults
order_coffee()

# Override some defaults
order_coffee(size="large", sugar=2)
order_coffee(milk=True, sugar=1)
order_coffee("small", True, 3)
```

**Output:**
```
Hello, Friend Alice!
Hello, Dr. Smith!
Hello, Professor Johnson!
Hello, Captain Brown!

Order: medium coffee

Order: large coffee
  - with 2 sugar(s)

Order: medium coffee
  - with milk
  - with 1 sugar(s)

Order: small coffee
  - with milk
  - with 3 sugar(s)
```

### Functions that Return Values

Often you want a function to calculate something and give you the result back. Use the `return` statement:

```python
# Function that returns a value
def add_numbers(a, b):
    result = a + b
    return result

# Store the returned value in a variable
sum1 = add_numbers(5, 3)
sum2 = add_numbers(10, 20)

print("First sum:", sum1)
print("Second sum:", sum2)

# You can also use the returned value directly
print("Third sum:", add_numbers(100, 50))
```

**Output:**
```
First sum: 8
Second sum: 30
Third sum: 150
```

**Important:** When a function hits a `return` statement, it immediately exits and gives back the value. Any code after `return` won't run!

```python
def calculate_area(length, width):
    area = length * width
    return area
    print("This will never print!")  # Code after return doesn't execute

result = calculate_area(5, 4)
print("Area:", result)
```

**Output:**
```
Area: 20
```

### Functions with Conditionals and Loops

Functions can contain any code, including if statements and loops:

```python
# Function that uses conditionals
def classify_grade(score):
    if score >= 90:
        return "A"
    elif score >= 80:
        return "B"
    elif score >= 70:
        return "C"
    elif score >= 60:
        return "D"
    else:
        return "F"

# Test the function
print("Score 95:", classify_grade(95))
print("Score 82:", classify_grade(82))
print("Score 58:", classify_grade(58))

print()

# Function that uses loops
def print_countdown(start):
    for i in range(start, 0, -1):
        print(i)
    print("Blast off!")

print_countdown(5)
```

**Output:**
```
Score 95: A
Score 82: B
Score 58: F

5
4
3
2
1
Blast off!
```

### Practical Example: Data Processing Function

Here's a more realistic example that you might use in research:

```python
import statistics

def analyze_data(data_list):
    """
    Analyzes a list of numbers and returns a summary.
    """
    if len(data_list) == 0:
        return "No data to analyze!"

    mean = statistics.mean(data_list)
    median = statistics.median(data_list)
    minimum = min(data_list)
    maximum = max(data_list)

    print(f"Data Analysis Results:")
    print(f"  Count: {len(data_list)}")
    print(f"  Mean: {mean:.2f}")
    print(f"  Median: {median:.2f}")
    print(f"  Min: {minimum}")
    print(f"  Max: {maximum}")

    return mean  # Return the mean for further use

# Test the function
test_scores = [85, 92, 78, 90, 88, 95, 82, 87]
average = analyze_data(test_scores)
print(f"\nReturned average: {average:.2f}")
```

**Output:**
```
Data Analysis Results:
  Count: 8
  Mean: 87.12
  Median: 88.00
  Min: 78
  Max: 95

Returned average: 87.12
```

**Note:** The text in triple quotes `"""` is called a **docstring** - it's a special comment that describes what the function does. This is good practice for documenting your code!

### Why Use Functions?

Functions provide several important benefits:

1. **Reusability** - Write code once, use it many times
2. **Organization** - Break complex problems into smaller, manageable pieces
3. **Readability** - Give meaningful names to chunks of code
4. **Testing** - Easier to test individual functions
5. **Maintenance** - Fix bugs in one place instead of many

### Example: Before and After Functions

```python
# WITHOUT functions - repetitive!
celsius1 = (98.6 - 32) * 5/9
print(f"98.6°F = {celsius1:.1f}°C")

celsius2 = (32 - 32) * 5/9
print(f"32°F = {celsius2:.1f}°C")

celsius3 = (212 - 32) * 5/9
print(f"212°F = {celsius3:.1f}°C")

print("\n--- WITH functions - much better! ---\n")

# WITH functions - clean and reusable!
def fahrenheit_to_celsius(fahrenheit):
    celsius = (fahrenheit - 32) * 5/9
    return celsius

# Easy to use multiple times
temps_f = [98.6, 32, 212, 72, 100]
for temp in temps_f:
    temp_c = fahrenheit_to_celsius(temp)
    print(f"{temp}°F = {temp_c:.1f}°C")
```

**Output:**
```
98.6°F = 37.0°C
32°F = 0.0°C
212°F = 100.0°C

--- WITH functions - much better! ---

98.6°F = 37.0°C
32°F = 0.0°C
212°F = 100.0°C
72°F = 22.2°C
100°F = 37.8°C
```

## Practice Exercises

Now it's your turn! Try these exercises to practice what you've learned throughout this guide.

### Exercise 1: Personal Introduction
Write a program that prints 5 sentences about yourself.

### Exercise 2: Simple Calculator
Create variables for two numbers, then print their sum, difference, product, and quotient.

### Exercise 3: Favorite Things
Ask the user for their favorite food, movie, and book, then print a summary message.

### Exercise 4: Temperature Converter (Challenge!)
Ask the user for a temperature in Fahrenheit, convert it to Celsius using the formula `(F - 32) * 5/9`, and display the result.

**Hint:** You'll need to convert the input to a number first using `int()` or `float()`!

### Exercise 5: Check if Even or Odd
Write a function called `is_even` that takes a number as a parameter and returns `True` if the number is even, and `False` if it's odd.

**Hint:** Remember the modulo operator `%` - a number is even if `number % 2 == 0`

### Exercise 6: Find the Maximum
Write a function called `find_max` that takes a list of numbers as a parameter and returns the largest number in the list.

**Hint:** You can use a variable to keep track of the maximum value found so far, and use a for loop to go through each number.

### Exercise 7: Count Vowels
Write a function called `count_vowels` that takes a string as a parameter and returns the number of vowels (a, e, i, o, u) in that string. You can ignore uppercase vs lowercase.

**Hint:** Use a for loop to go through each character in the string, and use an if statement to check if it's a vowel. Remember that you can check if a character is in a list: `if char in ['a', 'e', 'i', 'o', 'u']:`

## Congratulations!

You've completed the introduction to Python programming! You now understand:

- How to write and run Python code
- Variables and different data types
- User input and output
- Conditional statements (if/elif/else)
- Loops (for and while)
- Functions with parameters and return values

These fundamentals are the building blocks for everything else you'll learn in Python. Keep practicing, and don't be afraid to experiment with the code examples. The best way to learn programming is by doing!