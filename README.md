# LeetCode Mastery Protocol

> A structured, zero-to-competent system for learning Data Structures, Algorithms, and problem-solving patterns — built for depth, not random grinding.

15 Core Patterns · 6 Phases · ~16 Weeks · Patterns > Problem Count

⸻

01 — The Mental Model

Why Most People Fail

The default approach:

Open LeetCode
   ↓
Solve #1
   ↓
Solve #2
   ↓
Solve #3
   ↓
Repeat...

This often teaches you individual solutions, not reusable problem-solving patterns.

You may solve 300 random problems but still get stuck when a new problem uses a familiar idea in an unfamiliar way.

The Pattern Model

Instead:

Learn a pattern
      ↓
Understand WHY it works
      ↓
Solve 5–8 representative problems
      ↓
Re-solve them later
      ↓
Recognize the pattern in unseen problems

The goal is compression rather than memorization.

Core principle: Patterns > Problem Count


⸻


02 — Foundation Map

Before pattern-based LeetCode practice, build these foundations.

Foundation	Must Know	Suggested Time
Complexity / Big-O	Time, space, best/average/worst case, amortized cost	2–3 days
Arrays & Strings	In-place operations, prefix sums, sorting, two pointers	1 week
Hashing	HashMap/Set, lookup complexity, collision concept	3–4 days
Recursion	Base case, call stack, recursion tracing	1 week
Linked Lists	Traversal, dummy nodes, reversal, cycle detection	4–5 days
Stacks / Queues	Stack, queue, deque, monotonic stack	4–5 days
Trees	DFS, BFS, recursive/iterative traversal	1 week
Graphs	Adjacency list/matrix, BFS/DFS, cycles, topological sort	1–1.5 weeks
Heaps	Min/max heap, top-K problems	3–4 days
Dynamic Programming	Memoization, tabulation, overlapping subproblems	1.5–2 weeks

Dependency

Arrays / Strings
HashMap / Set
Linked Lists
Stack / Queue
Trees / Graphs
Heap / Trie
       ↓
Problem-Solving Patterns
       ↓
Unseen Problems

⸻

03 — Complexity Intuition

You should learn to recognize the required complexity before designing the algorithm.

Common Complexity Order

O(1)
 ↓
O(log n)
 ↓
O(n)
 ↓
O(n log n)
 ↓
O(n²)
 ↓
O(2ⁿ)
 ↓
O(n!)

The lower the growth rate, the more scalable the algorithm.

Constraint → Complexity

Input Size	Usually Acceptable	Danger Zone
n ≤ 10–12	O(2ⁿ), O(n!)	—
n ≤ 20–25	O(2ⁿ) with pruning / bitmask DP	Naive O(n!)
n ≤ 500–1000	O(n²)	O(n³)
n ≤ 10⁵	O(n log n), O(n)	O(n²)
n ≤ 10⁶–10⁷	O(n), O(log n)	Above O(n log n)

Reflex: Look at the constraints first.

The constraints frequently reveal the target complexity before you fully understand the problem.

⸻

04 — The 15-Pattern Library

Master these patterns systematically.

1. Two Pointers

Signal:

* Sorted array
* Pair/triplet sum
* Palindrome
* Opposite-end traversal

Examples:

* Two Sum II
* 3Sum
* Container With Most Water

⸻

2. Sliding Window

Signal:

* Subarray / substring
* Maximum/minimum length
* Sum constraint
* Distinct characters
* Contiguous range

Examples:

* Longest Substring Without Repeating Characters
* Maximum Sum Subarray of Size K

⸻

3. Fast & Slow Pointers

Signal:

* Linked-list cycle
* Middle of linked list
* Two pointers moving at different speeds
* “Meet somewhere” problems

Examples:

* Linked List Cycle
* Happy Number
* Middle of the Linked List

⸻

4. Merge Intervals

Signal:

* Overlapping ranges
* Scheduling
* Interval union
* Meeting times

Examples:

* Merge Intervals
* Insert Interval
* Meeting Rooms

⸻

5. In-Place Linked List Reversal

Signal:

* Reverse an entire list
* Reverse a section
* Reverse nodes without extra space

Examples:

* Reverse Linked List
* Reverse Nodes in k-Group

⸻

6. Tree BFS

Signal:

* Level-order traversal
* Minimum number of levels
* Shortest path in an unweighted structure

Examples:

* Binary Tree Level Order Traversal
* Rotting Oranges

