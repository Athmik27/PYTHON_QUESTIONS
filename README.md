# Python  — Syntax Cheat Sheet

# 1. Take User Input 

```python
value = input("Enter value: ")
```

Integer:

```python
value = int(input("Enter value: "))
```

Float:

```python
value = float(input("Enter value: "))
```

---

# 2. Even or Odd

```python
if number % 2 == 0:
    # Even
else:
    # Odd
```

---

# 3. Positive, Negative or Zero

```python
if number > 0:
    # Positive
elif number < 0:
    # Negative
else:
    # Zero
```

---

# 4. Largest of Two Numbers

```python
if a > b:
    # a is largest
else:
    # b is largest
```

---

# 5. Largest of Three Numbers

```python
if a > b and a > c:
    # a is largest
elif b > a and b > c:
    # b is largest
else:
    # c is largest
```

---

# 6. Smallest of Three Numbers

```python
if a < b and a < c:
    # a is smallest
elif b < a and b < c:
    # b is smallest
else:
    # c is smallest
```

---

# 7. Check Divisibility

```python
if number % divisor == 0:
    # Divisible
else:
    # Not divisible
```

---

# 8. Swap Two Numbers

Using a temporary variable:

```python
temp = a
a = b
b = temp
```

Python method:

```python
a, b = b, a
```

---

# 9. Sum of Two Numbers

```python
result = a + b
```

---

# 10. Sum of Digits

Basic pattern:

```python
sum = 0

while number > 0:
    digit = number % 10
    sum += digit
    number //= 10
```

---

# 11. Count Digits

```python
count = 0

while number > 0:
    count += 1
    number //= 10
```

Alternative:

```python
count = len(str(number))
```

---

# 12. Reverse a Number

```python
reverse = 0

while number > 0:
    digit = number % 10
    reverse = reverse * 10 + digit
    number //= 10
```

---

# 13. Palindrome Number

Basic pattern:

```python
original = number
reverse = 0

while number > 0:
    digit = number % 10
    reverse = reverse * 10 + digit
    number //= 10

if original == reverse:
    # Palindrome
else:
    # Not palindrome
```

---

# 14. Prime Number

Basic pattern:

```python
if number < 2:
    # Not prime
else:

    for i in range(2, number):
        if number % i == 0:
            # Not prime
            break
    else:
        # Prime
```

Optimized condition:

```python
for i in range(2, int(number ** 0.5) + 1):
```

---

# 15. Factorial

Using loop:

```python
factorial = 1

for i in range(1, number + 1):
    factorial *= i
```

Using recursion:

```python
def factorial(n):

    if n == 0 or n == 1:
        return 1

    return n * factorial(n - 1)
```

---

# 16. Fibonacci Series

Basic pattern:

```python
a = 0
b = 1

for i in range(n):
    print(a)

    a, b = b, a + b
```

---

# 17. Armstrong Number

Basic pattern:

```python
original = number
digits = len(str(number))
total = 0

while number > 0:

    digit = number % 10
    total += digit ** digits
    number //= 10

if total == original:
    # Armstrong
else:
    # Not Armstrong
```

---

# 18. Multiplication Table

```python
for i in range(1, 11):
    print(number * i)
```

---

# 19. Sum of Natural Numbers

```python
total = 0

for i in range(1, n + 1):
    total += i
```

Formula:

```python
total = n * (n + 1) // 2
```

---

# 20. Check Vowel

```python
if character in "aeiouAEIOU":
    # Vowel
else:
    # Not vowel
```

---

# 21. Count Vowels

```python
count = 0

for character in string:

    if character in "aeiouAEIOU":
        count += 1
```

---

# 22. Reverse a String

Using slicing:

```python
reverse = string[::-1]
```

Using loop:

```python
reverse = ""

for character in string:
    reverse = character + reverse
```

---

# 23. Palindrome String

```python
if string == string[::-1]:
    # Palindrome
else:
    # Not palindrome
```

---

# 24. Count Characters

```python
count = len(string)
```

---

# 25. Count Specific Character

```python
count = string.count(character)
```

---

# 26. Find Character

```python
position = string.find(character)
```

---

# 27. Convert to Uppercase

```python
string.upper()
```

---

# 28. Convert to Lowercase

```python
string.lower()
```

---

# 29. Remove Spaces

```python
string.replace(" ", "")
```

---

# 30. Split a String

```python
words = string.split()
```

With a specific separator:

```python
items = string.split(",")
```

---

# 31. Join Strings

```python
result = " ".join(words)
```

---

# 32. Check Anagram

Basic pattern:

```python
if sorted(string1) == sorted(string2):
    # Anagram
else:
    # Not anagram
```

---

# 33. Find Largest Element in List

Using loop:

```python
largest = list[0]

for value in list:

    if value > largest:
        largest = value
```

Built-in:

```python
largest = max(list)
```

---

# 34. Find Smallest Element in List

Using loop:

```python
smallest = list[0]

for value in list:

    if value < smallest:
        smallest = value
```

Built-in:

```python
smallest = min(list)
```

---

# 35. Sum of List Elements

