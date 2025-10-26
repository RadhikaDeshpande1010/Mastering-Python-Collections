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

### 1. Count Highest Occurrence in List

```python
# Input: [1,2,3,2,4,3,5,4,6,5,2,2,2,3,3,3]
# Ouput: 2, 3

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

### 2. Reverse a List
```python
# Input: [1, 2, 3, 4, 5]
# Output: [5, 4, 3, 2, 1]
input_list = [1, 2, 3, 4, 5]
list_output = input_list[::-1]
print(list_output)
```

### 3. Find Maximum Element
```python
# Input: [10, 25, 3, 99, 47]
# Output: 99
input_list = [10, 25, 3, 99, 47]
output_list = max(input_list)
print(output_list)
```

### 4. Remove Duplicates from List
```python
# Input: [1, 2, 2, 3, 4, 4, 5]
# Output: [1, 2, 3, 4, 5]
input_list = [1, 2, 2, 3, 4, 4, 5]
output_list = []
for i in input_list:
    if i not in output_list:
        output_list.append(i)
print(output_list)
```

### 5. Sum of All Elements
```python
# Input: [5, 10, 15, 20]
# Output: 50
input_list = [5, 10, 15, 20]
result = 0
for n in input_list:
    result += n
print(result)
```

### 6. Find Even Numbers
```python
# Input: [12, 7, 9, 14, 21, 6]
# Output: [12, 14, 6]
input_list = [12, 7, 9, 14, 21, 6]
output_list = []
for n in input_list:
    if n % 2 == 0:
        output_list.append(n)
print(output_list)
```

---

## String Operations - Basic

### 7. Reverse a String
```python
# Input: "Python"
# Output: "nohtyP"
input_string = "Python"
output_string = input_string[::-1]
print(output_string)
```

### 8. Check Palindrome String
```python
# Input: "madam"
# Output: True
input_string = "madam"
if input_string == input_string[::-1]:
    print(True)
else:
    print(False)
```

### 9. Count Vowels in String
```python
# Input: "Programming"
# Output: 3
input_string = "Programming"
vowels = "aeiou"
string_count = 0
for i in input_string:
    if i in vowels:
        string_count += 1
print(string_count)
```

### 10. Convert String to Uppercase
```python
# Input: "hello world"
# Output: "HELLO WORLD"
input_string = "hello world"
output_string = input_string.upper()
print(output_string)
```

### 11. Replace Spaces with Hyphens
```python
# Input: "Python is fun"
# Output: "Python-is-fun"
input_string = "Python is fun"
output_string = input_string.replace(" ","-")
print(output_string)
```

---

## String Operations - Advanced

### 12. Count Words Starting with Vowel
```python
# Input: "Apple is an orange fruit but mango is not"
# Output: 4
text = "Apple is an orange fruit but mango is not"
vowels = 'aeiou'
count_ch = 0
for word in text.split(" "):
    first_char = word[0]
    if first_char.lower() in vowels:
        count_ch += 1
print(count_ch)
```

### 13. Replace Special Characters with #
```python
# Input: "Hello@World#2025!"
# Output: "Hello#World#2025#"
text1 = "Hello@World#2025!"
text2 = ''
for i in text1:
    if i.isalnum():
        text2 += i
    else:
        text2 += '#'
print(text2)
```

### 14. Extract All Digits
```python
# Input: "abc123xyz456"
# Output: "123456"
text = "abc123xyz456"
text2 = ''
for ch in text:
    if ch.isdigit():
        text2 += ch
print(text2)
```

### 15. Count Word Occurrences
```python
# Input: "data science is fun and data is power"
# Output: {'data': 2, 'science': 1, 'is': 2, 'fun': 1, 'and': 1, 'power': 1}
text = "data science is fun and data is power"
dict1 = {}
for word in text.split(" "):
    if word in dict1:
        dict1[word] += 1
    else:
        dict1[word] = 1