⸻

7. Tree DFS

Signal:

* Path problems
* Subtree properties
* Tree height/depth
* Recursive exploration

Examples:

* Path Sum
* Diameter of Binary Tree
* Validate Binary Search Tree

⸻

8. Two Heaps

Signal:

* Dynamic median
* Maintain two balanced halves
* Continuously adding/removing values

Example:

* Find Median from Data Stream

⸻

9. Subsets / Backtracking

Signal:

* Generate combinations
* Generate permutations
* Generate subsets
* Constraint satisfaction

Examples:

* Subsets
* Permutations
* N-Queens
* Word Search

Core mental model:

Choose
  ↓
Explore
  ↓
Undo choice
  ↓
Choose next option

⸻

10. Modified Binary Search

Signal:

* Sorted array
* Rotated sorted array
* Find boundary
* Find threshold
* Search for a transition point

Examples:

* Search in Rotated Sorted Array
* Find Peak Element

⸻

11. Top-K Elements

Signal:

* K largest
* K smallest
* K most frequent
* K-th largest/smallest

Examples:

* Kth Largest Element
* Top K Frequent Elements

⸻

12. K-Way Merge

Signal:

* Multiple sorted arrays/lists
* Merge K sorted structures
* Smallest/largest element across multiple sorted sources

Examples:

* Merge K Sorted Lists
* Smallest Range Covering K Lists

⸻

13. Dynamic Programming

Signal:

* Optimal value
* Number of ways
* Minimum/maximum
* Repeated subproblems
* Multiple choices at each state

Examples:

* 0/1 Knapsack
* Longest Increasing Subsequence
* Coin Change
* Edit Distance

Core progression:

Brute Force Recursion
        ↓
Memoization
        ↓
Tabulation
        ↓
Space Optimization

⸻

14. Topological Sort

Signal:

* Dependencies
* Prerequisites
* “A must happen before B”
* Ordering constraints

Examples:

* Course Schedule
* Alien Dictionary

⸻

15. Union-Find / DSU

Signal:

* Connectivity
* Grouping
* Components
* Cycle detection in undirected graphs

Examples:

* Number of Provinces
* Redundant Connection

Core optimizations:

Path Compression
+
Union by Rank / Size

⸻

05 — Deep Dive: Sliding Window

Sliding Window is a fundamental pattern because it can transform many O(n²) brute-force solutions into O(n) solutions.

Example

a  b  [c  a]  b  c  b  b
       ↑  ↑
     left right

Current window:

"ca"

If another a enters the window:

[c  a  a]
 ↑     ↑
left  right

The constraint is violated because a appears twice.

Shrink from the left:

[c  a  a]
    ↑  ↑
   left right

Continue until the window becomes valid again.

General Algorithm

1. Move right pointer
2. Add the new element
3. Check the window constraint
4. If invalid:
       move left pointer
       remove/update elements
5. Track the best valid window
6. Continue

JavaScript Example

// Longest Substring Without Repeating Characters
// Time: O(n)
// Space: O(n)
function lengthOfLongestSubstring(s) {
    let seen = new Map();
    let left = 0;
    let best = 0;
    for (let right = 0; right < s.length; right++) {
        if (
            seen.has(s[right]) &&
            seen.get(s[right]) >= left
        ) {
            left = seen.get(s[right]) + 1;
        }
        seen.set(s[right], right);
        best = Math.max(
            best,
            right - left + 1
        );
    }
    return best;
}

Why O(n)?

Both pointers only move forward.

left  → → → → →
right → → → → →

Neither pointer repeatedly scans the array from the beginning.

Therefore:

Total pointer movements ≈ 2n
                    ↓
                  O(n)

⸻

06 — 6-Phase Roadmap

Phase 01 — Foundations

Weeks 1–2

Complexity + Arrays + Strings + Hashing

* Learn Big-O
* Analyze 20 code snippets without running them
* Solve 15–20 easy array/string/hashmap problems
* Learn prefix sums
* Learn sorting basics
* Practice HashMap/HashSet
* Compare brute force vs optimized solutions

Goal:

Stop writing O(n²) when an O(n) HashMap solution exists.

⸻

Phase 02 — First Pattern Block

Weeks 3–5

Two Pointers + Sliding Window + Linked Lists

* Learn Two Pointers
* Learn Sliding Window
* Learn Fast/Slow Pointers
* Learn Linked List Reversal
* Solve 5–8 problems per pattern
* Start with Easy → Medium
* Draw pointer movement before coding
* Re-solve problems after 3 days

