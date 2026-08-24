LeetCode Top Interview 150 — Pattern-Based DSA Roadmap

A pattern-first tracker for FAANG/MAANG internships, SDE roles, and technical interviews.
Focus on recognizing the underlying pattern rather than memorizing individual solutions.

🎯 Strategy

Recommended progression:

Arrays & Strings → Two Pointers → Sliding Window → HashMap → Stack → Linked List → Trees → Graphs → Backtracking → Binary Search → Heap → DP

GATE + LeetCode

LeetCode should be treated as a parallel interview-preparation track, not as a replacement for GATE preparation.

* GATE: concepts, correctness, complexity, mathematical reasoning, algorithm tracing
* LeetCode: implementation, pattern recognition, problem solving, coding speed
* Interview prep: combine both with timed practice and explanation

⸻

📊 Progress Tracker

Pattern	Problems	Status
Array / String	24	⬜
Two Pointers	5	⬜
Sliding Window	4	⬜
Matrix	5	⬜
HashMap	9	⬜
Intervals	4	⬜
Stack	5	⬜
Linked List	11	⬜
Binary Tree General	13	⬜
Binary Tree BFS	4	⬜
Binary Search Tree	3	⬜
Graph General	6	⬜
Graph BFS	3	⬜
Trie	3	⬜
Backtracking	7	⬜
Divide & Conquer	4	⬜
Kadane’s Algorithm	2	⬜
Binary Search	7	⬜
Heap	4	⬜
Bit Manipulation	6	⬜
Math	6	⬜
1D DP	5	⬜
Multidimensional DP	10	⬜
Total	150	0 / 150

⸻

01 — Array / String

* Merge Sorted Array
* Remove Element
* Remove Duplicates from Sorted Array
* Remove Duplicates from Sorted Array II
* Majority Element
* Rotate Array
* Best Time to Buy and Sell Stock
* Best Time to Buy and Sell Stock II
* Jump Game
* Jump Game II
* H-Index
* Insert Delete GetRandom O(1)
* Product of Array Except Self
* Gas Station
* Candy
* Trapping Rain Water
* Roman to Integer
* Integer to Roman
* Length of Last Word
* Longest Common Prefix
* Reverse Words in a String
* Zigzag Conversion
* Find the Index of the First Occurrence in a String
* Text Justification

Pattern focus: Two pointers, prefix/suffix, greedy, counting, simulation.

⸻

02 — Two Pointers

* Valid Palindrome
* Is Subsequence
* Two Sum II - Input Array Is Sorted
* Container With Most Water
* 3Sum

Pattern focus: Left/right pointers, sorted arrays, shrinking search space.

⸻

03 — Sliding Window

* Minimum Size Subarray Sum
* Longest Substring Without Repeating Characters
* Substring with Concatenation of All Words
* Minimum Window Substring

Pattern focus: Expand → maintain condition → shrink.

⸻

04 — Matrix

* Valid Sudoku
* Spiral Matrix
* Rotate Image
* Set Matrix Zeroes
* Game of Life

Pattern focus: Matrix traversal, coordinates, in-place modification.

⸻

05 — HashMap

* Ransom Note
* Isomorphic Strings
* Word Pattern
* Valid Anagram
* Group Anagrams
* Two Sum
* Happy Number
* Contains Duplicate II
* Longest Consecutive Sequence

Pattern focus: Frequency maps, lookup tables, grouping, O(1) average lookup.

⸻

06 — Intervals

* Summary Ranges
* Merge Intervals
* Insert Interval
* Minimum Number of Arrows to Burst Balloons

Pattern focus: Sorting + interval overlap.

⸻

07 — Stack

* Valid Parentheses
* Simplify Path
* Min Stack
* Evaluate Reverse Polish Notation
* Basic Calculator

Pattern focus: LIFO, expression evaluation, nested structures.

⸻

08 — Linked List

* Linked List Cycle
* Add Two Numbers
* Merge Two Sorted Lists
* Copy List with Random Pointer
* Reverse Linked List II
* Reverse Nodes in k-Group
* Remove Nth Node From End of List
* Remove Duplicates from Sorted List II
* Rotate List
* Partition List
* LRU Cache

