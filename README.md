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
| 12 | 2025-08-14 | GFG      | [Kadane’s Algorithm](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/kadanes-algorithm-1587115620) | Java | Mastered finding max subarray sum using current and global sum tracking. | `cur_s = max(arr[i], cur_s + arr[i])` | O(n) | O(1) | One scan, constant extra variables. |
| 13 | 2025-08-15 | GFG      | [Maximum Product Subarray](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/maximum-product-subarray3604) | Java | Learned to track both max and min products due to negatives. | DP with `max_p`, `min_p` | O(n) | O(1) | Trick: temp variable avoids overwrite errors. |
| 14 | 2025-08-20 | GFG      | [String to Integer (atoi)](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/string-gfg-160/problem/implement-atoi) | Java | Handled string to integer conversion with spaces, sign, and overflow. | `result = result * 10 + digit; check overflow` | O(n) | O(1) | Careful handling of max/min int overflow. |
| 15 | 2025-08-20 | GFG      | [Non-Repeating Character](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/string-gfg-160/problem/non-repeating-character-1587115620) | Java | Learned brute-force way to find first non-repeating char. | Nested loops to check uniqueness | O(n²) | O(1) | Returned `$` if no unique char exists. |
| 16 | 2025-08-20 | LeetCode | [String to Integer (atoi)](https://leetcode.com/problems/string-to-integer-atoi/description/) | Java | Reinforced handling of atoi with extra boolean for overflow check. | `willOverFlow = result > (MAX - digit)/10` | O(n) | O(1) | Similar to GFG, slightly optimized readability. |
| 17 | 2025-08-20 | LeetCode | [First Unique Character in a String](https://leetcode.com/problems/first-unique-character-in-a-string/) | Java | Optimized frequency array approach for unique char index. | `freq[s.charAt(i) - 'a']++` | O(n) | O(26) ≈ O(1) | Two-pass: count frequency, then find first unique. |
| 18 | 2025-08-16 | GFG      | [Maximum Circular Subarray Sum](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/max-circular-subarray-sum-1587115620) | Java | Learned to handle circular subarray max using total sum minus min subarray sum. | `max(max_s, tot - min_s)` | O(n) | O(1) | Handles all-negative arrays by checking `max_s < 0`. |
| 19 | 2025-08-16 | GFG      | [Smallest Positive Missing Number](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/smallest-positive-missing-number-1587115621) | Java | Used HashSet to track positives and find the first missing. | `while(!s.contains(i)) i++` | O(n) | O(n) | Efficient for unsorted arrays, handles positives only. |


I was doing my work. but no one is there to help me