⸻

Phase 03 — Trees + Graphs + Backtracking

Weeks 6–8

Highest-Leverage Structural Block

* Master recursive tree traversal
* Master iterative tree traversal
* Learn Tree BFS
* Learn Tree DFS
* Learn Graph BFS
* Learn Graph DFS
* Learn adjacency lists
* Learn cycle detection
* Learn topological sorting
* Learn backtracking

Backtracking Template

choose
   ↓
explore
   ↓
un-choose
   ↓
next choice

⸻

Phase 04 — Heaps + Intervals + Binary Search + DSU

Weeks 9–11

* Learn heaps
* Recognize Top-K problems
* Learn Merge Intervals
* Learn Modified Binary Search
* Learn Binary Search on Answer
* Learn Union-Find
* Implement DSU from memory
* Practice path compression
* Practice union by rank/size

⸻

Phase 05 — Dynamic Programming

Weeks 12–15

The hardest block. Budget extra time.

Study in this order:

1D DP
 ↓
2D DP
 ↓
Knapsack
 ↓
LIS
 ↓
LCS
 ↓
Edit Distance
 ↓
Advanced DP

For every DP problem:

1. Define the state.
2. Define what the state means.
3. Write the recurrence in words.
4. Identify base cases.
5. Implement recursion.
6. Add memoization.
7. Convert to tabulation.
8. Optimize space if possible.

Never memorize a DP formula without understanding what the state represents.

⸻

Phase 06 — Mixed Review

Week 16+

No major new material.

* Random-order problems
* Timed Medium problems
* Weekly contest participation
* Review failed problems
* Review weakest two patterns
* Practice identifying patterns without hints
* Mix multiple patterns together

Target:

45 minutes
      ↓
Read
      ↓
Identify pattern
      ↓
Design
      ↓
Code
      ↓
Test

⸻

07 — Curated Problem Sets

Avoid randomly selecting problems from the entire LeetCode database.

Blind 75

A compact, high-signal problem set.

Best for: Fast broad coverage.

NeetCode 150

An expanded collection organized by patterns.

Best default choice: Beginners who want structured learning.

LeetCode Study Plans

Official structured tracks for topic-specific practice.

Examples include:

* Top Interview 150
* Dynamic Programming
* Data Structures
* Algorithms

⸻

Recommended Difficulty Ratio

Difficulty	Ratio	Purpose
Easy	50%	Build pattern recognition
Medium	40%	Develop real problem-solving ability
Hard	10%	Stress-test pattern combinations

Do not rush toward Hard problems.

Easy
 ↓
Pattern recognition
 ↓
Medium
 ↓
Pattern mastery
 ↓
Hard
 ↓
Pattern combination

⸻

08 — The Per-Problem Loop

Use the following process for every problem.

┌─────────────────────┐
│ 1. READ              │
│    Constraints first │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 2. EXAMPLES          │
│    Trace by hand     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 3. PATTERN?          │
│    Identify signal   │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 4. PSEUDOCODE        │
│    Before coding     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 5. CODE + TEST       │
│    Check edge cases  │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 6. LOG + REVISIT     │
│    D+3 and D+14      │
└─────────────────────┘

Step 1 — Read

Check:

* Input size
* Data type
* Constraints
* Required output
* Sorted/unsorted
* Duplicates
* Negative values
* Special conditions

Step 2 — Examples

Trace the example manually.

Step 3 — Identify Pattern

Ask:

Is it a...
├── Two Pointer problem?
├── Sliding Window?
├── Hashing?
├── Binary Search?
├── BFS / DFS?
├── Heap?
├── Backtracking?
├── DP?
└── Graph / DSU?

Step 4 — Pseudocode

Do not immediately start typing code.

Step 5 — Code + Test

Test:

* Normal case
* Empty input
* Single element
* Duplicate values
* Minimum constraints
* Maximum constraints
* Negative values where applicable

Step 6 — Log + Revisit

Re-solve from scratch.

⸻

The 25–30 Minute Rule

If you have been genuinely stuck for around 25–30 minutes on a first attempt:

Don't immediately read the solution.
          ↓
Look for a pattern hint.
          ↓
Try again.
          ↓
If still stuck → study the solution.
          ↓
Close it.
          ↓
Re-code from memory.

The goal is productive struggle, not frustration.

