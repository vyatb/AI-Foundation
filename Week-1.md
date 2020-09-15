# Outline

* Introduction to Python
* Variable and Built-in Functions
* Function Construction
* Condition
* For Loop
* While Loop
* Common Errors

# Introduction to Python

## Python History

* 02/1991: Python 0.9.0
* 01/1994: Python 1.0
* 12/1997: Python 1.5
* 09/2000: Python 1.6
* 10/2000: Python 2.0
* 04/2001: Python 2.1
* 10/2008: Python 2.6
* 12/2008: Python 3.0
* 12/2016: Python 3.6
* 10/2019: Python 3.8
* 10/2020: Python 3.9

Python is a high-level, interpreted, and general-purpose scripting language developed by Guido van Rossum in the late 19th century. Python is a great programming language for beginner-level programmers and is widely used in Data Science and Machine Learning due to its code readability, easy-to-use syntax, and its massive libraries. 

## Python Ecosystem

* Visualization: 
  * matplotlib
  * plotly,
  * ...
* Machine Learning and Deep Learning: 
  * TensorFlow
  * Keras
  * PyTorch
  * Scikit-learn
  * ...
* Natural Language Processing (NLP):
  * Natural Language Toolkit (NLTK)
  * Gensim - Topic Modeling
  * spaCy
  * ...
* Scientific Computing:
  * NumPy
  * Pandas
* IDEs:
  * PyCharm
  * Jupyter Notebook
  * Google Colaboratory (Google Colab)
  * Visual Studio
  * Sublime Text
  * Atom
  * ...

## First Python Program

```python
print('Hello!')
```



## Variable

```
variable_name = variable_value
```

|         | variable_value                   |
| ------- | -------------------------------- |
| Integer | -2, -1, 0, 1, 2                  |
| Float   | 1.5, 0.5, -3.21, 1.0             |
| String  | 'Joe', 'Schmoe', "Joe", "Schmoe" |
| Boolean | True, False                      |

```python
# create an integer variable named number_of_days with value 10
number_of_days = 10

# create a float variable named distance with value 20.5
distance = 20.5

# create a string variable named greeting with assigned value as "Hello"
greeting = "Hello"

# create a boolean variable named is_student whose initial value is True
is_student = True
```

```python
age = 19
print(age) # print the value of age
```



## Built-in Functions

### print()

```
print(parameters)
```

```python
# create an integer variable named number_of_days with value 10
number_of_days = 10
print(number_of_days)

# create a float variable named distance with value 20.5
distance = 20.5
print(distance)

# create a string variable named greeting with assigned value as "Hello"
greeting = "Hello"
print(greeting)

# create a boolean variable named is_student whose initial value is True
is_student = True
print(is_student)
```

```python
def = 15
print(def) # Syntax Error
```

### type()

```
type(parameter)
```

```python
# create an integer variable named number_of_days with value 10
number_of_days = 10
data_type_of_number_of_days = type(number_of_days)
print(data_type_of_number_of_days)

# create a float variable named distance with value 20.5
distance = 20.5
data_type_of_distance = type(distance)
print(data_type_of_distance)

# create a string variable named greeting with assigned value as "Hello"
greeting = "Hello"
data_type_of_greeting = type(greeting)
print(data_type_of_greeting)

# create a boolean variable named is_student whose initial value is True
is_student = True
data_type_of_is_student = type(is_student)
print(data_type_of_is_student)
```

```python
greeting = 'Hello'
print(type(greeting)) # print out the type of greeting
```

### input()

```
input(prompt)
```

```python
# ask user for input
input_data = input("Please enter your name: ")

print(type(input_data))
print(input_data)
```

### Type Conversion

#### int()

```python
input_data = input("Please enter your age: ") # String type
input_data_int = int(input_data)
data_type = type(input_data_int)
print(data_type)
print(input_data_int)
```

#### float()

```python
input_data = input("Please enter your weight (kg): ") # String type
input_data_float = float(input_data)
data_type = type(input_data_float)
print(data_type)
print(input_data_float)
```



## Basic Operators

| Arithmetic Operators | Name             |
| -------------------- | ---------------- |
| +                    | Addition         |
| -                    | Subtraction      |
| *                    | Multiplication   |
| /                    | Division         |
| //                   | Integer division |
| %                    | Modulus          |
| **                   | Exponentiation   |

