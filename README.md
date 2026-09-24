LeetCode Solutions – String, Matrix & Binary Tree Problems

This repository contains Java and Python solutions for selected LeetCode problems covering strings, hash maps, matrices, and binary trees. Each solution focuses on improving problem-solving skills, algorithmic thinking, and efficient implementation.

| No. | LeetCode | Problem                                                    | Difficulty | Language |
| --- | -------: | ---------------------------------------------------------- | ---------- | -------- |
| 01  |      290 | Word Pattern                                               | Easy       | Python   |
| 02  |      409 | Longest Palindrome                                         | Easy       | Java     |
| 03  |      387 | First Unique Character in a String                         | Easy       | Java     |
| 04  |       76 | Minimum Window Substring                                   | Hard       | Java     |
| 05  |       73 | Set Matrix Zeroes                                          | Medium     | Java     |
| 06  |      105 | Construct Binary Tree from Preorder and Inorder Traversal  | Medium     | Java     |
| 07  |      106 | Construct Binary Tree from Inorder and Postorder Traversal | Medium     | Java     |

1. LeetCode 290 – Word Pattern

File: Solution-01-290.python

Problem Description

Given a pattern and a string s, determine whether s follows the same pattern.

A pattern character must map to exactly one word, and each word must map back to exactly one pattern character.

Example
Input:
pattern = "abba"
s = "dog cat cat dog"

Output:
true
Approach
Split the string into individual words.
Check that the number of pattern characters equals the number of words.
Maintain mappings between:
pattern character → word
word → pattern character
Verify that the mapping remains consistent.
Complexity
Time: O(n)
Space: O(n)
2. LeetCode 409 – Longest Palindrome

File: Solution-02-409.java

Problem Description

Given a string containing uppercase and lowercase letters, find the length of the longest palindrome that can be built using those letters.

Example
Input:
"abccccdd"

Output:
7
Approach
Count the frequency of every character.
For every even frequency, use the entire count.
For every odd frequency, use the largest possible even portion.
If there is an unused odd character, one character can be placed in the center.
Complexity
Time: O(n)
Space: O(1)

The space is constant when the character set is fixed.

3. LeetCode 387 – First Unique Character in a String

File: Solution-03-387.java

Problem Description

Given a string, find the index of the first non-repeating character.

If no unique character exists, return -1.

Example
Input:
"leetcode"

Output:
0
Approach
Count the frequency of each character.
Traverse the string again.
Return the index of the first character whose frequency is 1.
If none exists, return -1.
Complexity
Time: O(n)
Space: O(1)
4. LeetCode 76 – Minimum Window Substring

File: Solution-04-76.java

Problem Description

Given strings s and t, find the smallest substring of s that contains all characters of t, including duplicate characters.

Example
Input:
s = "ADOBECODEBANC"
t = "ABC"

Output:
"BANC"
Approach

The solution uses the Sliding Window technique.

Count the required characters from t.
Expand the right side of the window.
Keep track of characters currently inside the window.
Once the window contains all required characters, move the left pointer forward.
Store the smallest valid window.
Complexity
Time: O(n)
Space: O(k)

Where k represents the number of distinct characters.

5. LeetCode 73 – Set Matrix Zeroes

File: Solution-05-73.java

Problem Description

Given an m × n matrix, if an element is 0, set its entire row and column to 0.

The transformation must be performed in-place.

Example
Input:
1 1 1
1 0 1
1 1 1

Output:
1 0 1
0 0 0
1 0 1
Approach

The first row and first column are used as markers.

Check whether the first row contains zero.
Check whether the first column contains zero.
Use the first row and first column to mark rows and columns that need to become zero.
Update the matrix from the inside.
Finally update the first row and first column if required.
Complexity
Time: O(m × n)
Space: O(1)
6. LeetCode 105 – Construct Binary Tree from Preorder and Inorder Traversal

File: Solution-06-105.java

Problem Description

Given the preorder and inorder traversal of a binary tree, construct the original binary tree.

Example
Preorder:
[3, 9, 20, 15, 7]

Inorder:
[9, 3, 15, 20, 7]

Output tree:

        3
       / \
      9   20
         /  \
        15   7
Approach
The first element in preorder is always the root.
Find the root's position in the inorder array.
Elements to the left belong to the left subtree.
Elements to the right belong to the right subtree.
Recursively construct both subtrees.

A HashMap can be used to quickly find the position of each value in the inorder traversal.

Complexity
Time: O(n)
Space: O(n)
7. LeetCode 106 – Construct Binary Tree from Inorder and Postorder Traversal

File: Solution-07-106.java

Problem Description

Given the inorder and postorder traversal of a binary tree, construct the original binary tree.

Example
Inorder:
[9, 3, 15, 20, 7]

Postorder:
[9, 15, 7, 20, 3]

Output:

        3
       / \
      9   20
         /  \
        15   7
Approach
The last element of postorder is the root.
Find the root in the inorder traversal.
Values before the root in inorder belong to the left subtree.
Values after the root belong to the right subtree.
Recursively construct the left and right subtrees.

A HashMap is used to find inorder positions efficiently.

Complexity
Time: O(n)
Space: O(n)
🧠 Concepts Covered

This collection helps practice several important DSA concepts:

HashMap
HashSet
Character Frequency
String Manipulation
Two-Pointer Technique
Sliding Window
Matrix Manipulation
In-place Algorithms
Recursion
Binary Trees
Tree Traversals
Preorder Traversal
Inorder Traversal
Postorder Traversal
Divide and Conquer
📂 Repository Structure
LeetCode-Solutions/
│
├── Solution-01-290.py
├── Solution-02-409.java
├── Solution-03-387.java
├── Solution-04-76.java
├── Solution-05-73.java
├── Solution-06-105.java
├── Solution-07-106.java
│
└── README.md
🎯 Learning Objectives

The main objectives of these solutions are:

Improve Java and Python programming skills.
Practice common LeetCode patterns.
Understand efficient string algorithms.
Learn frequency-based HashMap techniques.
Practice Sliding Window problems.
Understand in-place matrix manipulation.
Strengthen recursion and binary-tree concepts.
Improve time and space complexity analysis.
Prepare for coding interviews and online programming contests.
📊 Complexity Summary
Problem	Time Complexity	Space Complexity	Main Technique
290	O(n)	O(n)	HashMap
409	O(n)	O(1)	Frequency Counting
387	O(n)	O(1)	Frequency Counting
76	O(n)	O(k)	Sliding Window
73	O(m × n)	O(1)	In-place Matrix
105	O(n)	O(n)	Recursion + HashMap
106	O(n)	O(n)	Recursion + HashMap
🏆 Key Takeaways

This set provides practice across three major areas:

Strings

Word Pattern
Longest Palindrome
First Unique Character
Minimum Window Substring

Matrices

Set Matrix Zeroes

Binary Trees

Construct Tree from Preorder + Inorder
Construct Tree from Inorder + Postorder

These problems build a strong foundation for HashMap techniques, Sliding Window, recursion, matrix algorithms, and binary-tree construction.