⸻

09 — Tracking System

Use spaced repetition for code.

problem-log.md

| Date       | Problem                       | Pattern        | 1st Try? | D+3 | D+14 |
|------------|-------------------------------|----------------|----------|-----|------|
| 2026-08-23 | Longest Substring...          | Sliding Window | No       | [ ] | [ ]  |
| 2026-08-23 | 3Sum                          | Two Pointers   | Yes      | [ ] | [ ]  |

Repository Structure

leetcode-mastery/
│
├── README.md
│
├── patterns/
│   ├── two-pointers/
│   │   └── README.md
│   │
│   ├── sliding-window/
│   │   └── README.md
│   │
│   ├── fast-slow-pointers/
│   │   └── README.md
│   │
│   ├── merge-intervals/
│   │   └── README.md
│   │
│   ├── linked-list-reversal/
│   │   └── README.md
│   │
│   ├── tree-bfs/
│   │   └── README.md
│   │
│   ├── tree-dfs/
│   │   └── README.md
│   │
│   ├── two-heaps/
│   │   └── README.md
│   │
│   ├── backtracking/
│   │   └── README.md
│   │
│   ├── binary-search/
│   │   └── README.md
│   │
│   ├── top-k/
│   │   └── README.md
│   │
│   ├── k-way-merge/
│   │   └── README.md
│   │
│   ├── dynamic-programming/
│   │   └── README.md
│   │
│   ├── topological-sort/
│   │   └── README.md
│   │
│   └── union-find/
│       └── README.md
│
└── problem-log.md

Each pattern README should contain:

1. What is the pattern?
2. When should I recognize it?
3. Key signals
4. Core template
5. Why does it work?
6. Complexity
7. Common mistakes
8. 5–8 representative problems
9. Personal notes

Failed-Twice Rule

Maintain a separate list:

FAILED TWICE
─────────────
Problem
Pattern
Mistake
Correct idea
Next review

If you fail the same pattern repeatedly, review the pattern instead of simply solving more problems.

⸻

10 — Failure Modes

❌ Solving by Difficulty

Bad:

Easy → Easy → Easy → Medium → Medium → Hard

Better:

Sliding Window
├── Easy
├── Easy
├── Medium
├── Medium
└── Medium

Pattern first. Difficulty second.

⸻

❌ Reading Solutions Too Early

If you immediately read the solution, you may recognize the answer without learning how to derive it.

Give yourself time to think.

⸻

❌ Never Re-solving

Recognition ≠ mastery.

If you remember seeing a solution but cannot reproduce it independently, you haven’t fully internalized it.

⸻

❌ Ignoring Constraints

A problem with:

n ≤ 10

and a problem with:

n ≤ 100,000

should immediately trigger very different algorithmic thinking.

⸻

❌ Skipping Dynamic Programming

DP is difficult, but skipping it creates a major gap.

Learn it gradually:

Recursion
   ↓
Memoization
   ↓
Tabulation
   ↓
Optimization

⸻

Final Mastery Checklist

Foundations

* Big-O
* Arrays
* Strings
* Hashing
* Recursion
* Linked Lists
* Stacks
* Queues
* Trees
* Graphs
* Heaps
* Basic DP

Patterns

* Two Pointers
* Sliding Window
* Fast/Slow Pointers
* Merge Intervals
* Linked List Reversal
* Tree BFS
* Tree DFS
* Two Heaps
* Backtracking
* Binary Search
* Top-K
* K-Way Merge
* Dynamic Programming
* Topological Sort
* Union-Find

Problem-Solving

* Read constraints first
* Trace examples manually
* Identify the pattern
* Write pseudocode
* Code
* Test edge cases
* Analyze complexity
* Record mistakes
* Re-solve after 3 days
* Re-solve after 14 days

⸻

The Ultimate Rule

DO NOT ASK:
"How many LeetCode problems have I solved?"
ASK:
"How many patterns can I recognize
and apply to a problem I've never seen?"

The objective is not to become good at memorizing LeetCode solutions.

The objective is to become good at thinking algorithmically.

PROBLEM
   ↓
CONSTRAINTS
   ↓
OBSERVATION
   ↓
PATTERN
   ↓
ALGORITHM
   ↓
IMPLEMENTATION
   ↓
COMPLEXITY
   ↓
REVIEW
   ↓
PATTERN MASTERY

End goal: Solve unfamiliar problems, not just familiar ones.LeetCode Mastery Protocol

