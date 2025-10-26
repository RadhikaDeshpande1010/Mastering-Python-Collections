<h1><sub><img src="https://github.com/RadhikaDeshpande1010/icon-library/blob/main/python-icon/python-icon.png" alt="Icon" height="27" width="27"></sub> Mastering Python Collections — Lists, Sets, and Strings </h1>

<h2>String Operations and Practice</h2>

This notebook This module — String Operations and Practice — is part of the Intermediate Concepts series and focuses on strengthening Python string manipulation skills through hands-on examples.

It contains a curated collection of frequently used string and list operations designed for practical understanding and interview readiness. Each question is self-contained, with clear input–output examples and executable Python code.

💡 Learning Objectives

Strengthen understanding of string handling and transformations

Practice Pythonic ways to manipulate text data efficiently

Apply loops, conditions, and comprehensions for string logic

Develop confidence in solving interview-style coding problems

🧩 Structure

This file includes:

Reversal, counting, and search-based string problems

String–list combined operations

Case conversion and formatting exercises

Practical examples relevant to real-world use cases

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

### Q1. Reverse a string
**Input:** "hello"  
**Output:** "olleh"
```python
# reverse_string.py
s = "hello"
print(s[::-1])

Output:
olleh
```
---

### Q2. Count vowels in a string
**Input:** "OpenAI"  
**Output:** 4
```python
# count_vowels.py
s = "OpenAI"
vowels = "aeiouAEIOU"
count = sum(1 for ch in s if ch in vowels)
print(count)

Output:
4
```
---

### Q3. Check if the string is a palindrome (case-insensitive)
**Input:** "Madam"  
**Output:** True
```python
# is_palindrome.py
s = "Madam"
t = s.lower()
print(t == t[::-1])

Output:
True
```
---

### Q4. Convert string to uppercase
**Input:** "python"  
**Output:** "PYTHON"
```python
# to_uppercase.py
s = "python"
print(s.upper())

Output:
PYTHON
```
---

### Q5. Replace all spaces with hyphens
**Input:** "data science is fun"  
**Output:** "data-science-is-fun"
```python
# replace_spaces_with_hyphens.py
s = "data science is fun"
print(s.replace(" ", "-"))

Output:
data-science-is-fun
```
---

### Q6. Find the length of a string
**Input:** "artificial"  
**Output:** 10
```python
# string_length.py
s = "artificial"
print(len(s))

Output:
10
```
---

### Q7. Check if a word is present in a string
**Input:** String="I love machine learning", Word="machine"  
**Output:** True
```python
# word_present.py
s = "I love machine learning"
w = "machine"
print(w in s)

Output:
True
```
---

### Q8. Count the number of words in a sentence
**Input:** "Python is easy to learn"  
**Output:** 5
```python
# word_count.py
s = "Python is easy to learn"
print(len(s.split()))

Output:
5
```
---

### Q9. Remove all digits from the string
**Input:** "abc123xyz456"  
**Output:** "abcxyz"
```python
# remove_digits.py
s = "abc123xyz456"
clean = ''.join(ch for ch in s if ch.isalpha())
print(clean)

Output:
abcxyz
```
---

### Q10. Swap case of a string (upper ↔ lower)
**Input:** "PyTHon123"  
**Output:** "pYthON123"
```python
# swap_case.py
s = "PyTHon123"
print(''.join(ch.lower() if ch.isupper() else ch.upper() for ch in s))

Output:
pYthON123
```
---

### Q11. Most frequent character (ignore spaces)
**Input:** "hello world"  
**Output:** "l"
```python
# most_frequent_char.py
s = "hello world".replace(" ", "")
max_char = max(set(s), key=s.count)
print(max_char)

Output:
l
```
---

### Q12. Remove all special characters (keep letters, digits, and spaces)
**Input:** "he@ll#o! w$o^r%l&d"  
**Output:** "hello world"
```python
# remove_special_chars.py
s = "he@ll#o! w$o^r%l&d"
clean = ''.join(ch for ch in s if ch.isalnum() or ch.isspace())
print(clean)

Output:
hello world
```
---

### Q13. Capitalize the first letter of each word
**Input:** "machine learning with python"  
**Output:** "Machine Learning With Python"
```python
# capitalize_each_word.py
s = "machine learning with python"
print(' '.join(w.capitalize() for w in s.split()))

Output:
Machine Learning With Python
```
---

### Q14. Find all duplicate characters in a string
**Input:** "programming"  
**Output:** ['g', 'm', 'r']
```python
# duplicate_characters.py
s = "programming"
dups = sorted({ch for ch in set(s) if s.count(ch) > 1})
print(dups)

Output:
['g', 'm', 'r']
```
---

