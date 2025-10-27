<h1><sub><img src="https://github.com/RadhikaDeshpande1010/icon-library/blob/main/python-icon/python-icon.png" alt="Icon" height="27" width="27"></sub> Mastering Python Collections — Lists, Sets, and Strings </h1>

<h2>Algorithmic Problems on Lists, Sets & Strings</h2>

This notebook — Algorithmic Problems on Lists, Sets, and Strings — is part of the Advanced Concepts module in Python.
It presents a curated collection of logic-driven, algorithmic exercises designed to strengthen your data handling and problem-solving capabilities in Python.

The problems focus on how to think algorithmically while manipulating lists, sets, and strings — emphasizing performance, readability, and Pythonic design patterns.

Each exercise includes step-by-step examples with clear input–output demonstrations, enabling hands-on understanding of key concepts.

🎯 Learning Objectives

- Master advanced sequence and text manipulation using Python’s core data structures

- Apply algorithmic thinking to solve real-world programming challenges

- Optimize logic through list/set comprehensions and functional approaches

- Build readiness for technical interviews, automation scripting, and analytics workflows

⚙️ Topics Covered

- Nested data structure traversal and transformation

- Advanced filtering, aggregation, and deduplication

- String parsing, formatting, and case transformations

- Algorithmic techniques using loops, conditions, and comprehensions

- Problem-solving patterns combining lists, sets, and strings

> **Python version:** 3.8+

---

### How to Run

1. **Clone** this repository and open the folder in your editor/terminal.
2. Start Jupyter Notebook:

   ```bash
    jupyter notebook
   ```

> Tip: You can also copy any solution function into your notebook/REPL to experiment quickly.

---

## List Operations

---
Q1. Write a Python program to find the element(s) that occur the most number of times in a given list.

If multiple elements have the same highest frequency, print all of them.

**Input:** `[1,2,3,2,4,3,5,4,6,5,2,2,2,3,3,3]`

**Output:** `2, 3`

```python
list1 = [1,2,3,2,4,3,5,4,6,5,2,2,2,3,3,3]
list2 = []
count_list = []

# Collect unique elements in list2:
for i in list1:
    if i not in list2:
        list2.append(i)
# Count occurrences of each unique element:
for k in list2:
    count_list.append(list1.count(k))

# Find the maximum count: 5
max_value = max(count_list)

# Print elements with max count (i.e., appearing most times):
index = 0
for k in count_list:
    if k == max_value:
        print(list2[index])
    index = index + 1

Output:
2, 3
```

### Q2. Write a Python program to reverse the elements of a given list using slicing.
**Input:** `[1, 2, 3, 4, 5]`

**Output:** `[5, 4, 3, 2, 1]`

```python
# Reverse a list using slicing
input_list = [1, 2, 3, 4, 5]
list_output = input_list[::-1]
print(list_output)

Output:
[5, 4, 3, 2, 1]
```

### Q3. Write a Python program to find and print the maximum element from a given list using the built-in max() function.
**Input:** `[10, 25, 3, 99, 47]`

**Output:** `99`

```python
# Find the maximum element in a list
input_list = [10, 25, 3, 99, 47]
output_list = max(input_list)
print(output_list)

Output:
99
```

### Q4. Write a Python program to remove duplicate elements from a list while preserving the original order.
**Input:** `[1, 2, 2, 3, 4, 4, 5]`

**Output:** `[1, 2, 3, 4, 5]`

```python
# Remove duplicates from a list
for i in input_list:
    if i not in output_list:
        output_list.append(i)
print(output_list)

Output:
[1, 2, 3, 4, 5]
```

### Q5. Write a Python program to calculate the sum of all elements in a given list using a loop.
**Input:** `[5, 10, 15, 20]`

**Output:** `50`

```python
input_list = [5, 10, 15, 20]
result = 0
for n in input_list:
    result += n
print(result)

Output:
50
```

### Q6. Write a Python program to extract and print all even numbers from a given list.
Input: `[12, 7, 9, 14, 21, 6]`

Output: `[12, 14, 6]`

```python
input_list = [12, 7, 9, 14, 21, 6]
output_list = []
for n in input_list:
    if n % 2 == 0:
        output_list.append(n)
print(output_list)

Output:
[12, 14, 6]
```

---

## String Operations - Basic

### Q7. Write a Python program to check whether a given string is a palindrome or not.
A palindrome reads the same backward as forward.

**Input:** `"madam"`

**Output:** `True`

