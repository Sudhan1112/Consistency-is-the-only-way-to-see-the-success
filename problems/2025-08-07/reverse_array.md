# Reverse Array — GFG

## 📜 Problem Statement
Reverse the elements of an array in-place.

---

## 🧩 Key Patterns & Concepts
- **Two-pointer swapping**
- Converging from both ends toward the center.

---

## 🌍 Real-World Relevance / Industry Use
- Reversing playback order in a music/video playlist.
- Reversing processing queue for LIFO simulations.
- Undo/Redo stack reversals in applications.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Create new reversed array → `O(n)` time, `O(n)` space.
- **Optimal:** Swap in place → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Always move pointers inward after each swap.
- Works for both odd and even length arrays.

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    public void reverseArray(int arr[]) {
        int j = 0;
        int i = arr.length - 1;
        while (j < i) {
            int temp = arr[j];
            arr[j] = arr[i];
            arr[i] = temp;
            j++;
            i--;
        }
    }
}