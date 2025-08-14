## 📅 Date: 2025-08-13
### 🧠 Problem Title  
**Platform:** GFG — Stock Buy and Sell (Multiple Transactions Allowed)

### 📜 Problem Statement (Brief)  
Given stock prices for `n` days, maximize profit when you are allowed to make multiple buy/sell transactions (but cannot hold more than one stock at a time).

### 🧩 Key Patterns & Concepts  
- Greedy profit accumulation
- Only buy before a rise, sell before a fall
- Sum up every profitable upward movement

### 🌍 Real-world Relevance  
- Stock market short-term trading strategies
- Cryptocurrency day-trading bots
- Seasonal commodity buying/selling cycles

---

### 🥉 Brute Force Approach  
**Idea:**  
Try all buy-sell pairs and track total profit.

**Time:** O(n²)  
**Space:** O(1)  

---

### 🥇 Optimal Approach  
**Idea:**  
Iterate through the prices array, and whenever today’s price is higher than yesterday’s, add the difference to profit.

**Time:** O(n) — single pass  
**Space:** O(1) — only one profit counter  

---

### 📚 Detailed Learning Notes  
- This problem is purely greedy — you never miss profit opportunities.  
- The “multiple transactions” condition makes it different from the max-one-transaction variant.  
- Avoids tracking exact buy/sell days — profit calculation is enough.

---

### 💻 Code Snippet (Java)
```java
class Solution {
    public int maximumProfit(int prices[]) {
        int result = 0;
        for (int i = 1; i < prices.length; i++) {
            if (prices[i] > prices[i - 1]) {
                result += prices[i] - prices[i - 1];
            }
        }
        return result;
    }
}