```python
input_string = "madam"
if input_string == input_string[::-1]:
    print(True)
else:
    print(False)

Output:
True
```

### Q8. Write a Python program to count the number of vowels in a given string.
(Consider only lowercase vowels for simplicity.)

**Input:** `"Programming"`

**Output:** `3`

```python
input_string = "Programming"
vowels = "aeiou"
string_count = 0
for i in input_string:
    if i in vowels:
        string_count += 1
print(string_count)

Ouput:
3
```

### Q9. Write a Python program to convert a given string into uppercase using the built-in string method .upper().
**Input:** `"hello world"`

**Output:** `"HELLO WORLD"`

```python
input_string = "hello world"
output_string = input_string.upper()
print(output_string)

Output:
HELLO WORLD
```

### Q10. Write a Python program to replace all spaces in a given string with hyphens (-) using the .replace() method.
**Input:** `"Python is fun"`

**Output:** `"Python-is-fun"`

```python
input_string = "Python is fun"
output_string = input_string.replace(" ","-")
print(output_string)

Output:
Python-is-fun
```

---

## String Operations - Advanced

### Q11. Write a Python program to count how many words in a given sentence start with a vowel (a, e, i, o, u).
**Input:** `"Apple is an orange fruit but mango is not"`

**Output:** `4`

```python
text = "Apple is an orange fruit but mango is not"
vowels = 'aeiou'
count_ch = 0
for word in text.split(" "):
    first_char = word[0]
    if first_char.lower() in vowels:
        count_ch += 1
print(count_ch)

Output:
4
```

### Q12. Write a Python program to replace all special characters in a given string with the # symbol.
(Consider alphabets and numbers as valid characters — everything else should be replaced.)

**Input:** `"Hello@World#2025!"`

**Output:** `"Hello#World#2025#"`

```python
text1 = "Hello@World#2025!"
text2 = ''
for i in text1:
    if i.isalnum():
        text2 += i
    else:
        text2 += '#'
print(text2)

Output:
Hello#World#2025#
```

### Q13. Write a Python program to extract and print all digits from a given alphanumeric string.
**Input:** `"abc123xyz456"`

**Output:** `"123456"`

```python
text = "abc123xyz456"
text2 = ''
for ch in text:
    if ch.isdigit():
        text2 += ch
print(text2)

Output:
123456
```

### Q14. Write a Python program to count how many times each word appears in a given sentence and store the result in a dictionary.
**Input:** `"data science is fun and data is power"`

**Output:** `{'data': 2, 'science': 1, 'is': 2, 'fun': 1, 'and': 1, 'power': 1}`

```python
text = "data science is fun and data is power"
dict1 = {}

for word in text.split(" "):
    if word in dict1:
        dict1[word] += 1
    else:
        dict1[word] = 1

print(dict1)

Output:
{'data': 2, 'science': 1, 'is': 2, 'fun': 1, 'and': 1, 'power': 1}
```

### Q15. Write a Python program to find and print the first non-repeating (unique) character from a given string.
**Input:** `"aabbcddeeff"`

**Output:** `"c"`

```python
text = "aabbcddeeff"
for ch in text:
    if text.count(ch) == 1:
        print(ch)
        break

Output:
c
```

### Q16. Write a Python program to replace spaces with underscores (_) only in the first three words of a given sentence.
Keep the remaining words separated by spaces.

**Input:** `"Python is awesome and very powerful"`

**Output:** `"Python_is_awesome_and very powerful"`

```python
text = "Python is awesome and very powerful"
word = text.split(" ")
first_part = "_".join(word[:3])
last_part = " ".join(word[3:])
print(first_part + "_" + last_part)
```

### Q17. Write a Python program to find and print the longest word in a given sentence.
If multiple words have the same length, print the first one that appears.

**Input:** `"Artificial Intelligence is revolutionary"`

**Output:** `"revolutionary"`

```python
text = "Artificial Intelligence is revolutionary"
max_len = 0
long_word = ''
for word in text.split(" "):
    word_length = len(word)
    if word_length > max_len:
        max_len = word_length
        long_word = word
print(long_word)

Output:
revolutionary
```

### Q18. Write a Python program to count how many words in a given sentence end with the letter 'e'.
**Input:** `"We love code in the evening"`

**Output:** `4`

```python
text = "We love code in the evening"
count_word = 0
for word in text.split(" "):
    if word[-1] == 'e':
        count_word += 1
print(count_word)

Output:
4
```

