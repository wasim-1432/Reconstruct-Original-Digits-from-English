# LeetCode – Original Digits (C++)

## Problem Description
Given a string `s` containing English letters in lowercase, the task is to reconstruct the original digits (0–9) and return them in ascending order.

Each digit is represented by its English word:
- 0 → zero
- 1 → one
- 2 → two
- 3 → three
- 4 → four
- 5 → five
- 6 → six
- 7 → seven
- 8 → eight
- 9 → nine

## Approach: Hashing + Frequency Counting

I used an `unordered_map<char, int>` to maintain the frequency of every character in the given string.

### Steps:
1. Traverse the input string and store the frequency of each character in an unordered map.
2. Check whether the characters required to form a particular digit are available.
3. If a digit can be formed:
   - Add that digit to the answer.
   - Decrease the frequency of its corresponding characters.
   - Remove characters from the map when their frequency becomes zero using `erase()`.
4. Repeat the process until no more digits can be extracted.
5. Return the constructed answer.

## C++ Concepts Used
- `unordered_map`
- Hashing
- Character Frequency Counting
- `find()` Function
- `erase()` Function
- String Manipulation
- Loops and Conditional Statements

## Code
The solution is implemented in C++ using an unordered map for character frequency management.

## Complexity Analysis

Let `n` be the length of the input string.

- **Time Complexity:** O(n) expected for frequency counting and digit extraction, assuming a fixed alphabet and bounded number of digit types.
- **Space Complexity:** O(1), since the unordered map stores at most 26 lowercase English characters.

## Learning Outcomes
- Practiced character frequency counting using hashing.
- Learned how to delete specific keys from an unordered map.
- Improved understanding of string manipulation and greedy digit extraction.

---

**Language:** C++

**Platform:** LeetCode

**Topic:** Hashing | String | Greedy | Unordered Map