### Q15. Count uppercase and lowercase characters
**Input:** "PyThOn"  
**Output:** Uppercase: 3, Lowercase: 3
```python
# count_upper_lower.py
s = "PyThOn"
u = sum(1 for ch in s if ch.isupper())
l = sum(1 for ch in s if ch.islower())
print("Uppercase:", u)
print("Lowercase:", l)

Output:
Uppercase: 3
Lowercase: 3
```
---

### Q16. Replace the first occurrence of a word
**Input:** "the sky is blue and the ocean is blue", replace "blue"→"green"  
**Output:** "the sky is green and the ocean is blue"
```python
# replace_first_occurrence.py
s = "the sky is blue and the ocean is blue"
print(s.replace("blue", "green", 1))

Output:
the sky is green and the ocean is blue
```
---

### Q17. Check if a string contains only digits
**Input:** "123456"  
**Output:** True
```python
# only_digits.py
s = "123456"
print(s.isdigit())

Output:
True
```
---

### Q18. Find the longest word in a sentence
**Input:** "AI is transforming the world rapidly"  
**Output:** "transforming"
```python
# longest_word_in_sentence.py
s = "AI is transforming the world rapidly"
words = s.split()
print(max(words, key=len))

Output:
transforming
```
---

### Q19. Reverse each word in a list
**Input:** ["hello", "world"]  
**Output:** ["olleh", "dlrow"]
```python
# reverse_each_word_list.py
lst = ["hello", "world"]
print([w[::-1] for w in lst])

Output:
['olleh', 'dlrow']
```
---

### Q20. Capitalize words in a list
**Input:** ["apple", "banana", "grape"]  
**Output:** ["Apple", "Banana", "Grape"]
```python
# capitalize_words_list.py
lst = ["apple", "banana", "grape"]
print([w.capitalize() for w in lst])

Output:
['Apple', 'Banana', 'Grape']
```
---

### Q21. Filter words starting with a vowel
**Input:** ["apple", "banana", "orange", "grape", "umbrella"]  
**Output:** ["apple", "orange", "umbrella"]
```python
# filter_words_starting_vowel.py
lst = ["apple", "banana", "orange", "grape", "umbrella"]
v = set("aeiouAEIOU")
print([w for w in lst if w[0] in v])

Output:
['apple', 'orange', 'umbrella']
```
---

### Q22. Remove duplicate words
**Input:** ["pen", "book", "pen", "note", "book"]  
**Output:** ["pen", "book", "note"]
```python
# remove_duplicate_words.py
lst = ["pen", "book", "pen", "note", "book"]
res = []
for w in lst:
    if w not in res:
        res.append(w)
print(res)

Output:
['pen', 'book', 'note']
```
---

### Q23. Count total characters across all words
**Input:** ["cat", "dog", "fish"]  
**Output:** 10
```python
# total_characters_in_list.py
lst = ["cat", "dog", "fish"]
print(sum(len(w) for w in lst))

Output:
10
```
---

### Q24. Join words with hyphen
**Input:** ["data", "science", "python"]  
**Output:** "data-science-python"
```python
# join_words_with_hyphen.py
lst = ["data", "science", "python"]
print("-".join(lst))

Output:
data-science-python
```
---

### Q25. Find longest word in a list
**Input:** ["sun", "moon", "earth", "jupiter"]  
**Output:** "jupiter"
```python
# longest_word_in_list.py
lst = ["sun", "moon", "earth", "jupiter"]
print(max(lst, key=len))

Output:
jupiter
```
---

### Q26. Get words with length ≥ 4
**Input:** ["box", "window", "sky", "frame"]  
**Output:** ["window", "frame"]
```python
# words_length_gte_4.py
lst = ["box", "window", "sky", "frame"]
print([w for w in lst if len(w) >= 4])

Output:
['window', 'frame']
```
---

### Q27. Count words ending with 'e'
**Input:** ["love", "hate", "free", "file", "cat"]  
**Output:** 4
```python
# count_words_ending_e.py
lst = ["love", "hate", "free", "file", "cat"]
print(sum(1 for w in lst if w.endswith('e')))

Output:
4
```
---

### Q28. Sort words alphabetically
**Input:** ["zebra", "apple", "monkey"]  
**Output:** ["apple", "monkey", "zebra"]
```python
# sort_words_alpha.py
lst = ["zebra", "apple", "monkey"]
print(sorted(lst))

Output:
['apple', 'monkey', 'zebra']
```
---