Pattern focus: Fast/slow pointers, reversal, dummy nodes, pointer manipulation.

⸻

09 — Binary Tree General

* Maximum Depth of Binary Tree
* Same Tree
* Invert Binary Tree
* Symmetric Tree
* Construct Binary Tree from Preorder and Inorder Traversal
* Populating Next Right Pointers in Each Node II
* Flatten Binary Tree to Linked List
* Path Sum
* Sum Root to Leaf Numbers
* Binary Tree Maximum Path Sum
* BST Iterator
* Count Complete Tree Nodes
* Lowest Common Ancestor of a Binary Tree

Pattern focus: DFS, recursion, subtree information, tree traversal.

⸻

10 — Binary Tree BFS

* Binary Tree Right Side View
* Average of Levels in Binary Tree
* Binary Tree Level Order Traversal
* Binary Tree Zigzag Level Order Traversal

Pattern focus: Queue + level-by-level traversal.

⸻

11 — Binary Search Tree

* Minimum Absolute Difference in BST
* Kth Smallest Element in a BST
* Validate Binary Search Tree

Pattern focus: BST ordering + inorder traversal.

⸻

12 — Graph General

* Number of Islands
* Surrounded Regions
* Clone Graph
* Evaluate Division
* Course Schedule
* Course Schedule II

Pattern focus: DFS, BFS, visited sets, adjacency lists, topological sorting.

⸻

13 — Graph BFS

* Snakes and Ladders
* Minimum Genetic Mutation
* Word Ladder

Pattern focus: Shortest path in unweighted graphs.

⸻

14 — Trie

* Implement Trie
* Design Add and Search Words Data Structure
* Word Search II

Pattern focus: Prefix trees, character-by-character traversal.

⸻

15 — Backtracking

* Permutations
* Subsets
* Letter Combinations of a Phone Number
* Combination Sum
* N-Queens II
* Generate Parentheses
* Word Search

Pattern focus:

Choose
  ↓
Explore
  ↓
Undo
  ↓
Choose next

⸻

16 — Divide & Conquer

* Convert Sorted Array to Binary Search Tree
* Sort List
* Construct Quad Tree
* Merge k Sorted Lists

Pattern focus: Break → solve subproblems → combine.

⸻

17 — Kadane’s Algorithm

* Maximum Subarray
* Maximum Sum Circular Subarray

Pattern focus: Maintaining the best subarray ending at the current position.

⸻

18 — Binary Search

* Search Insert Position
* Search a 2D Matrix
* Find Peak Element
* Search in Rotated Sorted Array
* Find First and Last Position of Element in Sorted Array
* Find Minimum in Rotated Sorted Array
* Median of Two Sorted Arrays

Pattern focus: Reduce search space by half.

⸻

19 — Heap

* Kth Largest Element in an Array
* IPO
* Find K Pairs with Smallest Sums
* Find Median from Data Stream

Pattern focus: Priority queues, top-K, min/max heap.

⸻

20 — Bit Manipulation

* Add Binary
* Reverse Bits
* Number of 1 Bits
* Single Number
* Single Number II
* Bitwise AND of Numbers Range

Pattern focus: XOR, bit masks, shifts, binary representation.

⸻

21 — Math

* Palindrome Number
* Plus One
* Factorial Trailing Zeroes
* Sqrt(x)
* Pow(x, n)
* Max Points on a Line

Pattern focus: Mathematical observation + efficient implementation.

⸻

22 — 1D Dynamic Programming

* Climbing Stairs
* House Robber
* Word Break
* Coin Change
* Longest Increasing Subsequence

Pattern focus:

State
 ↓
Transition
 ↓
Base Case
 ↓
Answer

⸻

23 — Multidimensional Dynamic Programming

* Triangle
* Minimum Path Sum
* Unique Paths II
* Longest Palindromic Substring
* Interleaving String
* Edit Distance
* Best Time to Buy and Sell Stock III
* Best Time to Buy and Sell Stock IV
* Maximum Profit in Job Scheduling
* Regular Expression Matching

Pattern focus: 2D states, multiple dimensions, state transitions.

⸻

🧠 Pattern Recognition Cheat Sheet

