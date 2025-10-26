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

### Q1. Mask Middle Digits
**Input:** "9876543210"  
**Output:** "98******10"
```python
# mask_middle_digits.py
s = "9876543210"
masked = s[:2] + '*' * (len(s) - 4) + s[-2:]
print(masked)

Output:
98******10
```
---

### Q2. Reverse Each Word
**Input:** "Python is fun"  
**Output:** "nohtyP si nuf"
```python
# reverse_each_word.py
s = "Python is fun"
words = s.split()
reversed_words = [w[::-1] for w in words]
print(" ".join(reversed_words))

Output:
nohtyP si nuf
```
---

### Q3. Replace Vowels with *
**Input:** "Artificial Intelligence"  
**Output:** "Art*f*c**l *nt*ll*g*nc*"
```python
# replace_vowels_star.py
s = "Artificial Intelligence"
vowels = 'aeiouAEIOU'
res = ''.join('*' if ch in vowels else ch for ch in s)
print(res)

Output:
Art*f*c**l *nt*ll*g*nc*
```
---

### Q4. Extract Digits Only
**Input:** "Room 24, Floor 7"  
**Output:** "247"
```python
# extract_digits.py
s = "Room 24, Floor 7"
digits = ''.join(ch for ch in s if ch.isdigit())
print(digits)

Output:
247
```
---

### Q5. Count Words in a Sentence
**Input:** "Data Science with Python"  
**Output:** 4
```python
# count_words.py
s = "Data Science with Python"
print(len(s.split()))

Output:
4
```
---

### Q6. First and Last Character Swap
**Input:** "HELLO"  
**Output:** "OELLH"
```python
# swap_first_last_char.py
s = "HELLO"
res = s[-1] + s[1:-1] + s[0]
print(res)

Output:
OELLH
```
---

### Q7. Convert Snake Case to Camel Case
**Input:** "machine_learning_project"  
**Output:** "machineLearningProject"
```python
# snake_to_camel.py
s = "machine_learning_project"
parts = s.split("_")
camel = parts[0] + ''.join(p.capitalize() for p in parts[1:])
print(camel)

Output:
machineLearningProject
```
---

### Q8. Palindrome Check
**Input:** "madam"  
**Output:** True
```python
# palindrome_check.py
s = "madam"
print(s == s[::-1])

Output:
True
```
---

### Q9. Remove Spaces from String
**Input:** " Hello World "  
**Output:** "HelloWorld"
```python
# remove_spaces.py
s = " Hello World "
cleaned = ''.join(s.split())
print(cleaned)

Output:
HelloWorld
```
---

### Q10. Replace First and Last Word with ****
**Input:** "Python makes programming easy"  
**Output:** "**** makes programming ****"
```python
# replace_first_last_word.py
s = "Python makes programming easy"
words = s.split()
words[0], words[-1] = "****", "****"
print(" ".join(words))

Output:
**** makes programming ****
```
---

### Q11. Reverse a List
**Input:** [1, 2, 3, 4, 5]  
**Output:** [5, 4, 3, 2, 1]
```python
# reverse_list.py
lst = [1, 2, 3, 4, 5]
print(lst[::-1])

Output:
[5, 4, 3, 2, 1]
```
---

### Q12. Find Maximum Element in a List
**Input:** [10, 25, 3, 99, 47]  
**Output:** 99
```python
# max_in_list.py
lst = [10, 25, 3, 99, 47]
print(max(lst))

Output:
99
```
---

### Q13. Remove Duplicates from a List
**Input:** [1, 2, 2, 3, 4, 4, 5]  
**Output:** [1, 2, 3, 4, 5]
```python
# remove_duplicates_list.py
lst = [1, 2, 2, 3, 4, 4, 5]
unique = []
for n in lst:
    if n not in unique:
        unique.append(n)
print(unique)

Output:
[1, 2, 3, 4, 5]
```
---

### Q14. Sum of All Elements in a List
**Input:** [5, 10, 15, 20]  
**Output:** 50
```python
# sum_of_elements.py
lst = [5, 10, 15, 20]
print(sum(lst))

Output:
50
```
---

### Q15. Find Even Numbers from a List
**Input:** [12, 7, 9, 14, 21, 6]  
**Output:** [12, 14, 6]
```python
# even_numbers_list.py
lst = [12, 7, 9, 14, 21, 6]
print([n for n in lst if n % 2 == 0])

Output:
[12, 14, 6]
```
---

### Q16. Find Longest Word in String
**Input:** "Artificial Intelligence is revolutionary"  
**Output:** "revolutionary"
```python
# longest_word.py
s = "Artificial Intelligence is revolutionary"
print(max(s.split(), key=len))

Output:
revolutionary
```
---

### Q17. Count Words That End with 'e'
**Input:** "We love code in the evening"  
**Output:** 4
```python
# words_ending_with_e.py
s = "We love code in the evening"
count = sum(1 for w in s.split() if w.endswith('e'))
print(count)

Output:
4
```
---

### Q18. Replace All Special Characters with #
**Input:** "Hello@World#2025!"  
**Output:** "Hello#World#2025#"
```python
# replace_special_chars.py
s = "Hello@World#2025!"
res = ''.join(ch if ch.isalnum() else '#' for ch in s)
print(res)

Output:
Hello#World#2025#
```
---

### Q19. Extract Digits from String
**Input:** "abc123xyz456"  
**Output:** "123456"
```python
# extract_digits_str.py
s = "abc123xyz456"
digits = ''.join(ch for ch in s if ch.isdigit())
print(digits)

Output:
123456
```
---

### Q20. Count Words Starting with Vowel
**Input:** "Apple is an orange fruit but mango is not"  
**Output:** 4
```python
# words_starting_with_vowel.py
s = "Apple is an orange fruit but mango is not"
vowels = 'aeiouAEIOU'
count = sum(1 for w in s.split() if w[0] in vowels)
print(count)

Output:
4
```
---

### Q21. Replace nth Occurrence of a Substring
**Input:** "test test test test", n=3, replace='exam'  
**Output:** "test test exam test"
```python
# replace_nth_occurrence.py
s = "test test test test"
n = 3
parts = s.split()
parts[n-1] = "exam"
print(" ".join(parts))

Output:
test test exam test
```
---

### Q22. Swap Case of Each Letter
**Input:** "HeLLo WOrLD"  
**Output:** "hEllO woRld"
```python
# swap_case.py
s = "HeLLo WOrLD"
print(''.join(ch.lower() if ch.isupper() else ch.upper() for ch in s))

Output:
hEllO woRld
```
---

### Q23. Reverse a String
**Input:** "Python"  
**Output:** "nohtyP"
```python
# reverse_string.py
s = "Python"
print(s[::-1])

Output:
nohtyP
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
