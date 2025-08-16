# Next Permutation — GFG

## 📜 Problem Statement
Transform the given array into the lexicographically next greater permutation.  
If not possible, rearrange to the lowest permutation.

---

## 🧩 Key Patterns & Concepts
- **Pivot finding**: first decreasing element from right.
- **Swap pivot** with just larger element.
- **Reverse suffix** to get smallest arrangement.

---

## 🌍 Real-World Relevance / Industry Use
- Generating next test case in combinatorics.
- Next order of items in warehouse picking.
- Possible product configurations listing.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Generate all permutations and pick next → `O(n!)`.
- **Optimal:** Identify pivot and rearrange → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Pivot search must start from right end.
- After swapping, suffix is always in descending order — reverse it.

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    void swap(int[] arr, int a, int b) {
        int temp = arr[a];
        arr[a] = arr[b];
        arr[b] = temp;
    }

    void reverse(int[] arr, int left, int right) {
        while (left < right) {
            swap(arr, left++, right--);
        }
    }

    void nextPermutation(int[] arr) {
        int n = arr.length;
        int i = n - 2;

        while (i >= 0 && arr[i] >= arr[i + 1]) {
            i--;
        }

        if (i >= 0) {
            int j = n - 1;
            while (arr[j] <= arr[i]) {
                j--;
            }
            swap(arr, i, j);
        }

        reverse(arr, i + 1, n - 1);
    }
}