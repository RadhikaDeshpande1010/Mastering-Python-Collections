<h1><sub><img src="https://github.com/RadhikaDeshpande1010/icon-library/blob/main/python-icon/python-icon.png" alt="Icon" height="27" width="27"></sub> Mastering Python Collections — Lists, Sets, and Strings </h1>

<h2>List Manipulation and Comprehensions</h2>

This notebook provides a hands-on introduction to List Manipulation and Comprehensions in Python. It is designed for learners to strengthen their understanding of how to efficiently modify, transform, and generate lists using both traditional techniques and Pythonic list comprehensions. Through step-by-step examples and exercises, you’ll gain practical experience in writing concise, optimized, and readable list-based code.

> **Python version:** 3.8+

---

### 🔍 Introduction to List Manipulation and Comprehensions in Python
In Python, lists are one of the most versatile and widely used data structures—perfect for storing sequences of items, whether numbers, strings, or complex objects. Efficient handling of lists is essential for writing clean, readable, and performant code.

**List manipulation** refers to the various operations we can perform on lists, such as adding, removing, slicing, filtering, and transforming elements. These techniques form the backbone of data wrangling and algorithmic logic in Python applications.

**List comprehensions**, on the other hand, offer a concise and expressive way to construct new lists by iterating over existing ones. They combine looping and conditional logic into a single elegant line, making your code more Pythonic and often more efficient.

Whether you're cleaning datasets, transforming inputs, or building dynamic structures, mastering list manipulation and comprehensions will elevate your Python skills and streamline your workflows.

---

### How to Run

1. **Clone** this repository and open the folder in your editor/terminal.
2. Start Jupyter Notebook:

   ```bash
    jupyter notebook
   ```

> Tip: You can also copy any solution function into your notebook/REPL to experiment quickly.

---

### Q1. Print all negative elements in a list.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** -98, -30  
```python
# negative_elements_in_list.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
for i in list1:
    if i < 0:
        print(i)

Output:
-98
-30
```
---

### Q2. Find the sum of all list elements.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** 124  
```python
# sum_of_list.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
sum = 0
for i in list1:
    sum = sum + i
print(sum)

Output:
124
```
---

### Q3. Find maximum and minimum element in a list.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** 76  
```python
# max_min_in_list.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
max_num = list1[0]
for i in list1:
    if i > max_num:
        max_num = i
print(max_num)

Output:
76
```
---

### Q4. Find second largest element in a list.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** 56  
```python
# second_largest_in_list.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
sorted_list = sorted(list1)
result = sorted_list[-2]
print(result)

Output:
56
```
---

### Q5. Count total number of even and odd elements in a list.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** Even=6, Odd=2  
```python
# even_odd_count.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
even_list = []
odd_list = []
for i in list1:
    if i % 2 == 0:
        even_list.append(i)
    else:
        odd_list.append(i)
print("Even element list:", even_list)
print("Odd element list:", odd_list)
print("Count of total numbers in even list:", len(even_list))
print("Count of total numbers in odd list:", len(odd_list))

Output:
Even element list: [56, -98, 12, -30, 76, 34]
Odd element list: [51, 23]
Count of total numbers in even list: 6
Count of total numbers in odd list: 2
```
---

### Q6. Count total number of negative elements in a list.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** 2  
```python
# negative_count.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
negative_list = [i for i in list1 if i < 0]
print(len(negative_list))

Output:
2
```
---

### Q7. Copy all elements from one list to another.
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** [56, -98, 12, -30, 76, 51, 23, 34]  
```python
# copy_list.py
list1 = [56, -98, 12, -30, 76, 51, 23, 34]
list2 = list1.copy()
print(list2)

Output:
[56, -98, 12, -30, 76, 51, 23, 34]
```
---

### Q8. Remove duplicates from a list.
**Input:** [56, -98, 12, 12, -30, -30, 76, 51, 23, 23, 34, 34]  
**Output:** [56, -98, 12, -30, 76, 51, 23, 34]  
```python
# remove_duplicates.py
list1 = [56, -98, 12, 12, -30, -30, 76, 51, 23, 23, 34, 34]
list2 = []
for i in list1:
    if i not in list2:
        list2.append(i)
print(list2)

Output:
[56, -98, 12, -30, 76, 51, 23, 34]
```
---

### Q9. Find the list of words that are longer than n.
**Input:** ["Hello", "how", "are", "there"]  
**Output:** Hello 5, there 5  
```python
# words_longer_than_n.py
list1 = ["Hello", "how", "are", "there"]
dict1 = {i: len(i) for i in list1}
max_val = max(dict1.values())
for key, value in dict1.items():
    if value == max_val:
        print(key, value)

Output:
Hello 5
there 5
```
---

## Surprise Test Programs

### Q10. Join characters with a dash.
**Input:** "code"  
**Output:** "c-o-d-e"  
```python
# join_characters_with_dash.py
text = "code"
result = "-".join(text)
print(result)

Output:
c-o-d-e
```
---

### Q11. Find second largest in list.
**Input:** [5, 2, 9, 1, 7]  
**Output:** 7  
```python
# second_largest_number.py
text = [5, 2, 9, 1, 7]
sorted_text = sorted(text)
print(sorted_text[-2])

Output:
7
```
---

