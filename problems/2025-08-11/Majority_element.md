## 📅 Date: 2025-08-11  
### 🧠 Problem Title  
**Platform:** — Majority Element (More than ⌊n/3⌋ times)  

### 📜 Problem Statement (Brief)  
Find all elements in an array that occur more than ⌊n/3⌋ times. Return them sorted.  

### 🧩 Key Patterns & Concepts  
- Frequency counting  
- Sorting vs. Boyer–Moore Majority Vote algorithm (n/3 variation)  
- At most 2 elements can appear more than ⌊n/3⌋ times  

### 🌍 Real-world Relevance  
- Identifying “high engagement” items in user activity logs  
- Detecting dominant trends or modes in streaming data  
- Summarizing market basket items with strong frequency bias  

---

### 🥉 Brute Force / Your Approach  
**Idea:**  
Sort the array and count consecutive occurrences to determine frequency. Keep those above the ⌊n/3⌋ threshold.  

**Time:** O(n log n) — dominated by sorting  
**Space:** O(1) extra (O(n) if storing frequency map explicitly)  

---

### 🥇 Optimal Approach  
**Idea:**  
Use the Boyer–Moore Majority Vote algorithm (adapted for n/3). First pass finds at most 2 candidates by "voting" and canceling counts. Second pass verifies actual counts.  

**Time:** O(n) — two linear passes  
**Space:** O(1) — constant extra variables  

---

### 📚 Detailed Learning Notes  
- Threshold is based on total length `n`, not unique count.  
- Sorting is fine for quick implementation, but for n up to 10^6, O(n) is better.  
- Boyer–Moore works because there can be at most 2 majority elements when the threshold is n/3.  
- Verification step is essential to avoid returning false candidates.  
- Problem also hints at the “more than n/k” generalization pattern, where k-1 candidates exist.  

---

### 💻 Code Snippet — Your Sort-based Approach (Java)  
```java
import java.util.*;

class SolutionSortApproach {
    public List<Integer> findMajority(int[] arr) {
        int n = arr.length;
        Arrays.sort(arr);
        List<Integer> result = new ArrayList<>();
        int count = 1;

        for (int i = 1; i <= n; i++) {
            if (i < n && arr[i] == arr[i - 1]) {
                count++;
            } else {
                if (count > n / 3) {
                    result.add(arr[i - 1]);
                }
                count = 1;
            }
        }
        return result;
    }
}
````

---

### 💻 Code Snippet — Optimal Boyer–Moore n/3 (Java)

```java
import java.util.*;

class SolutionOptimal {
    public List<Integer> findMajority(int[] arr) {
        int n = arr.length;
        int candidate1 = 0, candidate2 = 0;
        int count1 = 0, count2 = 0;

        // Voting phase
        for (int num : arr) {
            if (num == candidate1) {
                count1++;
            } else if (num == candidate2) {
                count2++;
            } else if (count1 == 0) {
                candidate1 = num;
                count1 = 1;
            } else if (count2 == 0) {
                candidate2 = num;
                count2 = 1;
            } else {
                count1--;
                count2--;
            }
        }

        // Verification phase
        count1 = 0;
        count2 = 0;
        for (int num : arr) {
            if (num == candidate1) count1++;
            else if (num == candidate2) count2++;
        }

        List<Integer> result = new ArrayList<>();
        if (count1 > n / 3) result.add(candidate1);
        if (count2 > n / 3) result.add(candidate2);
        Collections.sort(result);
        return result;
    }
}
```
