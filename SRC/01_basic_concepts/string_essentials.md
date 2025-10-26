<h1><sub><img src="https://github.com/RadhikaDeshpande1010/icon-library/blob/main/python-icon/python-icon.png" alt="Icon" height="27" width="27"></sub> Mastering Python Collections — Lists, Sets, and Strings </h1>

<h2>String Basics and Core Operations</h2>

This notebook provides a hands-on introduction to **Python strings** and their commonly used methods. It is designed for beginners to build a strong foundation in handling lists through step-by-step examples and exercises.

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

### Q1. Access each character in a string.

**Input:**
`str1 = "Hello"`

**Output:**
```
H
e
l
```

```python
# access_characters_in_string.py

str1 = "Hello"
print(str1[0])
print(str1[1])
print(str1[2])

Output:
H
e
l
```
---

### Q2. Find the length of a string.

**Input:**
`str1 = "Hello"`

**Output:** `5`

```python
# string_length.py

str1 = "Hello"
res = len(str1)
print(res)

Output:
5
```
---

### Q3. Slice characters from a string.

**Input:**
`str1 = "Hello How"`

**Output:** `ell`

```python
# slice_string.py

str1 = "Hello How"
res = str1[1:4]
print(res)

Output:
ell
```
---

### Q4. Get the last character of a string.

**Input:**
`str1 = "Hello"`

**Output:** `o`

```python
# last_character_of_string.py

str1 = "Hello"
res = str1[-1]
print(res)

Output:
o
```
---

### Q5. Check if a string contains only alphabets.

**Input:**
`str1 = "Hello"`

**Output:** `True`

```python
# string_isalpha.py

str1 = "Hello"
res = str1.isalpha()
print(res)

Output:
True
```
---

### Q6. Check if a string with numbers is alphabetic.

**Input:**
`str1 = "Hello 123"`

**Output:** `False`

```python
# string_isalpha_false.py

str1 = "Hello 123"
res = str1.isalpha()
print(res)

Output:
False
```
---

### Q7. Check if a string contains only digits.

**Input:**
`str1 = "123"`

**Output:** `True`

```python
# string_isdigit.py

str1 = "123"
res = str1.isdigit()
print(res)

Output:
True
```
---

### Q8. Find a substring in a string.

**Input:**
`str1 = "this is string example... wowo"`  
`str2 = "exam"`

**Output:** `15`

```python
# find_substring.py

str1 = "this is string example... wowo"
str2 = "exam"
res1 = str1.find(str2)
print(res1)

Output:
15
```
---

### Q9. Find a substring that does not exist.

**Input:**
`str1 = "this is string example... wowo"`  
`str2 = "oxam"`

**Output:** `-1`

```python
# find_nonexisting_substring.py

str1 = "this is string example... wowo"
str2 = "oxam"
res1 = str1.find(str2)
print(res1)

Output:
-1
```
---

### Q10. Check if a character exists in a string.

**Input:**
`str1 = "Hello how are you?"`  
`ch = "H"`

**Output:** `True`

```python
# check_character_in_string.py

str1 = "Hello how are you?"
ch = "H"
res1 = ch in str1
print(res1)

Output:
True
```
---

### Q11. Check if a character is not in a string.

**Input:**
`str1 = "Hello how are you?"`  
`ch = "n"`

**Output:** `True`

```python
# check_character_not_in_string.py

str1 = "Hello how are you?"
ch = "n"
res1 = ch not in str1
print(res1)

Output:
True
```
---

### Q12. Check if a string is in uppercase.

**Input:**
`str1 = "HELLO THIS IS PYTHON CLASS."`

**Output:** `True`

```python
# string_isupper.py

str1 = "HELLO THIS IS PYTHON CLASS."
res1 = str1.isupper()
print(res1)

Output:
True
```
---

### Q13. Check if a string is in lowercase.

**Input:**
`str1 = "hello this is python class"`

**Output:** `True`

```python
# string_islower.py

str1 = "hello this is python class"
res1 = str1.islower()
print(res1)

Output:
True
```
---

### Q14. Convert string to lowercase.

**Input:**
`str1 = "Hello"`

**Output:** `hello`

```python
# string_to_lowercase.py

str1 = "Hello"
res1 = str1.lower()
print(res1)

Output:
hello
```
---

### Q15. Convert string to uppercase.

**Input:**
`str1 = "Hello"`

**Output:** `HELLO`

```python
# string_to_uppercase.py

str1 = "Hello"
res1 = str1.upper()
print(res1)

Output:
HELLO
```
---

### Q16. Capitalize the first letter of a string.

**Input:**
`str1 = "hello how are you"`

**Output:** `Hello how are you`

```python
# capitalize_string.py

str1 = "hello how are you"
res1 = str1.capitalize()
print(res1)

Output:
Hello how are you
```
---

### Q17. Count occurrences of a character.

**Input:**
`str1 = "This is python class"`  
`character = "i"`

**Output:** `2`

```python
# count_character_in_string.py

str1 = "This is python class"
res1 = str1.count("i")
print(res1)

Output:
2
```
---

### Q18. Replace substring in a string.

**Input:**
`str1 = "This is python class"`  
`replace "is" with "was"`

**Output:** `Thwas was python class`

```python
# replace_substring.py

str1 = "This is python class"
res1 = str1.replace("is", "was")
print(res1)

Output:
Thwas was python class
```
---

### Q19. Split string into words.

**Input:**
`str1 = "This is python class"`

**Output:** `['This', 'is', 'python', 'class']`

```python
# split_string.py

str1 = "This is python class"
res1 = str1.split(" ")
print(res1)

Output:
['This', 'is', 'python', 'class']
```
---

### Q20. Reverse a string.

**Input:**
`str1 = "Hello"`

**Output:** `'olleH'`

```python
# reverse_string.py

str1 = "Hello"
rev = ""
for i in str1:
    rev = i + rev
print(rev)

Output:
olleH
```
---

### Q21. Remove white spaces from a string.

**Input:**
`str1 = "Hello W orld Th ere"`

**Output:** `HelloWorldThere`

```python
# remove_whitespace.py

str1 = "Hello W orld Th ere"
space_check = str1.replace(" ", "")
print(space_check)

Output:
HelloWorldThere
```
---

### Q22. Find duplicate characters in a string.

**Input:**
`str1 = "Hello"`

**Output:** `['l', 'l']`

```python
# duplicate_characters.py

str1 = "Hello"
dup = []
for i in str1:
    if str1.count(i) > 1:
        dup.append(i)
print(dup)

Output:
['l', 'l']
```
---

### Q23. Convert string to integer and vice versa.

**Input:**
`str1 = "123"`

**Output:**
```
123
<class 'int'>
123
<class 'str'>
```

```python
# string_to_int_and_back.py

str1 = "123"
x = int(str1)
print(x)
print(type(x))

y = str(x)
print(y)
print(type(y))

Output:
123
<class 'int'>
123
<class 'str'>
```
---

### Q24. Get index of all characters in a string.

**Input:**
`str1 = "Hello"`

**Output:**  
```
0
1
2
3
4
```

```python
# index_of_characters.py

str1 = "Hello"
for i in str1:
    index = str1.index(i)
    print(index)

Output:
0
1
2
3
4
```

### Conclusion

By the end of this notebook, you’ll have a solid grasp of strings fundamentals and essential methods that are building blocks for more advanced Python concepts.
