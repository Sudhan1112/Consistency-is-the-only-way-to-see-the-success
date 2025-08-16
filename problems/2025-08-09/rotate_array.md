# Rotate Array — GFG

## 📜 Problem Statement
Rotate an array by `d` elements in a counter-clockwise direction in-place.

---

## 🧩 Key Patterns & Concepts
- **Array rotation via reversal algorithm**
- Steps:
  1. Reverse first `d` elements
  2. Reverse remaining elements
  3. Reverse the whole array
- Handles cases where `d > n` using modulo.

---

## 🌍 Real-World Relevance / Industry Use
- Scheduling tasks in cyclic order.
- Circular buffer manipulation.
- Data shuffling for cryptography.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Shift elements one by one → `O(n*d)` time.
- **Optimal:** 3-step reversal → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Modulo helps avoid unnecessary rotations when `d > n`.
- This approach avoids extra space and minimizes swaps.

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    static void rev_arr(int arr[], int start, int end) {
        while (start < end) {
            int temp = arr[start];
            arr[start] = arr[end];
            arr[end] = temp;
            start++;
            end--;
        }
    }

    static void rotateArr(int arr[], int d) {
        int size = arr.length;
        d = d % size;
        if (d == 0) return;

        rev_arr(arr, 0, d - 1);
        rev_arr(arr, d, size - 1);
        rev_arr(arr, 0, size - 1);
    }
}