```python
total = 0

for value in list:
    total += value
```

Built-in:

```python
total = sum(list)
```

---

# 36. Count Elements in List

```python
count = len(list)
```

---

# 37. Search Element in List

```python
if value in list:
    # Found
else:
    # Not found
```

---

# 38. Remove Duplicates from List

Using `set`:

```python
unique = list(set(values))
```

Using loop:

```python
unique = []

for value in values:

    if value not in unique:
        unique.append(value)
```

---

# 39. Find Duplicate Elements

Basic pattern:

```python
duplicates = []

for value in values:

    if values.count(value) > 1 and value not in duplicates:
        duplicates.append(value)
```

---

# 40. Sort a List

Ascending:

```python
values.sort()
```

Descending:

```python
values.sort(reverse=True)
```

Using a new list:

```python
sorted_values = sorted(values)
```

---

# 41. Reverse a List

```python
values.reverse()
```

Using slicing:

```python
reverse = values[::-1]
```

---

# 42. Find Second Largest

Basic pattern:

```python
unique = list(set(values))
unique.sort()

second_largest = unique[-2]
```

---

# 43. Find Second Smallest

```python
unique = list(set(values))
unique.sort()

second_smallest = unique[1]
```

---

# 44. Even Numbers from List

```python
for value in values:

    if value % 2 == 0:
        print(value)
```

---

# 45. Odd Numbers from List

```python
for value in values:

    if value % 2 != 0:
        print(value)
```

---

# 46. Create List of Even Numbers

```python
even = [value for value in values if value % 2 == 0]
```

---

# 47. Create List of Odd Numbers

```python
odd = [value for value in values if value % 2 != 0]
```

---

# 48. Find Frequency of Element

```python
count = values.count(value)
```

Using dictionary:

```python
frequency = {}

for value in values:

    frequency[value] = frequency.get(value, 0) + 1
```

---

# 49. Find Maximum Without `max()`

```python
largest = values[0]

for value in values:

    if value > largest:
        largest = value
```

---

# 50. Find Minimum Without `min()`

```python
smallest = values[0]

for value in values:

    if value < smallest:
        smallest = value
```

---

# 51. Factorial Using Recursion

```python
def factorial(n):

    if n == 0:
        return 1

    return n * factorial(n - 1)
```

---

# 52. Sum of Natural Numbers Using Recursion

```python
def natural_sum(n):

    if n == 0:
        return 0

    return n + natural_sum(n - 1)
```

---

# 53. Sum of Digits Using Recursion

```python
def digit_sum(n):

    if n == 0:
        return 0

    return (n % 10) + digit_sum(n // 10)
```

---

# 54. Reverse String Using Function

```python
def reverse_string(string):

    return string[::-1]
```

---

# 55. Check Prime Using Function

```python
def is_prime(number):

    if number < 2:
        return False

    for i in range(2, int(number ** 0.5) + 1):

        if number % i == 0:
            return False

    return True
```

---

# 56. Find Factorial Using Function

```python
def factorial(number):

    result = 1

    for i in range(1, number + 1):
        result *= i

    return result
```

---

# 57. Count Vowels Using Function

```python
def count_vowels(string):

    count = 0

    for character in string:

        if character in "aeiouAEIOU":
            count += 1

    return count
```

---

# 58. Lambda Function

Basic syntax:

```python
lambda arguments: expression
```

Example:

```python
square = lambda x: x * x
```

---

# 59. Map

```python
result = map(function, iterable)
```

Example:

```python
result = list(map(lambda x: x * 2, values))
```

---

# 60. Filter

```python
result = filter(function, iterable)
```

Example:

```python
result = list(filter(lambda x: x % 2 == 0, values))
```

---

# 61. List Comprehension

Basic syntax:

```python
[expression for item in iterable]
```

With condition:

```python
[expression for item in iterable if condition]
```

Example:

```python
squares = [x * x for x in values]
```

---

# 62. Dictionary Comprehension

Basic syntax:

```python
{key: value for item in iterable}
```

Example:

```python
squares = {x: x * x for x in values}
```

---

# 63. Set Comprehension

```python
{x * x for x in values}
```

---

# 64. Generator

Basic syntax:

```python
def generator():

    yield value
```

Example:

```python
def numbers():

    for i in range(5):
        yield i
```

---

# 65. `*args`

Used to accept multiple positional arguments.

```python
def function(*args):

    for value in args:
        print(value)
```

Call:

```python
function(10, 20, 30)
```

---

# 66. `**kwargs`

Used to accept multiple keyword arguments.

```python
def function(**kwargs):

    for key, value in kwargs.items():
        print(key, value)
```

Call:

```python
function(name="Athmik", age=20)
```

---

# 67. Exception Handling

```python
try:
    # risky code

except Exception:
    # error handling

finally:
    # always executed
```

---

# 68. Raise Exception

```python
if condition:
    raise ValueError("Error message")
```

---

# 69. File Reading

```python
with open("file.txt", "r") as file:
    data = file.read()
```

---

# 70. File Writing

```python
with open("file.txt", "w") as file:
    file.write("Hello")
```

---