A structured, zero-to-competent system for learning Data Structures, Algorithms, and problem-solving patterns — built for depth, not random grinding.

15 Core Patterns · 6 Phases · ~16 Weeks · Patterns > Problem Count

⸻

01 — The Mental Model

Why Most People Fail

The default approach:

Open LeetCode
   ↓
Solve #1
   ↓
Solve #2
   ↓
Solve #3
   ↓
Repeat...

This often teaches you individual solutions, not reusable problem-solving patterns.

You may solve 300 random problems but still get stuck when a new problem uses a familiar idea in an unfamiliar way.

The Pattern Model

Instead:

Learn a pattern
      ↓
Understand WHY it works
      ↓
Solve 5–8 representative problems
      ↓
Re-solve them later
      ↓
Recognize the pattern in unseen problems

The goal is compression rather than memorization.

Core principle: Patterns > Problem Count

⸻

02 — Foundation Map

Before pattern-based LeetCode practice, build these foundations.

Foundation	Must Know	Suggested Time
Complexity / Big-O	Time, space, best/average/worst case, amortized cost	2–3 days
Arrays & Strings	In-place operations, prefix sums, sorting, two pointers	1 week
Hashing	HashMap/Set, lookup complexity, collision concept	3–4 days
Recursion	Base case, call stack, recursion tracing	1 week
Linked Lists	Traversal, dummy nodes, reversal, cycle detection	4–5 days
Stacks / Queues	Stack, queue, deque, monotonic stack	4–5 days
Trees	DFS, BFS, recursive/iterative traversal	1 week
Graphs	Adjacency list/matrix, BFS/DFS, cycles, topological sort	1–1.5 weeks
Heaps	Min/max heap, top-K problems	3–4 days
Dynamic Programming	Memoization, tabulation, overlapping subproblems	1.5–2 weeks

Dependency

Arrays / Strings
HashMap / Set
Linked Lists
Stack / Queue
Trees / Graphs
Heap / Trie
       ↓
Problem-Solving Patterns
       ↓
Unseen Problems

⸻

03 — Complexity Intuition

You should learn to recognize the required complexity before designing the algorithm.

Common Complexity Order

O(1)
 ↓
O(log n)
 ↓
O(n)
 ↓
O(n log n)
 ↓
O(n²)
 ↓
O(2ⁿ)
 ↓
O(n!)

The lower the growth rate, the more scalable the algorithm.

Constraint → Complexity

Input Size	Usually Acceptable	Danger Zone
n ≤ 10–12	O(2ⁿ), O(n!)	—
n ≤ 20–25	O(2ⁿ) with pruning / bitmask DP	Naive O(n!)
n ≤ 500–1000	O(n²)	O(n³)
n ≤ 10⁵	O(n log n), O(n)	O(n²)
n ≤ 10⁶–10⁷	O(n), O(log n)	Above O(n log n)

Reflex: Look at the constraints first.

The constraints frequently reveal the target complexity before you fully understand the problem.

⸻

04 — The 15-Pattern Library

Master these patterns systematically.

1. Two Pointers

Signal:

* Sorted array
* Pair/triplet sum
* Palindrome
* Opposite-end traversal

Examples:

* Two Sum II
* 3Sum
* Container With Most Water

⸻

2. Sliding Window

Signal:

* Subarray / substring
* Maximum/minimum length
* Sum constraint
* Distinct characters
* Contiguous range

Examples:

* Longest Substring Without Repeating Characters
* Maximum Sum Subarray of Size K

⸻

3. Fast & Slow Pointers

Signal:

* Linked-list cycle
* Middle of linked list
* Two pointers moving at different speeds
* “Meet somewhere” problems

Examples:

* Linked List Cycle
* Happy Number
* Middle of the Linked List

⸻

4. Merge Intervals

Signal:

* Overlapping ranges
* Scheduling
* Interval union
* Meeting times

Examples:

* Merge Intervals
* Insert Interval
* Meeting Rooms

⸻

5. In-Place Linked List Reversal

Signal:

* Reverse an entire list
* Reverse a section
* Reverse nodes without extra space

Examples:

* Reverse Linked List
* Reverse Nodes in k-Group

⸻

6. Tree BFS

Signal:

* Level-order traversal
* Minimum number of levels
* Shortest path in an unweighted structure

Examples:

* Binary Tree Level Order Traversal
* Rotting Oranges