```python
# Initialize x as 3
x = 3

# Initialize y as 2
y = 2

# Print the sum of x and y
print(x + y)

# Print the difference between x and y
print(x - y)

# Print the product of x and y
print(x * y)

# Print the division of x / y
print(x / y)

# Print the integer division of x / y
print(x // y)

# Print the remainder of x / y
print(x % y)

# Print the result of x to the power y
print(x ** y)
```



## Example

### Celsius to Fahrenheit conversion

$$
F =  \frac{9C}{5} + 32
$$

```python
# input prompt
temp_c = float(input('Enter temperature in celsius: '))

# calculate
temp_f = ((9/5) * temp_c) + 32

# output
print("The corresponding fahrenheit degree is ", temp_f)
```

### Fahrenheit to Celsius conversion

$$
C =  \frac{5}{9}(F-32) 
$$

```python
temp_f = float(input("Celsius: "))
temp_c = (5/9) * (temp_f - 32)
print(temp_c)
```



## Functions

### Notes for function construction

* Define function name: Lowercase with underscores and begin with a verb.
* Indentation: 4 spaces (preferred) for indentation.
* Determine function parameters: Input data.
* Do docstring: Explain and describe the function.
* Output of the function.

### General structure of a function

```python
def function_name(parameters):
    '''
    docstring stays here
    '''
    
    code goes here
    
    return result
```

#### Example: Calculate area of a rectangle

```python
def compute_rectangle_area(height, width):
    '''
    Some things about this function
    '''
    area = height * width
    return area
```

```python
# test cases:
# h = 5, w = 6: area = 30
# h = 10, w = 4: area = 40

area_1 = compute_rectangle_area(5, 6)
print(area_1)

area_2 = compute_rectangle_area (10, 4)
print(area_2)
```

#### Area of common plane shapes

