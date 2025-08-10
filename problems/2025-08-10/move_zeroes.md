# Move Zeroes — LeetCode

## 📜 Problem Statement
Move all zeroes in an array to the end while maintaining order of non-zero elements.

---

## 🧩 Key Patterns & Concepts
- **Two-pointer technique** (same as "Move All Zeroes to End").
- Stable order preservation.

---

## 🌍 Real-World Relevance / Industry Use
- Similar to GFG version, applies in cleaning sparse data sets.
- Optimizing UI element placement in rendering loops.
- Financial data processing — pushing inactive records to end.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Create a new array → `O(n)` with extra space.
- **Optimal:** In-place overwrite → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Reinforced concept by solving in multiple platforms.
- Same core approach but different platform syntax.

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    public void moveZeroes(int[] nums) {
        int j = 0;
        for (int i = 0; i < nums.length; i++) {
            if (nums[i] != 0) {
                nums[j] = nums[i];
                j++;
            }
        }
        while (j < nums.length) {
            nums[j] = 0;
            j++;
        }
    }
}