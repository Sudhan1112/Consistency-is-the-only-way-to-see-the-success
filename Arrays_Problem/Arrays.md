# Arrays (DSA Notes)

Arrays are the foundation for many DSA problems. Different **patterns** help solve different types of problems efficiently.  
This mindmap organizes problems by **pattern → problem type → example**.  

---

## 🔹 Linear Scan (Baseline)

> Pattern Idea: Just scan the array once (or twice), keep track of the needed values.  
> Best for **extreme value problems (max, min, ranking, shifting/placement).**  
> Time: O(n), Space: O(1).

- **Find Maximum Element**  
  - Problem: Find Maximum in Array  
  - Example: `arr = [5, 10, 2, 8] → max = 10`

- **Find Minimum Element**  
  - Problem: Find Minimum in Array  
  - Example: `arr = [5, 10, 2, 8] → min = 2`

- **Find Second Largest Element**  
  - Problem: Second Largest in Array  
  - Optimized: Track two variables (`largest`, `secondLargest`) in one pass.  
  - Example: `arr = [10, 20, 5, 8] → second largest = 10`

- **Move Zeros to End (continuous scan + overwrite)**  
  - Problem: Move All Zeros to End of Array  
  - Idea: Scan array, shift non-zero elements forward, fill remaining with zeros.  
  - Example: `arr = [0,1,0,3,12] → [1,3,12,0,0]`  

Takeaway: Linear scan baseline is the cleanest choice for simple ranking, shifting, and placement problems.  

---

## 🔹 Two Pointers

> Pattern Idea: Use two indices moving towards each other (or in the same direction) to reduce nested loops.  
> Best for **reversals, partitioning, pair-search, and sorted array operations.**

- **Reverse an Array**  
  - Problem: Reverse Array  
  - Idea: Place one pointer at the start and one at the end, swap while moving inward.  
  - Example: `arr = [1,2,3,4,5] → [5,4,3,2,1]`  

- **Move Zeros to End (partitioning style)**  
  - Problem: Move All Zeros to End of Array  
  - `i` scans entire array, `j` tracks next position for non-zero.  
  - When `arr[i] != 0`, place at `arr[j]` and increment `j`.  
  - After loop, fill rest with zeros.  
  - Example: `arr = [0,1,0,3,12] → [1,3,12,0,0]`  

- **Pair with Target Sum**  
- **Remove Duplicates from Sorted Array**  
- **Container With Most Water**  

---

## 🔹 Sliding Window

> Pattern Idea: A "window" slides over the array while maintaining some running info (sum, frequency, etc.).  
> Best for **subarray problems (fixed/variable size, longest/shortest with constraints).**

- **Maximum Sum Subarray of Size k**  
- **Longest Subarray with Sum ≤ K**  
- **Minimum Window Substring (string variant)**  

---

## 🔹 Heap / Priority Queue

> Pattern Idea: Use a heap (binary tree stored as an array) to efficiently track **top-k elements** or **k-th statistics**.  
> Best for **order statistics, frequency counts, and streaming problems.**

- **Find Second Largest (special case of K-th Largest)**  
  - Problem: Find Second Largest in Array  
  - Example: `arr = [5, 10, 20, 10] → second largest = 10`  

- **Future Problems (to add later):**  
  - Find K-th largest element  
  - Top-K frequent elements  
  - Running median of a stream  

---

## 🔹 Binary Search

> Pattern Idea: Divide and conquer by halving search space. Works on **sorted arrays** or **monotonic conditions**.  
> Best for **search problems and optimization (binary search on answer).**

- **Search Element in Sorted Array**  
- **Search in Rotated Sorted Array**  
- **Find Minimum in Rotated Sorted Array**  
- **Allocate Minimum Pages (binary search on answer)**  
