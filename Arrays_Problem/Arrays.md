# Arrays (DSA Notes)

Arrays are the foundation for many DSA problems. Different **patterns** help solve different types of problems efficiently.  
This mindmap organizes problems by **pattern → problem type → example**.  

---

## 🔹 Linear Scan (Baseline)

> Pattern Idea: Just scan the array once (or twice), keep track of the needed values.  
> Best for **extreme value problems** (max, min, second largest, etc.).  
> Time: O(n), Space: O(1).

- **Find Maximum Element**
  - Brute Force: Scan the array and track max. O(n).
  - Optimized: Same as brute force (already optimal).
  - Example: `arr = [5, 10, 2, 8] → max = 10`

- **Find Minimum Element**
  - Brute Force: Scan the array and track min. O(n).
  - Optimized: Same as brute force.
  - Example: `arr = [5, 10, 2, 8] → min = 2`

- **Find Second Largest Element**
  - Brute Force:
    - Step 1: Scan once to find `largest`.
    - Step 2: Scan again ignoring largest, find max among remaining.  
    - Time: O(2n) ≈ O(n).
  - Optimized:
    - Track two variables in one pass: `largest` and `secondLargest`.
    - Update them as you scan.
    - Time: O(n), Space: O(1).
  - Example: `arr = [10, 20, 5, 8] → second largest = 10`
  - Takeaway: Linear scan baseline is the cleanest choice for simple ranking problems.

---

## 🔹 Two Pointers

> Pattern Idea: Use two indices moving towards each other (or in the same direction) to reduce nested loops.  
> Best for **sorted arrays, subarray sums, or pairing problems**.

- **Examples (to add later)**:
  - Pair with target sum
  - Remove duplicates from sorted array
  - Container with most water

---

## 🔹 Sliding Window

> Pattern Idea: A "window" slides over the array while maintaining some running info (sum, frequency, etc.).  
> Best for **subarray and substring problems**.

- **Examples (to add later)**:
  - Maximum sum subarray of size k
  - Longest subarray with sum ≤ K
  - Minimum window substring (string variant)

---

## 🔹 Heap / Priority Queue

> Pattern Idea: Use a heap (binary tree stored as an array) to efficiently track **top-k elements** or **k-th statistics**.  
> Best for **order statistics, frequency counts, and streaming problems**.

- **Find Second Largest (special case of K-th Largest)**
  - Brute Force:
    - Sort array → take second last element.
    - Time: O(n log n).
  - Optimized (Heap):
    - Maintain a **min-heap of size 2** while scanning.
    - Root = second largest.
    - Time: O(n log 2) ≈ O(n), Space: O(2).
  - Example: `arr = [5, 10, 20, 10] → second largest = 10`
  - Takeaway:  
    - For small fixed k (like 2), linear scan is faster.  
    - For general k or streaming data, heap is the go-to.

- **Future Problems (to add later)**:
  - Find K-th largest element
  - Top-K frequent elements
  - Running median of a stream

---

## 🔹 Binary Search

> Pattern Idea: Divide and conquer by halving search space. Works on **sorted arrays** or **monotonic conditions**.  
> Best for **searching problems and optimization (binary search on answer)**.

- **Examples (to add later)**:
  - Search element in sorted array
  - Search in rotated sorted array
  - Find minimum in rotated sorted array
  - Allocate minimum pages (binary search on answer)

---