⸻

7. Tree DFS

Signal:

* Path problems
* Subtree properties
* Tree height/depth
* Recursive exploration

Examples:

* Path Sum
* Diameter of Binary Tree
* Validate Binary Search Tree

⸻

8. Two Heaps

Signal:

* Dynamic median
* Maintain two balanced halves
* Continuously adding/removing values

Example:

* Find Median from Data Stream

⸻

9. Subsets / Backtracking

Signal:

* Generate combinations
* Generate permutations
* Generate subsets
* Constraint satisfaction

Examples:

* Subsets
* Permutations
* N-Queens
* Word Search

Core mental model:

Choose
  ↓
Explore
  ↓
Undo choice
  ↓
Choose next option

⸻

10. Modified Binary Search

Signal:

* Sorted array
* Rotated sorted array
* Find boundary
* Find threshold
* Search for a transition point

Examples:

* Search in Rotated Sorted Array
* Find Peak Element

⸻

11. Top-K Elements

Signal:

* K largest
* K smallest
* K most frequent
* K-th largest/smallest

Examples:

* Kth Largest Element
* Top K Frequent Elements

⸻

12. K-Way Merge

Signal:

* Multiple sorted arrays/lists
* Merge K sorted structures
* Smallest/largest element across multiple sorted sources

Examples:

* Merge K Sorted Lists
* Smallest Range Covering K Lists

⸻

13. Dynamic Programming

Signal:

* Optimal value
* Number of ways
* Minimum/maximum
* Repeated subproblems
* Multiple choices at each state

Examples:

* 0/1 Knapsack
* Longest Increasing Subsequence
* Coin Change
* Edit Distance

Core progression:

Brute Force Recursion
        ↓
Memoization
        ↓
Tabulation
        ↓
Space Optimization

⸻

14. Topological Sort

Signal:

* Dependencies
* Prerequisites
* “A must happen before B”
* Ordering constraints

Examples:

* Course Schedule
* Alien Dictionary

⸻

15. Union-Find / DSU

Signal:

* Connectivity
* Grouping
* Components
* Cycle detection in undirected graphs

Examples:

* Number of Provinces
* Redundant Connection

Core optimizations:

Path Compression
+
Union by Rank / Size

⸻

05 — Deep Dive: Sliding Window

Sliding Window is a fundamental pattern because it can transform many O(n²) brute-force solutions into O(n) solutions.

Example

a  b  [c  a]  b  c  b  b
       ↑  ↑
     left right

Current window:

"ca"

If another a enters the window:

[c  a  a]
 ↑     ↑
left  right

The constraint is violated because a appears twice.

Shrink from the left:

[c  a  a]
    ↑  ↑
   left right

Continue until the window becomes valid again.

General Algorithm

1. Move right pointer
2. Add the new element
3. Check the window constraint
4. If invalid:
       move left pointer
       remove/update elements
5. Track the best valid window
6. Continue

JavaScript Example

// Longest Substring Without Repeating Characters
// Time: O(n)
// Space: O(n)
function lengthOfLongestSubstring(s) {
    let seen = new Map();
    let left = 0;
    let best = 0;
    for (let right = 0; right < s.length; right++) {
        if (
            seen.has(s[right]) &&
            seen.get(s[right]) >= left
        ) {
            left = seen.get(s[right]) + 1;
        }
        seen.set(s[right], right);
        best = Math.max(
            best,
            right - left + 1
        );
    }
    return best;
}

Why O(n)?

Both pointers only move forward.

left  → → → → →
right → → → → →

Neither pointer repeatedly scans the array from the beginning.

Therefore:

Total pointer movements ≈ 2n
                    ↓
                  O(n)

⸻

06 — 6-Phase Roadmap

Phase 01 — Foundations

Weeks 1–2

Complexity + Arrays + Strings + Hashing

* Learn Big-O
* Analyze 20 code snippets without running them
* Solve 15–20 easy array/string/hashmap problems
* Learn prefix sums
* Learn sorting basics
* Practice HashMap/HashSet
* Compare brute force vs optimized solutions

Goal:

Stop writing O(n²) when an O(n) HashMap solution exists.

⸻

Phase 02 — First Pattern Block

Weeks 3–5

Two Pointers + Sliding Window + Linked Lists

* Learn Two Pointers
* Learn Sliding Window
* Learn Fast/Slow Pointers
* Learn Linked List Reversal
* Solve 5–8 problems per pattern
* Start with Easy → Medium
* Draw pointer movement before coding
* Re-solve problems after 3 days