### Q29. Reverse all words in a sentence and join with "-"
**Input:** "Python is powerful"  
**Output:** "nohtyP-si-lufrewop"
```python
# reverse_words_join_dash.py
s = "Python is powerful"
parts = s.split()
rev = [w[::-1] for w in parts]
print("-".join(rev))

Output:
nohtyP-si-lufrewop
```
---

### Q30. Remove all vowels from a list of words
**Input:** ["apple", "banana", "grape"]  
**Output:** ["ppl", "bnn", "grp"]
```python
# remove_vowels_from_words.py
lst = ["apple", "banana", "grape"]
vowels = set("aeiouAEIOU")
def strip_vowels(w): return ''.join(ch for ch in w if ch not in vowels)
print([strip_vowels(w) for w in lst])

Output:
['ppl', 'bnn', 'grp']
```
---

### Q31. Check palindromes in a list of strings
**Input:** ["madam", "apple", "racecar", "hello"]  
**Output:** [True, False, True, False]
```python
# list_palindromes.py
lst = ["madam", "apple", "racecar", "hello"]
print([w == w[::-1] for w in lst])

Output:
[True, False, True, False]
```
---

### Q32. Remove duplicate characters in a string (keep first occurrence)
**Input:** "success"  
**Output:** "suce"
```python
# remove_duplicate_chars_keep_first.py
s = "success"
seen = set()
out = []
for ch in s:
    if ch not in seen:
        seen.add(ch)
        out.append(ch)
print(''.join(out))

Output:
suce
```
---

### Q33. Find common characters in two strings (sorted list)
**Input:** "database", "backend"  
**Output:** ['a', 'b', 'd', 'e']
```python
# common_characters_sorted.py
a, b = "database", "backend"
res = sorted(set(a) & set(b))
print(res)

Output:
['a', 'b', 'd', 'e']
```
---

### Q34. Build a dict of word → length from a list
**Input:** ["code", "python", "AI"]  
**Output:** {'code': 4, 'python': 6, 'AI': 2}
```python
# word_length_dict.py
lst = ["code", "python", "AI"]
print({w: len(w) for w in lst})

Output:
{'code': 4, 'python': 6, 'AI': 2}
```
---

### Q35. Count words that start and end with the same character
**Input:** ["refer", "apple", "wow", "data"]  
**Output:** 2
```python
# count_same_start_end.py
lst = ["refer", "apple", "wow", "data"]
print(sum(1 for w in lst if w[0] == w[-1]))

Output:
2
```
---

### Q36. Join characters of a string with a dash
**Input:** "code"  
**Output:** "c-o-d-e"
```python
# join_characters_with_dash.py
s = "code"
print("-".join(s))

Output:
c-o-d-e
```
---

### Q37. Print all negative elements in a list
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** -98, -30
```python
# negative_elements.py
lst = [56, -98, 12, -30, 76, 51, 23, 34]
for n in lst:
    if n < 0:
        print(n)

Output:
-98
-30
```
---

### Q38. Sum of all list elements
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** 124
```python
# sum_of_list.py
lst = [56, -98, 12, -30, 76, 51, 23, 34]
print(sum(lst))

Output:
124
```
---

### Q39. Find maximum and minimum element in a list
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** max=76, min=-98
```python
# max_min_list.py
lst = [56, -98, 12, -30, 76, 51, 23, 34]
print(max(lst), min(lst))

Output:
76 -98
```
---

### Q40. Find second largest element in a list
**Input:** [5, 2, 9, 1, 7]  
**Output:** 7
```python
# second_largest.py
lst = [5, 2, 9, 1, 7]
print(sorted(lst)[-2])

Output:
7
```
---

### Q41. Count even and odd elements in a list
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** Even=6, Odd=2
```python
# count_even_odd.py
lst = [56, -98, 12, -30, 76, 51, 23, 34]
ev = sum(1 for n in lst if n % 2 == 0)
od = len(lst) - ev
print("Even:", ev)
print("Odd:", od)

Output:
Even: 6
Odd: 2
```
---

### Q42. Count total number of negative elements in a list
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** 2
```python
# count_negatives.py
lst = [56, -98, 12, -30, 76, 51, 23, 34]
print(sum(1 for n in lst if n < 0))

Output:
2
```
---

### Q43. Copy all elements from one list to another
**Input:** [56, -98, 12, -30, 76, 51, 23, 34]  
**Output:** [56, -98, 12, -30, 76, 51, 23, 34]
```python
# copy_list.py
lst = [56, -98, 12, -30, 76, 51, 23, 34]
copy_lst = lst.copy()
print(copy_lst)

Output:
[56, -98, 12, -30, 76, 51, 23, 34]
```
---