print(dict1)
```

### 16. Find First Non-Repeating Character
```python
# Input: "aabbcddeeff"
# Output: "c"
text = "aabbcddeeff"
for ch in text:
    if text.count(ch) == 1:
        print(ch)
        break
```

### 17. Replace Spaces in First 3 Words
```python
# Input: "Python is awesome and very powerful"
# Output: "Python_is_awesome_and very powerful"
text = "Python is awesome and very powerful"
word = text.split(" ")
first_part = "_".join(word[:3])
last_part = " ".join(word[3:])
print(first_part + "_" + last_part)
```

### 18. Find Longest Word
```python
# Input: "Artificial Intelligence is revolutionary"
# Output: "revolutionary"
text = "Artificial Intelligence is revolutionary"
max_len = 0
long_word = ''
for word in text.split(" "):
    word_length = len(word)
    if word_length > max_len:
        max_len = word_length
        long_word = word
print(long_word)
```

### 19. Count Words Ending with 'e'
```python
# Input: "We love code in the evening"
# Output: 4
text = "We love code in the evening"
count_word = 0
for word in text.split(" "):
    if word[-1] == 'e':
        count_word += 1
print(count_word)
```

### 20. Remove All Digits
```python
# Input: "abc123def456"
# Output: "abcdef"
text = "abc123def456"
text2 = ''
for i in text:
    if i.isalpha():
        text2 += i
print(text2)
```

### 21. Character Count Dictionary
```python
# Input: "google"
# Output: {'g': 2, 'o': 2, 'l': 1, 'e': 1}
text = "google"
dict1 = {}
for i in text:
    if i in dict1:
        dict1[i] += 1
    else:
        dict1[i] = 1
print(dict1)
```

### 22. Remove All Vowels
```python
# Input: "Programming is exciting"
# Output: "Prgrmmng s xctng"
text = "Programming is exciting"
vowels = 'aeiou'
res = ''
for i in text:
    if i.lower() not in vowels:
        res += i
print(res)
```

### 23. Reverse Words in Sentence
```python
# Input: "I love Python"
# Output: "Python love I"
text = "I love Python"
word = text.split(" ")
rev_word = word[::-1]
result = " ".join(rev_word)
print(result)
```

### 24. Remove Duplicate Characters
```python
# Input: "programming"
# Output: "progamin"
text = "programming"
count_ch = ''
for ch in text:
    if ch not in count_ch:
        count_ch += ch
print(count_ch)
```

### 25. Replace nth Occurrence
```python
# Input: "test test test test", n=3, replace='exam'
# Output: "test test exam test"
text = "test test test test"
n = 3
words = text.split(" ")
words[n-1] = "exam"
result = " ".join(words)
print(result)
```

### 26. Title Case Conversion
```python
# Input: "wELCoMe TO PYthon"
# Output: "Welcome To Python"
text = "wELCoMe TO PYthon"
res = text.title()
print(res)
```

### 27. Swap Case
```python
# Input: "HeLLo WOrLD"
# Output: "hEllO woRld"
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
```

### 28. Mask Middle Digits
```python
# Input: "9876543210"
# Output: "98******10"
str1 = "9876543210"
str_output = str1[:2] + '*' * (len(str1) - 4) + str1[-2:]
print(str_output)
```

### 29. Reverse Each Word
```python
# Input: "Python is fun"
# Output: "nohtyP si nuf"
str1 = "Python is fun"
list_output = []
words = str1.strip().split()
for word in words:
    list_output.append(word[::-1])
string_output = ' '.join(list_output)
print(string_output)
```

### 30. Replace Vowels with *
```python
# Input: "Artificial Intelligence"
# Output: "*rt*f*c**l *nt*ll*g*nc*"
str1 = "Artificial Intelligence"
vowels = 'aeiouAEIOU'
string_output = ''
for ch in str1:
    if ch in vowels:
        string_output += '*'
    else:
        string_output += ch
print(string_output)
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