⸻

Phase 03 — Trees + Graphs + Backtracking

Weeks 6–8

Highest-Leverage Structural Block

* Master recursive tree traversal
* Master iterative tree traversal
* Learn Tree BFS
* Learn Tree DFS
* Learn Graph BFS
* Learn Graph DFS
* Learn adjacency lists
* Learn cycle detection
* Learn topological sorting
* Learn backtracking

Backtracking Template

choose
   ↓
explore
   ↓
un-choose
   ↓
next choice

⸻

Phase 04 — Heaps + Intervals + Binary Search + DSU

Weeks 9–11

* Learn heaps
* Recognize Top-K problems
* Learn Merge Intervals
* Learn Modified Binary Search
* Learn Binary Search on Answer
* Learn Union-Find
* Implement DSU from memory
* Practice path compression
* Practice union by rank/size

⸻

Phase 05 — Dynamic Programming

Weeks 12–15

The hardest block. Budget extra time.

Study in this order:

1D DP
 ↓
2D DP
 ↓
Knapsack
 ↓
LIS
 ↓
LCS
 ↓
Edit Distance
 ↓
Advanced DP

For every DP problem:

1. Define the state.
2. Define what the state means.
3. Write the recurrence in words.
4. Identify base cases.
5. Implement recursion.
6. Add memoization.
7. Convert to tabulation.
8. Optimize space if possible.

Never memorize a DP formula without understanding what the state represents.

⸻

Phase 06 — Mixed Review

Week 16+

No major new material.

* Random-order problems
* Timed Medium problems
* Weekly contest participation
* Review failed problems
* Review weakest two patterns
* Practice identifying patterns without hints
* Mix multiple patterns together

Target:

45 minutes
      ↓
Read
      ↓
Identify pattern
      ↓
Design
      ↓
Code
      ↓
Test

⸻

07 — Curated Problem Sets

Avoid randomly selecting problems from the entire LeetCode database.

Blind 75

A compact, high-signal problem set.

Best for: Fast broad coverage.

NeetCode 150

An expanded collection organized by patterns.

Best default choice: Beginners who want structured learning.

LeetCode Study Plans

Official structured tracks for topic-specific practice.

Examples include:

* Top Interview 150
* Dynamic Programming
* Data Structures
* Algorithms

⸻

Recommended Difficulty Ratio

Difficulty	Ratio	Purpose
Easy	50%	Build pattern recognition
Medium	40%	Develop real problem-solving ability
Hard	10%	Stress-test pattern combinations

Do not rush toward Hard problems.

Easy
 ↓
Pattern recognition
 ↓
Medium
 ↓
Pattern mastery
 ↓
Hard
 ↓
Pattern combination

⸻

08 — The Per-Problem Loop

Use the following process for every problem.

┌─────────────────────┐
│ 1. READ              │
│    Constraints first │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 2. EXAMPLES          │
│    Trace by hand     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 3. PATTERN?          │
│    Identify signal   │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 4. PSEUDOCODE        │
│    Before coding     │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 5. CODE + TEST       │
│    Check edge cases  │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│ 6. LOG + REVISIT     │
│    D+3 and D+14      │
└─────────────────────┘

Step 1 — Read

Check:

* Input size
* Data type
* Constraints
* Required output
* Sorted/unsorted
* Duplicates
* Negative values
* Special conditions

Step 2 — Examples

Trace the example manually.

Step 3 — Identify Pattern

Ask:

Is it a...
├── Two Pointer problem?
├── Sliding Window?
├── Hashing?
├── Binary Search?
├── BFS / DFS?
├── Heap?
├── Backtracking?
├── DP?
└── Graph / DSU?

Step 4 — Pseudocode

Do not immediately start typing code.

Step 5 — Code + Test

Test:

* Normal case
* Empty input
* Single element
* Duplicate values
* Minimum constraints
* Maximum constraints
* Negative values where applicable

Step 6 — Log + Revisit

Re-solve from scratch.

⸻

The 25–30 Minute Rule

If you have been genuinely stuck for around 25–30 minutes on a first attempt:

Don't immediately read the solution.
          ↓
Look for a pattern hint.
          ↓
Try again.
          ↓
If still stuck → study the solution.
          ↓
Close it.
          ↓
Re-code from memory.

The goal is productive struggle, not frustration.