![common-plane](https://miro.medium.com/max/1050/0*hpiUZgo87jdP6Src.png)



### Default values

```python
def compute_rectangle_area(height=0, width=0):
    '''
    This function calculates the area of a rectangle.
    
    height -- rectangle's height
    width -- rectangle's width
    
    Return value is the area of the rectangle.
    '''
    area = height * width
    return area
```

```python
area_1 = compute_rectangle_area(5, 6)
print('Area 1:', area_1)

area_2 = compute_rectangle_area (height=5, width = 6)
print('Area 2:', area_2)

area_3 = compute_rectangle_area(width=6, height=5)
print('Area 3:', area_3)

area_4 = compute_rectangle_area(width=6,
                               height=5)
print('Area 4:', area_4)

area_5 = compute_rectangle_area()
print('Area 5:', area_5)
```



## Comparison

### Comparison operators

| Comparison operators | Name                     |
| -------------------- | ------------------------ |
| ==                   | Equal                    |
| !=                   | Not equal                |
| >                    | Greater than             |
| <                    | Smaller than             |
| >=                   | Greater than or equal to |
| <=                   | Smaller than or equal to |

```python
a = 5
b = 8
print(a == b) # False
print(a != b) # True
print(a > b) # False
print(a >= b) # False
print(a < b) # True
print(a <= b) # True
```



## Condition

### if condition

Python relies on indentation to define the scope of a function, in this case if condition.

```python
# code statements/blocks before if 

if condition:
    # code inside 
    
# code after if
```

#### Example: ReLU

$$
ReLU(x) =  x =\begin{cases}0 & if & x <= 0\\x & if & x > 0\end{cases}
$$

```python
def ReLU(x):
    '''
    This function calculates ReLU for a value x.
    '''
    
    result = 0
    
    if x > 0:
        result = x
      
    return result
```

```python
value_1 = ReLU(5)
value_2 = ReLU(-2)
print(value_1)
print(value_2)
```

### if-else condition

```python
# code statements/blocks before if

if condition:
    # when condition is satisfied, evaluate line(s) of code inside if
else:
    # when condition is not satisfied, evaluate line(s) of code inside else
    
# code after if
```

#### Example: Compute LBP(x, y)

$$
LBP(x, y) =  x =\begin{cases}0 & if & x = y\\1 & if & x > y\\-1 & if & x < y\end{cases} 
$$

```python
def compute_LBP(x, y):
    '''
    docstring does here
    '''
    
    result = 1000
    
    if x == y:
        result = 0
    elif x < y:
        result = -1
    else:
        result = 1
        
    return result
```



## Random and Math Modules

### Absolute value of x

```python
import math
n1 = 1
n2 = 2
print(math.fabs(n1))
print(math.fabs(n2))
```

### Exponential of x

```python
import math
x = 2
print(math.exp(x))
```

### Log(x)

```python
import math
x = 4
print(math.log(x))
print(math.log(math.e))
```

### Square root of x

```python
import math
x = 4
print(math.sqrt(x))
```

### Sine of x

```python
import math
x = 2
print(math.sin(x))
```

### Cosine of x

```python
import math
x = 2
print(math.cos(x))
```

### The number e (mathematical constant)

```python
import math
print(math.e)
```

### The number PI (mathematical constant)

```python
import math
print(math.pi)
```

### Generate random floating-point numbers in [0, 1]

```python
import random
print(random.random())
```



## For Loops

```python
# iterate through a list
fruits = ['apple', 'bananas', 'melon', 'peach']
for fruit in fruits:
    print(fruit)
```

```python
# iterate through a string
greeting = 'Hello'
for char in greeting:
    print(char)
```

```python
# iterate through a dictionary
parameters = ('learning_rate': 0.1,
             'optimizer': 'Adam',
             'metric': 'Accuracy')
for key in parameters:
    print(key, parameters.get(key))
```

```python
# iterate through a tuple
fruits = ('apple', 'banana', 'melon')
for fruit in fruits:
    print(fruit)
```

```python
# use range()
for i in range(5):
    print(i)
```

### range()

```
range(start, stop, step)
```

### *break* keyword

**break** stops the current loop and resumes the execution of the next statement. In case of nested loops, **break** terminate the execution of the innermost statement and resumes the execution of the next line of code after the loop.

```python
for i in range(10):
    if i == 5:
        break
    print('i is', i)
```

### ***continue*** keyword

**continue** ends the current iteration in a for loop (or a while loop) and continues to the next iteration.

```python
for i in range(10):
    if i == 5:
        continue
	print('i is ', i)
```



## Example

### Simulation of coin tossing

* Event: a set of outcomes of an experiment.
* Experiment: any procedure that can be infinitely repeated and has a well-defined set of possible outcomes, known as the sample space.
* Sample space: the set of all possible outcomes or results of an experiment
* Random variable: a numerical description of the outcome of a statistical experiment

```python
import random

total_flips = 0
num_tails = 0
num_heads = 0

for i in range(100):
    n = random.random()
    if n < 0.5:
        num_tails += 1
    else:
        num_heads += 1
    
    total_flips += 1
```

### PI Estimation (through Monte Carlo simulation)

<img src="https://cvw.cac.cornell.edu/python/images/throwingdarts.png" alt="pi-estimation" style="zoom: 33%;" />

N<sub>s</sub> is the number of random samples within the square generated according to uniform distribution.

N<sub>c</sub> is the number of random samples within the circle generated according to uniform distribution.
$$
Circle \\
r = 1 \\S_c = \pi r^2
$$

$$
Square \\
s = 2 \\ S_s = s^2
$$

$$
\frac{S_s}{S_c} = \frac{N_s}{N_c}
$$

$$
\pi \approx \frac{s^2 N_c}{N_s}
$$

```
random numbers are within [-1, 1]
Let c be distance between two point A(xA, yA) and B(xB, yB)
```

![distance-1](https://www.mathsisfun.com/algebra/images/dist-2-points-a.svg)

![distance-2](https://www.mathsisfun.com/algebra/images/dist-2-points-b.gif)

![distance-3](https://www.mathsisfun.com/algebra/images/dist-2-points-c.gif)
$$
c = \sqrt{(x_A - x_B)^2 + (y_A - y_B)^2}
$$

```python
import random
import math

# Total number of point p
N = 100000

# Number of points falling within the circle
N_T = 0

# Calculation
for i in range(N):
    # x and y are within [-1, 1]
    x = random.random() * 2 - 1
    y = random.random() * 2 - 1
    
    x2 = x ** 2
    y2 = y ** 2
    
    # check if p is inside the circlew
    if math.sqrt(x2 + y2) <= 1.0:
        N_T += 1
        
# Calculate PI
pi = (N_T / N) * 4
print(pi)
```

