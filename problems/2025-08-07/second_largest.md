# Second Largest — GFG

## 📜 Problem Statement
Given an array of integers, find the second largest element without using built-in sort.

---

## 🧩 Key Patterns & Concepts
- **Single pass array traversal**
- **Tracking two values**: largest & second largest
- Works even if there are duplicate elements.

---

## 🌍 Real-World Relevance / Industry Use
- Leaderboard ranking systems (e.g., finding second-best score).
- Sales data analysis — quickly getting the runner-up product.
- Competitive sports result processing.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Sort the array, pick second largest → `O(n log n)` time.
- **Optimal:** Track in one scan with two variables → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Important to handle arrays with less than 2 distinct elements.
- Resetting `secondLargest` when updating `largest` is key.
- Avoid counting duplicates as second largest.

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    public int getSecondLargest(int[] arr) {
        if (arr.length < 2) return -1;

        int larg = Integer.MIN_VALUE;
        int smal = Integer.MIN_VALUE;

        for (int num : arr) {
            if (num > larg) {
                smal = larg;
                larg = num;
            } else if (num > smal && num != larg) {
                smal = num;
            }
        }
        return (smal == Integer.MIN_VALUE) ? -1 : smal;
    }
}