### Q19. Write a Python program to remove all numeric digits from a given alphanumeric string and print only the letters.
**Input:** `"abc123def456"`

**Output:** `"abcdef"`

```python
text = "abc123def456"
text2 = ''
for i in text:
    if i.isalpha():
        text2 += i
print(text2)

Output:
abcdef
```

### Q20. Write a Python program to count the occurrences of each character in a given string and store the result in a dictionary.
**Input:** `"google"`

**Output:** `{'g': 2, 'o': 2, 'l': 1, 'e': 1}`

```python
text = "google"
dict1 = {}
for i in text:
    if i in dict1:
        dict1[i] += 1
    else:
        dict1[i] = 1
print(dict1)

Output:
{'g': 2, 'o': 2, 'l': 1, 'e': 1}
```

### Q21. Write a Python program to remove all vowels (a, e, i, o, u) from a given string and print the result.
**Input:** `"Programming is exciting"`

**Output:** `"Prgrmmng s xctng"`

```python
text = "Programming is exciting"
vowels = 'aeiou'
res = ''
for i in text:
    if i.lower() not in vowels:
        res += i
print(res)

Output:
Prgrmmng s xctng
```

### Q22. Write a Python program to reverse the order of words in a given sentence while keeping each word intact.
**Input:** `"I love Python"`

**Output:** `"Python love I"`

```python
text = "I love Python"
word = text.split(" ")
rev_word = word[::-1]
result = " ".join(rev_word)
print(result)

Output:
Python love I
```

### Q23. Write a Python program to remove duplicate characters from a given string while preserving the order of their first appearance.
**Input:** `"programming"`

**Output:** `"progamin"`

```python
text = "programming"
count_ch = ''
for ch in text:
    if ch not in count_ch:
        count_ch += ch
print(count_ch)

Output:
progamin
```

### Q24. Write a Python program to replace the nth occurrence of a word in a string with a new given word.
For example, replace the 3rd occurrence of "test" with "exam".

**Input:** `"test test test test", n = 3, replace = "exam"`

**Output:** `"test test exam test"`

```python
text = "test test test test"
n = 3
words = text.split(" ")
words[n-1] = "exam"
result = " ".join(words)
print(result)

Python:
test test exam test
```

### Q25. Write a Python program to convert a given string into title case, where the first letter of each word is capitalized, and the rest are in lowercase.

**Input:** `"wELCoMe TO PYthon"`

**Output:** `"Welcome To Python"`

```python
text = "wELCoMe TO PYthon"
res = text.title()
print(res)

Python:
Welcome To Python
```

### Q26. Write a Python program to swap the case of each character in a given string — converting uppercase letters to lowercase and lowercase letters to uppercase.

**Input:** `"HeLLo WOrLD"`

**Output:** `"hEllO woRld"`

```python
text = "HeLLo WOrLD"
char_ch = ''
for ch in text:
    if ch.islower():
        char_ch += ch.upper()
    elif ch.isupper():
        char_ch += ch.lower()
    else:
        char_ch += ch
print(char_ch)

Output:
hEllO woRld
```

### Q27. Write a Python program to mask all the middle digits of a given number string with asterisks (*), keeping only the first two and last two digits visible.
**Input:** `"9876543210"`

**Output:** `"98******10"`

```python
str1 = "9876543210"
str_output = str1[:2] + '*' * (len(str1) - 4) + str1[-2:]
print(str_output)

Output:
98******10
```

### Q28. Write a Python program to reverse each word in a given sentence while keeping the word order unchanged.
**Input:** `"Python is fun"`

**Output:** `"nohtyP si nuf"`

```python
str1 = "Python is fun"
list_output = []
words = str1.strip().split()
for word in words:
    list_output.append(word[::-1])
string_output = ' '.join(list_output)
print(string_output)

Python:
nohtyP si nuf
```

### Q29. Write a Python program to replace all vowels in a given string with the * symbol.
***Input:*** `"Artificial Intelligence"`

***Output:*** `"*rt*f*c**l *nt*ll*g*nc*"`

```python
str1 = "Artificial Intelligence"
vowels = 'aeiouAEIOU'
string_output = ''
for ch in str1:
    if ch in vowels:
        string_output += '*'
    else:
        string_output += ch
print(string_output)

Output:
*rt*f*c**l *nt*ll*g*nc*
```

