## 📅 Date: YYYY-MM-DD  
### 🧠 Problem Title  
**Platform:** (e.g., LeetCode #344)  

### 📜 Problem Statement (Brief)  
Short 1–2 sentence version of the problem.  

### 🧩 Key Patterns & Concepts  
Main approach/pattern used.  

### 🌍 Real-world Relevance  
How or where this applies outside of coding challenges.  

### 🥉 Brute Force Approach  
**Idea:** Short description.  

**Time:** O(?)  

**Space:** O(?)  

### 🥇 Optimal Approach  
**Idea:** Short description.  

**Time:** O(?)  

**Space:** O(?)  

### 📚 Detailed Learning Notes  
Insights you gained, mistakes avoided, tricks learned.  

### 💻 Code Snippet (Python)  
```python
# Your code here
````

---

## Example — Reverse Array

📅 Date: 2025-08-07

**Platform:** —

**Problem Statement:** Reverse the elements of an array in-place.

**Key Patterns & Concepts:**

* Two-pointer swap from both ends toward center.

**Real-world Relevance:**

* Data reversal in media buffers, undo operations, queue/stack transformations.

**Brute Force:**

* Make a new array, push elements from last to first.
* **Time:** O(n)
* **Space:** O(n)

**Optimal:**

* Swap in-place using two pointers.
* **Time:** O(n)
* **Space:** O(1)

**Learning Notes:**

* Two-pointer is memory efficient.
* Often avoids the overhead of extra data structures.

**Code:**

```python
def reverse_array(arr):
    left, right = 0, len(arr) - 1
    while left < right:
        arr[left], arr[right] = arr[right], arr[left]
        left += 1
        right -= 1
    return arr
```