### Q12. Count specific character in string.
**Input:** ("mississippi", "s")  
**Output:** 4  
```python
# count_specific_character.py
word = "mississippi"
count_s = word.count('s')
print(count_s)

Output:
4
```
---

### Q13. Flatten a nested list.
**Input:** [[1, 2], [3, 4], [5]]  
**Output:** [1, 2, 3, 4, 5]  
```python
# flatten_nested_list.py
list1 = [[1, 2], [3, 4], [5]]
list2 = []
for i in list1:
    for j in i:
        list2.append(j)
print(list2)

Output:
[1, 2, 3, 4, 5]
```
---

### Q14. Filter words by length.
**Input:** (["dog", "elephant", "cat", "tiger"], 3)  
**Output:** ["elephant", "tiger"]  
```python
# filter_words_by_length.py
text = ["dog", "elephant", "cat", "tiger"]
result = [word for word in text if len(word) > 3]
print(result)

Output:
['elephant', 'tiger']
```
---

### Q15. Merge two lists alternately.
**Input:** [1, 2, 3], ['a', 'b', 'c']  
**Output:** [1, 'a', 2, 'b', 3, 'c']  
```python
# merge_lists_alternately.py
list1 = [1, 2, 3]
list2 = ['a', 'b', 'c']
merge_list = []
for i1, i2 in zip(list1, list2):
    merge_list.append(i1)
    merge_list.append(i2)
print(merge_list)

Output:
[1, 'a', 2, 'b', 3, 'c']
```
---

### Q16. Rotate list right by one position.
**Input:** [1, 2, 3, 4]  
**Output:** [4, 1, 2, 3]  
```python
# rotate_list_right.py
text = [1, 2, 3, 4]
list3 = text[-1:] + text[:-1]
print(list3)

Output:
[4, 1, 2, 3]
```
---

### Q17. Convert string to list of words.
**Input:** "Data science is fun"  
**Output:** ["Data", "science", "is", "fun"]  
```python
# string_to_list_of_words.py
text = "Data science is fun"
words = text.split(" ")
print(words)

Output:
['Data', 'science', 'is', 'fun']
```
---

### Q18. Find strings that start and end with same character.
**Input:** ["level", "data", "apple", "radar"]  
**Output:** ["level", "radar"]  
```python
# same_start_end_strings.py
text = ["level", "data", "apple", "radar"]
result = [word for word in text if word[0] == word[-1]]
print(result)

Output:
['level', 'radar']
```
---

### Q19. Extract digits from a string.
**Input:** "a1b2c3d"  
**Output:** [1, 2, 3]  
```python
# extract_digits_from_string.py
text = "a1b2c3d"
result = [int(ch) for ch in text if ch.isdigit()]
print(result)

Output:
[1, 2, 3]
```
---

### Q20. Remove empty strings from list.
**Input:** ["hello", "", "world", "", "python"]  
**Output:** ["hello", "world", "python"]  
```python
# remove_empty_strings.py
text = ["hello", "", "world", "", "python"]
result = [word for word in text if word]
print(result)

Output:
['hello', 'world', 'python']
```
---

### Q21. Sort list by string length.
**Input:** ["banana", "apple", "fig", "grape"]  
**Output:** ["fig", "apple", "grape", "banana"]  
```python
# sort_list_by_length.py
text = ["banana", "apple", "fig", "grape"]
sorted_list = sorted(text, key=len)
print(sorted_list)

Output:
['fig', 'apple', 'grape', 'banana']
```
---

### Q22. Convert list to string without spaces.
**Input:** ["Python", "is", "awesome"]  
**Output:** "Pythonisawesome"  
```python
# list_to_string.py
text = ["Python", "is", "awesome"]
string = ''.join(text)
print(string)

Output:
Pythonisawesome
```
---

### Q23. Find unique characters in a string.
**Input:** "programming"  
**Output:** ['p', 'r', 'o', 'g', 'a', 'm', 'i', 'n']  
```python
# unique_characters_in_string.py
text = "programming"
unique_char_list = list(set(text))
print(unique_char_list)

Output:
['p', 'r', 'o', 'g', 'a', 'm', 'i', 'n']
```
---

### Q24. Split list into chunks.
**Input:** ([1, 2, 3, 4, 5, 6], 2)  
**Output:** [[1, 2], [3, 4], [5, 6]]  
```python
# split_list_into_chunks.py
list1 = [1, 2, 3, 4, 5, 6]
size = 2
result = [list1[i:i+size] for i in range(0, len(list1), size)]
print(result)

Output:
[[1, 2], [3, 4], [5, 6]]
```
---

This collection of Python practice programs covers essential concepts of lists and strings, ranging from basic operations to intermediate-level problem-solving.
Each example is designed to strengthen logical thinking, enhance coding fluency, and prepare for real-world interview or test scenarios.

By completing these exercises, you’ll gain confidence in:

Handling lists, strings, and nested structures efficiently

Applying loops, conditionals, and built-in functions

Writing clean, modular, and Pythonic code

💡 Next Step: Try modifying each program to accept user input and handle edge cases — this will deepen your understanding and improve your Python skills further.