⸻

09 — Tracking System

Use spaced repetition for code.

problem-log.md

| Date       | Problem                       | Pattern        | 1st Try? | D+3 | D+14 |
|------------|-------------------------------|----------------|----------|-----|------|
| 2026-08-23 | Longest Substring...          | Sliding Window | No       | [ ] | [ ]  |
| 2026-08-23 | 3Sum                          | Two Pointers   | Yes      | [ ] | [ ]  |

Repository Structure

leetcode-mastery/
│
├── README.md
│
├── patterns/
│   ├── two-pointers/
│   │   └── README.md
│   │
│   ├── sliding-window/
│   │   └── README.md
│   │
│   ├── fast-slow-pointers/
│   │   └── README.md
│   │
│   ├── merge-intervals/
│   │   └── README.md
│   │
│   ├── linked-list-reversal/
│   │   └── README.md
│   │
│   ├── tree-bfs/
│   │   └── README.md
│   │
│   ├── tree-dfs/
│   │   └── README.md
│   │
│   ├── two-heaps/
│   │   └── README.md
│   │
│   ├── backtracking/
│   │   └── README.md
│   │
│   ├── binary-search/
│   │   └── README.md
│   │
│   ├── top-k/
│   │   └── README.md
│   │
│   ├── k-way-merge/
│   │   └── README.md
│   │
│   ├── dynamic-programming/
│   │   └── README.md
│   │
│   ├── topological-sort/
│   │   └── README.md
│   │
│   └── union-find/
│       └── README.md
│
└── problem-log.md

Each pattern README should contain:

1. What is the pattern?
2. When should I recognize it?
3. Key signals
4. Core template
5. Why does it work?
6. Complexity
7. Common mistakes
8. 5–8 representative problems
9. Personal notes

Failed-Twice Rule

Maintain a separate list:

FAILED TWICE
─────────────
Problem
Pattern
Mistake
Correct idea
Next review

If you fail the same pattern repeatedly, review the pattern instead of simply solving more problems.

⸻

10 — Failure Modes

❌ Solving by Difficulty

Bad:

Easy → Easy → Easy → Medium → Medium → Hard

Better:

Sliding Window
├── Easy
├── Easy
├── Medium
├── Medium
└── Medium

Pattern first. Difficulty second.

⸻

❌ Reading Solutions Too Early

If you immediately read the solution, you may recognize the answer without learning how to derive it.

Give yourself time to think.

⸻

❌ Never Re-solving

Recognition ≠ mastery.

If you remember seeing a solution but cannot reproduce it independently, you haven’t fully internalized it.

⸻

❌ Ignoring Constraints

A problem with:

n ≤ 10

and a problem with:

n ≤ 100,000

should immediately trigger very different algorithmic thinking.

⸻

❌ Skipping Dynamic Programming

DP is difficult, but skipping it creates a major gap.

Learn it gradually:

Recursion
   ↓
Memoization
   ↓
Tabulation
   ↓
Optimization

⸻

Final Mastery Checklist

Foundations

* Big-O
* Arrays
* Strings
* Hashing
* Recursion
* Linked Lists
* Stacks
* Queues
* Trees
* Graphs
* Heaps
* Basic DP

Patterns

* Two Pointers
* Sliding Window
* Fast/Slow Pointers
* Merge Intervals
* Linked List Reversal
* Tree BFS
* Tree DFS
* Two Heaps
* Backtracking
* Binary Search
* Top-K
* K-Way Merge
* Dynamic Programming
* Topological Sort
* Union-Find

Problem-Solving

* Read constraints first
* Trace examples manually
* Identify the pattern
* Write pseudocode
* Code
* Test edge cases
* Analyze complexity
* Record mistakes
* Re-solve after 3 days
* Re-solve after 14 days

⸻

The Ultimate Rule

DO NOT ASK:
"How many LeetCode problems have I solved?"
ASK:
"How many patterns can I recognize
and apply to a problem I've never seen?"

The objective is not to become good at memorizing LeetCode solutions.

The objective is to become good at thinking algorithmically.

PROBLEM
   ↓
CONSTRAINTS
   ↓
OBSERVATION
   ↓
PATTERN
   ↓
ALGORITHM
   ↓
IMPLEMENTATION
   ↓
COMPLEXITY
   ↓
REVIEW
   ↓
PATTERN MASTERY

End goal: Solve unfamiliar problems, not just familiar ones.