If you see…	Think…
Sorted array + target	Binary Search / Two Pointers
Pair/triplet	HashMap / Two Pointers
Contiguous subarray	Sliding Window / Prefix Sum
Substring constraint	Sliding Window
Frequency/counting	HashMap
Matching brackets	Stack
Next greater/smaller	Monotonic Stack
Linked-list cycle	Fast + Slow Pointer
Reverse linked list	Pointer manipulation
Tree traversal	DFS / BFS
Level-by-level tree	BFS
Shortest unweighted path	BFS
Dependencies	Topological Sort
Explore every possibility	Backtracking
Top K	Heap
Repeated overlapping subproblems	DP
Best contiguous sum	Kadane
Prefix matching	Trie
Sorted search space	Binary Search
XOR / parity	Bit Manipulation

⸻

📈 Difficulty Progression

Phase 1 — Foundations

Arrays
  ↓
Strings
  ↓
HashMap
  ↓
Two Pointers
  ↓
Sliding Window

Phase 2 — Core Data Structures

Stack
  ↓
Linked List
  ↓
Trees
  ↓
BST
  ↓
Heap

Phase 3 — Algorithms

Binary Search
  ↓
Graphs
  ↓
Backtracking
  ↓
Divide & Conquer

Phase 4 — Advanced

Kadane
  ↓
1D DP
  ↓
2D DP
  ↓
Advanced DP

⸻

🔥 How To Solve Each Problem

Don’t simply solve → submit → move on.

Use this process:

1. Read the problem
        ↓
2. Identify the pattern
        ↓
3. Explain brute force
        ↓
4. Find the bottleneck
        ↓
5. Optimize
        ↓
6. Code
        ↓
7. Analyze Time Complexity
        ↓
8. Analyze Space Complexity
        ↓
9. Test edge cases
        ↓
10. Write down the key insight

Problem Notes Template

Problem:
Pattern:
Difficulty:
Brute Force:
Time:
Space:
Optimal Approach:
Time:
Space:
Key Insight:
Common Mistake:
Edge Cases:
Can I solve it without help?
[ ] Yes
[ ] No

⸻

🏆 Mastery Levels

Level 0 — Unseen

You have never encountered the problem.

⬜

Level 1 — Understand

You understand the problem but cannot derive the solution.

🟨

Level 2 — Assisted

You can solve it after seeing a hint.

🟧

Level 3 — Independent

You can solve it independently.

🟩

Level 4 — Fast

You can solve it within interview time.

🟦

Level 5 — Mastered

You recognize the pattern almost immediately and can explain the trade-offs.

🟪

⸻

⏱️ Daily LeetCode Routine

For 1–2 hours/day:

10 min  → Review yesterday's patterns
35 min  → Problem 1
35 min  → Problem 2
15 min  → Review solutions / mistakes
10 min  → Update notes

If a problem is taking too long:

Don’t spend 2 hours blindly stuck.

Use:

30–40 min attempt
       ↓
Small hint
       ↓
Try again
       ↓
Study solution if necessary
       ↓
Close solution
       ↓
Re-code from memory
       ↓
Revisit after 2–3 days

⸻

🎯 The Real Goal

The goal isn’t:

“I solved 150 LeetCode problems.”

The goal is:

“I can look at a new problem and identify the underlying pattern.”

For example:

New Problem
     ↓
What type of data?
     ↓
What constraints?
     ↓
What is being optimized?
     ↓
Is the data sorted?
     ↓
Contiguous?
     ↓
Frequency?
     ↓
Graph?
     ↓
Tree?
     ↓
Repeated subproblems?
     ↓
Recognize Pattern
     ↓
Choose Algorithm
     ↓
Implement

⸻

🚀 Final Target

                    LEETCODE TOP INTERVIEW 150
                              │
          ┌───────────────────┼───────────────────┐
          ↓                   ↓                   ↓
      Patterns            Algorithms         Data Structures
          │                   │                   │
          ↓                   ↓                   ↓
    Recognition          Complexity           Implementation
          │                   │                   │
          └───────────────────┼───────────────────┘
                              ↓
                       INTERVIEW READY

Target: 150 / 150

Primary objective: Pattern recognition
Secondary objective: Coding speed
Final objective: Solve unfamiliar problems under interview pressure.