### Q44. Remove duplicates from a numeric list
**Input:** [56, -98, 12, 12, -30, -30, 76, 51, 23, 23, 34, 34]  
**Output:** [56, -98, 12, -30, 76, 51, 23, 34]
```python
# remove_duplicates_list.py
lst = [56, -98, 12, 12, -30, -30, 76, 51, 23, 23, 34, 34]
res = []
for n in lst:
    if n not in res:
        res.append(n)
print(res)

Output:
[56, -98, 12, -30, 76, 51, 23, 34]
```
---

### Q45. Extract digits from a string as a list
**Input:** "a1b2c3d"  
**Output:** [1, 2, 3]
```python
# extract_digits.py
s = "a1b2c3d"
print([int(ch) for ch in s if ch.isdigit()])

Output:
[1, 2, 3]
```
---

### Q46. Remove empty strings from a list
**Input:** ["hello", "", "world", "", "python"]  
**Output:** ["hello", "world", "python"]
```python
# remove_empty_strings.py
lst = ["hello", "", "world", "", "python"]
print([w for w in lst if w])

Output:
['hello', 'world', 'python']
```
---

### Q47. Sort list by string length
**Input:** ["banana", "apple", "fig", "grape"]  
**Output:** ["fig", "apple", "grape", "banana"]
```python
# sort_by_length.py
lst = ["banana", "apple", "fig", "grape"]
print(sorted(lst, key=len))

Output:
['fig', 'apple', 'grape', 'banana']
```
---

### Q48. Convert list to string without spaces
**Input:** ["Python", "is", "awesome"]  
**Output:** "Pythonisawesome"
```python
# list_to_string_no_spaces.py
lst = ["Python", "is", "awesome"]
print(''.join(lst))

Output:
Pythonisawesome
```
---

### Q49. First non-repeating character in a string
**Input:** "aabbcddeeff"  
**Output:** "c"
```python
# first_non_repeating_char.py
s = "aabbcddeeff"
for ch in s:
    if s.count(ch) == 1:
        print(ch)
        break

Output:
c
```
---

### Q50. Remove punctuation from a string
**Input:** "Hello, world!"  
**Output:** "Hello world"
```python
# remove_punctuation.py
s = "Hello, world!"
punct = ",.!?;:'"-()[]{}"
clean = ''.join(ch for ch in s if ch not in punct)
print(clean)

Output:
Hello world
```
---

### Q51. Flatten a nested list (one level deep)
**Input:** [[1, 2], [3, 4], [5]]  
**Output:** [1, 2, 3, 4, 5]
```python
# flatten_one_level.py
nested = [[1, 2], [3, 4], [5]]
flat = [x for sub in nested for x in sub]
print(flat)

Output:
[1, 2, 3, 4, 5]
```
---

### Q52. Merge two lists alternately
**Input:** [1, 2, 3], ['a', 'b', 'c']  
**Output:** [1, 'a', 2, 'b', 3, 'c']
```python
# merge_alternate.py
a = [1, 2, 3]
b = ['a', 'b', 'c']
out = []
for x, y in zip(a, b):
    out.extend([x, y])
print(out)

Output:
[1, 'a', 2, 'b', 3, 'c']
```
---

### Q53. Rotate a list to the right by one
**Input:** [1, 2, 3, 4]  
**Output:** [4, 1, 2, 3]
```python
# rotate_right_one.py
lst = [1, 2, 3, 4]
print(lst[-1:] + lst[:-1])

Output:
[4, 1, 2, 3]
```
---

### Q54. Split list into chunks of given size
**Input:** ([1, 2, 3, 4, 5, 6], 2)  
**Output:** [[1, 2], [3, 4], [5, 6]]
```python
# split_into_chunks.py
lst = [1, 2, 3, 4, 5, 6]
size = 2
print([lst[i:i+size] for i in range(0, len(lst), size)])

Output:
[[1, 2], [3, 4], [5, 6]]
```
---

### ✅Conclusion

This practice file brought together key string manipulation techniques—from simple tasks like reversing and formatting to more advanced operations such as encoding, filtering, and pattern-based logic. Each exercise was designed to reinforce practical skills and deepen your understanding of how Python handles textual data.
By completing these challenges, you’ve strengthened your ability to:
- Work confidently with strings, lists, and nested structures
- Apply Pythonic logic using built-in functions and list comprehensions
- Tackle real-world and interview-style problems with clarity and precision
  
🚀 What’s Next?

Keep building momentum by diving into the next module in the Intermediate Concepts track:
Set Manipulation and Applications — where you’ll explore deduplication, membership testing, and efficient data filtering using Python sets.
