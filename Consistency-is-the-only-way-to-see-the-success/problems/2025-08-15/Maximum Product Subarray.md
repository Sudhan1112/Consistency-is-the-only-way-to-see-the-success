# 📘 DSA Problem-Solving Journal  

## 📅 Date: 2025-08-15  
### 🧠 Problem Title  
**Platform:** GFG — [Maximum Product Subarray](https://www.geeksforgeeks.org/batch/gfg-160-problems/track/arrays-gfg-160/problem/maximum-product-subarray3604)  

### 📜 Problem Statement (Brief)  
Find the contiguous subarray within an array (containing at least one number) which has the largest product.  

### 🧩 Key Patterns & Concepts  
- Dynamic Programming with **tracking both max and min products**.  
- Multiplying by a negative number flips max ↔ min, so we must store both.  

### 🌍 Real-world Relevance  
- Stock trading (profit/loss sequences where negatives flip growth).  
- Signal processing where values can swing between amplification and attenuation.  

### 🥉 Brute Force Approach  
**Idea:** Try all subarrays, compute product for each.  
- **Time:** O(n²)  
- **Space:** O(1)  

### 🥇 Optimal Approach  
**Idea:** Use DP tracking `max_p` and `min_p` at each index.  
- Update `max_p = max(arr[i], max_p*arr[i], min_p*arr[i])`.  
- Update `min_p = min(arr[i], temp*arr[i], min_p*arr[i])`.  
- Keep global answer as max of all `max_p`.  

- **Time:** O(n)  
- **Space:** O(1)  

### 📚 Detailed Learning Notes  
- Multiplying by negatives flips the situation — that’s why we track both max and min.  
- Very similar thinking to Kadane’s Algorithm but with an extra dimension (min).  
- Learned the trick of using a `temp` variable to avoid overwriting `max_p` before updating `min_p`.  

### 💻 Code Snippet (Python)  
```python
def maxProduct(nums):
    ans = nums[0]
    max_p, min_p = nums[0], nums[0]

    for i in range(1, len(nums)):
        temp = max_p
        max_p = max(nums[i], max_p * nums[i], min_p * nums[i])
        min_p = min(nums[i], temp * nums[i], min_p * nums[i])
        ans = max(ans, max_p)
    
    return ans
