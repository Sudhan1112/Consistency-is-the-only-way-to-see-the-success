📅 Date: 2025-08-13
🧠 Problem Title

Platform: GFG — Stock Buy and Sell (Max One Transaction Allowed)

📜 Problem Statement (Brief)

Given stock prices for n days, find the maximum profit possible with at most one buy and one sell.

🧩 Key Patterns & Concepts

Track minimum price so far

Calculate max profit dynamically

Single pass greedy scan

🌍 Real-world Relevance

One-time investment decisions

Buying and selling foreign currency at optimal time

Event-driven commodity purchase

🥉 Brute Force Approach

Idea:
Check all pairs of days (buy, sell) and take the maximum profit.

Time: O(n²)
Space: O(1)

🥇 Optimal Approach

Idea:
Track the lowest price so far and update max profit if current price - min price is greater.

Time: O(n)
Space: O(1)

📚 Detailed Learning Notes

Min price tracking is the core — don’t update profit if price drops.

Simpler than multiple-transaction version — no sum accumulation.

Works in one scan without extra arrays.

💻 Code Snippet (Java)
class Solution {
    public int maximumProfit(int prices[]) {
        int min_p = prices[0];
        int max_p = 0;
        for (int i = 1; i < prices.length; i++) {
            if (prices[i] < min_p) {
                min_p = prices[i];
            } else {
                max_p = Math.max(max_p, prices[i] - min_p);
            }
        }
        return max_p;
    }
}