# 71. File Append

```python
with open("file.txt", "a") as file:
    file.write("New data")
```

---

# 72. Read File Line by Line

```python
with open("file.txt", "r") as file:

    for line in file:
        print(line)
```

---

# 73. Class

```python
class Student:

    def __init__(self, name):
        self.name = name

    def display(self):
        print(self.name)
```

Create object:

```python
student = Student("Athmik")
student.display()
```

---

# 74. Constructor

```python
def __init__(self, parameters):
    # initialization
```

---

# 75. Inheritance

```python
class Parent:

    def display(self):
        print("Parent")


class Child(Parent):

    pass
```

---

# 76. Method Overriding

```python
class Parent:

    def show(self):
        print("Parent")


class Child(Parent):

    def show(self):
        print("Child")
```

---

# 77. Dictionary Access

```python
student = {
    "name": "Athmik",
    "age": 20
}

print(student["name"])
```

Safe access:

```python
student.get("name")
```

---

# 78. Add Dictionary Element

```python
dictionary["key"] = "value"
```

---

# 79. Delete Dictionary Element

```python
del dictionary["key"]
```

Or:

```python
dictionary.pop("key")
```

---

# 80. Loop Through Dictionary

Keys:

```python
for key in dictionary:
    print(key)
```

Keys and values:

```python
for key, value in dictionary.items():
    print(key, value)
```

---

# 81. Find Common Elements

Using sets:

```python
common = set(list1) & set(list2)
```

---

# 82. Combine Two Lists

```python
combined = list1 + list2
```

---

# 83. Find Difference Between Lists

```python
difference = set(list1) - set(list2)
```

---

# 84. Check Leap Year

```python
if year % 400 == 0 or (year % 4 == 0 and year % 100 != 0):
    # Leap year
else:
    # Not leap year
```

---

# 85. FizzBuzz

Basic pattern:

```python
for i in range(1, n + 1):

    if i % 3 == 0 and i % 5 == 0:
        # FizzBuzz

    elif i % 3 == 0:
        # Fizz

    elif i % 5 == 0:
        # Buzz

    else:
        # Number
```

---

# 86. Find Missing Number

For numbers from `1` to `n`:

```python
expected = n * (n + 1) // 2

actual = sum(values)

missing = expected - actual
```

---

# 87. Find Common Characters

```python
common = set(string1) & set(string2)
```

---

# 88. Remove Spaces from String

```python
result = string.replace(" ", "")
```

---

# 89. Count Words

```python
words = string.split()

count = len(words)
```

---

# 90. Find Longest Word

```python
words = string.split()

longest = max(words, key=len)
```

---

# 91. Find Shortest Word

```python
words = string.split()

shortest = min(words, key=len)
```

---

# 92. Sort Words

```python
words = string.split()

words.sort()
```

---

# 93. Character Frequency

```python
frequency = {}

for character in string:

    frequency[character] = frequency.get(character, 0) + 1
```

---

# 94. First Non-Repeating Character

Basic pattern:

```python
for character in string:

    if string.count(character) == 1:
        # First non-repeating character
        break
```

---

# 95. Number Pattern

Basic nested-loop syntax:

```python
for i in range(1, n + 1):

    for j in range(i):
        print("*", end="")

    print()
```

Output:

```text
*
**
***
****
```

---

# 96. Nested Loop

```python
for i in range(rows):

    for j in range(columns):

        # operation
```

---

# 97. Matrix Input

```python
matrix = []

for i in range(rows):

    row = []

    for j in range(columns):
        value = int(input())
        row.append(value)

    matrix.append(row)
```

---

# 98. Matrix Traversal

```python
for row in matrix:

    for value in row:
        print(value)
```

---

# 99. Transpose Matrix

Using zip:

```python
transpose = list(zip(*matrix))
```

---

# 100. Basic Sorting Logic

Bubble sort pattern:

```python
for i in range(n):

    for j in range(0, n - i - 1):

        if values[j] > values[j + 1]:

            values[j], values[j + 1] = values[j + 1], values[j]
```

---


---

# Revision Pattern

```text
NUMBER PROBLEMS
        ↓
% 10     → Get last digit
// 10    → Remove last digit
* 10     → Build reverse number
```

```text
STRING PROBLEMS
        ↓
[::-1]       → Reverse
split()      → Words
join()       → Combine
count()      → Frequency
replace()    → Replace
upper()      → Uppercase
lower()      → Lowercase
```

```text
LIST PROBLEMS
        ↓
len()        → Length
max()        → Largest
min()        → Smallest
sum()        → Sum
sort()       → Sort
reverse()    → Reverse
count()      → Frequency
```

```text
DICTIONARY
        ↓
keys()       → Keys
values()     → Values
items()      → Key + Value
get()        → Safe access
pop()        → Remove
```

```text
LOOPS
        ↓
for          → Known/repeated iteration
while        → Condition-based iteration
nested loop  → Patterns / matrices
```

```text
FUNCTIONS
        ↓
def          → Create function
return       → Return result
*args        → Multiple positional arguments
**kwargs     → Multiple keyword arguments
```

---





