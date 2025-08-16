# Move All Zeroes to End — GFG

## 📜 Problem Statement
Given an array, move all zeroes to the end without changing the order of non-zero elements.

---

## 🧩 Key Patterns & Concepts
- **Two-pointer technique**
- Stable rearrangement of elements.
- Preserves order of non-zero values.

---

## 🌍 Real-World Relevance / Industry Use
- Data cleaning — pushing placeholder values (0) to end for easier processing.
- UI element rendering — move inactive items to the end of a display list.
- E-commerce inventory — pushing out-of-stock (0 quantity) products to the end.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Create new array for non-zeros, fill with zeros later → `O(n)` but uses extra `O(n)` space.
- **Optimal:** In-place shifting using pointer `j` → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Maintaining index for next non-zero insertion is critical.
- Ensure no unnecessary swaps (just overwrite).

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    void pushZerosToEnd(int[] arr) {
        int j = 0; // next position for non-zero
        for (int i = 0; i < arr.length; i++) {
            if (arr[i] != 0) {
                arr[j] = arr[i];
                j++;
            }
        }
        while (j < arr.length) {
            arr[j] = 0;
            j++;
        }
    }
}