### 31. Extract Digits Only
```python
# Input: "Room 24, Floor 7"
# Output: "247"
str1 = "Room 24, Floor 7"
string_output = ""
for ch in str1:
    if ch.isdigit():
        string_output += ch
print(string_output)
```

### 32. Count Words in Sentence
```python
# Input: "Data Science with Python"
# Output: 4
str1 = "Data Science with Python"
words = str1.strip().split()
count_val = len(words)
print(count_val)
```

### 33. First and Last Character Swap
```python
# Input: "HELLO"
# Output: "OELLH"
str1 = "HELLO"
swapped = str1[-1] + str1[1:-1] + str1[0]
print(swapped)
```

### 34. Snake Case to Camel Case
```python
# Input: "machine_learning_project"
# Output: "machineLearningProject"
str1 = "machine_learning_project"
part = str1.split("_")
string_output = part[0]
for word in part[1:]:
    string_output += word.capitalize()
print(string_output)
```

### 35. Remove Spaces from String
```python
# Input: " Hello World "
# Output: "HelloWorld"
str1 = " Hello World "
string_output = str1.strip()
cleaned = "".join(string_output.split())
print(cleaned)
```

### 36. Replace First and Last Word
```python
# Input: "Python makes programming easy"
# Output: "**** makes programming ****"
str1 = "Python makes programming easy"
words = str1.strip().split()
words[0] = "****"
words[-1] = "****"
string_output = " ".join(words)
print(string_output)
```

---

## Dictionary Operations

### 37. Find Length of Dictionary
```python
# Input: {"a": 1, "b": 2, "c": 3}
# Output: 3
input_dict = {"a": 1, "b": 2, "c": 3}
output = len(input_dict)
print(output)
```

### 38. Access Value by Key
```python
# Input: {"name": "Alice", "age": 25}, key="age"
# Output: 25
input_dict = {"name": "Alice", "age": 25}
print(input_dict["age"])
```

### 39. Merge Two Dictionaries
```python
# Input: {"a": 1, "b": 2}, {"c": 3, "d": 4}
# Output: {"a": 1, "b": 2, "c": 3, "d": 4}
input_dict1 = {"a": 1, "b": 2}
input_dict2 = {"c": 3, "d": 4}
input_dict1.update(input_dict2)
print(input_dict1)
```

### 40. Find Key with Maximum Value
```python
# Input: {"apple": 50, "banana": 100, "orange": 70}
# Output: "banana"
input_dict = {"apple": 50, "banana": 100, "orange": 70}
output = max(input_dict, key=input_dict.get)
print(output)
```

### 41. Remove a Key from Dictionary
```python
# Input: {"x": 10, "y": 20, "z": 30}, remove "y"
# Output: {"x": 10, "z": 30}
input_dict = {"x": 10, "y": 20, "z": 30}
output = input_dict.pop("y")
print(input_dict)
```

---

## Function Exercises

### 42. Calculate Factorial
```python
# Input: factorial(5)
# Output: 120
def factorial(n):
    fact = 1
    for i in range(1, n+1):
        fact *= i
    return fact

output = factorial(5)
print(output)
```

### 43. Fibonacci Series
```python
# Generate Fibonacci series till n numbers
# Output for n=7: 0 1 1 2 3 5 8
first = 0
second = 1
n = 7

print(first, second, end=" ")

for i in range(3, n + 1):
    next_num = first + second
    print(next_num, end=" ")
    first = second
    second = next_num
```

### 44. Count Words in String
```python
# Input: count_words("Python is fun")
# Output: 3
def count_words(get_input_string):
    words = get_input_string.strip().split()
    return len(words)

text = "Python is fun"
output = count_words(text)
print(output)
```

### 45. Square of Numbers in List
```python
# Input: square_list([1, 2, 3, 4])
# Output: [1, 4, 9, 16]
def square_list(n):
    return n * n

input_list = [1, 2, 3, 4]
output = list(map(square_list, input_list))
print(output)
```

---

### ✅Conclusion

This module brought together a wide range of algorithmic exercises that strengthen problem-solving skills across lists, sets, and strings — three of Python’s most powerful data structures.

- Through these hands-on examples, you’ve practiced:

- Building efficient and reusable logic using Pythonic patterns

- Applying loops, conditions, and comprehensions to real-world data problems

- Writing clean, optimized, and readable code suitable for both interviews and production environments

As you move forward, continue exploring complex data manipulations, pattern recognition, and algorithm design using Python’s standard libraries and functional constructs.
This foundation will help you approach any coding challenge with clarity, structure, and confidence.
