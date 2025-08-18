# 🚀 Mission: Beginner to Master DSA in 3 Months 🔥

## 🎯 Goal
Solve **180 to 240 DSA problems** over the next **3 months**, focusing on **depth, consistency, and mastery** — not just numbers.

## 📌 Destination
**Start Date:** 2025-08-07  
**End Date:** 2025-11-07  
**Active Days:** Monday to Friday (Weekends = Recall + Review Sessions)  
**Daily Target:** Solve **3 to 4 quality problems per day**

## 🧠 Why This Matters
> _"Consistency creates clarity.  
Clarity builds confidence.  
Confidence lands offers."_

Let’s go — one problem at a time. One concept at a time. One step closer to becoming unstoppable.

### 🔁 Reusable Daily Entry Template


You can copy and paste this below the tracker to add a new entry quickly:

| S.No | Date       | Platform(s)  | [Problem Title](Problem Link)                                        | Language(s) Used | What I Learned Today                                                                     | Code Snippet / Notes                          | TC   | SC   | Why TC & SC                                            |
|-------|------------|--------------|----------------------------------------------------------------------|------------------|-----------------------------------------------------------------------------------------|-----------------------------------------------|-------|-------|--------------------------------------------------------|
| 1     | YYYY-MM-DD | PlatformName | [Example Problem](https://example.com)                              | C++, Java, Python | Brief 1–2 line takeaway about the new concept or insight learned                         | Key code snippet, pattern, or notable trick  | O(?)  | O(?)  | Explanation of time complexity (TC) and space complexity (SC) |


## 📈 Daily Progress Tracker

| S.No | Date       | Platform | Problem Name / Link | Language(s) Used | What I Learned Today | Code Snippet / Notes | TC | SC | Why TC & SC |
|------|------------|----------|---------------------|------------------|----------------------|----------------------|----|----|-------------|
| 1    | 2025-08-07 | GFG      | [Second Largest](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/second-largest3735) | Java | Learned array traversal to find largest & second largest without sorting. | Track `largest` and `secondLargest` in one pass. | O(n) | O(1) | Single scan of array; no extra space. |
| 2    | 2025-08-07 | GFG      | [Move All Zeroes to End](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/move-all-zeroes-to-end-of-array0751) | Java | Two-pointer approach to push non-zero elements first. | Maintain index `j` for next non-zero placement. | O(n) | O(1) | Linear scan; swaps in place. |
| 3    | 2025-08-07 | GFG      | [Reverse Array](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/reverse-an-array) | Java | Two-pointer swap from ends towards center. | Swap `arr[i]` and `arr[j]` until i<j. | O(n) | O(1) | Each element swapped once. |
| 4    | 2025-08-09 | GFG      | [Rotate Array](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/rotate-array-by-n-elements-1587115621) | Java | Mastered 3-step reversal method for rotation. | Reverse parts then whole array. | O(n) | O(1) | All elements reversed exactly once. |
| 5    | 2025-08-09 | GFG      | [Next Permutation](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/next-permutation5226) | Java | Learned lexicographical ordering & pivot swap. | Find pivot, swap, reverse suffix. | O(n) | O(1) | Scan + reverse. |
| 6    | 2025-08-10 | LeetCode | [Second Largest Digit in a String](https://leetcode.com/problems/second-largest-digit-in-a-string/) | Java | Traversing string & tracking digits dynamically. | Keep track of largest & second largest digit. | O(n) | O(1) | Scan once, store two values. |
| 7    | 2025-08-10 | LeetCode | [Move Zeroes](https://leetcode.com/problems/move-zeroes/) | Java | Same as "Move All Zeroes to End" — reinforced two-pointer pattern. | Maintain write pointer `j`. | O(n) | O(1) | Linear pass; in-place. |
| 8    | 2025-08-11 | GFG      | [Majority Element (More than ⌊n/3⌋ times)](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/majority-vote) | Java | Learned Boyer–Moore Majority Vote algorithm for n/3 variation; also implemented sort-based counting. | At most 2 elements can exceed ⌊n/3⌋; use two-pass vote + verify. | O(n) optimal, O(n log n) sort-based | O(1) optimal, O(1) sort-based | Boyer–Moore is constant space and avoids sorting overhead. |
| 9    | 2025-08-13 | GFG      | [Stock Buy and Sell – Multiple Transactions Allowed](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/stock-buy-and-sell2615) | Java | Learned to sum all upward price differences for multiple transactions. | Add (prices[i] - prices[i-1]) if positive. | O(n) | O(1) | One pass over prices; no extra memory. |
| 10   | 2025-08-13 | GFG      | [Stock Buy and Sell – Max One Transaction Allowed](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/buy-stock-2) | Java | Learned to track min price so far and compute max profit in one pass. | Maintain `min_p` and update max profit. | O(n) | O(1) | Single scan, no extra storage. |
| 11 | 2025-08-14 | GFG      | [Minimize the Heights II](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/minimize-the-heights3351)      | Java | Learned greedy + sorting to minimize height difference after modification. | Sort array; try adjusting smallest and largest. | O(n log n) | O(1)  | Sorting dominates time; no extra structures.  |
| 12 | 2025-08-14 | GFG      | [Kadane’s Algorithm](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/kadanes-algorithm-1587115620)       | Java | Mastered finding max subarray sum using current and global sum tracking.   | `cur_s = max(arr[i], cur_s + arr[i])`.          | O(n)       | O(1)  | One scan, constant extra variables.           |
| 13 | 2025-08-15 | GFG      | [Maximum Product Subarray](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/maximum-product-subarray3604) | Java | Learned to track both max and min products due to negatives.               | DP with `max_p`, `min_p`.                       | O(n)       | O(1)  | Trick: temp variable avoids overwrite errors. |

still in process