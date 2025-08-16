# Second Largest Digit in a String — LeetCode

## 📜 Problem Statement
Given a string containing digits and letters, return the second largest digit present. If it doesn't exist, return -1.

---

## 🧩 Key Patterns & Concepts
- **String traversal with digit check**
- Track `largest` and `secondLargest` without sorting.
- Ignore letters entirely.

---

## 🌍 Real-World Relevance / Industry Use
- Parsing user input where both digits and characters exist.
- Extracting top two numeric priorities from mixed-format data.
- Detecting second highest score in text logs.

---

## 🥊 Brute Force vs Optimal
- **Brute Force:** Extract digits, sort, pick → `O(n log n)`.
- **Optimal:** One pass → `O(n)` time, `O(1)` space.

---

## 📒 Learning Notes
- Always check if char is digit before processing.
- Maintain strict inequality to avoid duplicate largest value.

---

## 💻 Code Snippet with Explanation
```java
class Solution {
    public int secondHighest(String s) {
        int largest = Integer.MIN_VALUE;
        int secondLargest = Integer.MIN_VALUE;

        for (char c : s.toCharArray()) {
            if (Character.isDigit(c)) {
                int num = c - '0';
                if (num > largest) {
                    secondLargest = largest;
                    largest = num;
                } else if (num > secondLargest && num < largest) {
                    secondLargest = num;
                }
            }
        }
        return (secondLargest == Integer.MIN_VALUE) ? -1 : secondLargest;
    }
}