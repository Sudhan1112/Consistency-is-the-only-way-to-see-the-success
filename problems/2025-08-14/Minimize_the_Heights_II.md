📅 Date: 2025-08-14
🧠 Problem Title

Platform: GFG — Minimize the Heights II

📜 Problem Statement (Brief)

Given heights of towers and a value k, increase or decrease each tower height by exactly k and minimize the difference between the tallest and shortest tower.

🧩 Key Patterns & Concepts

Sorting + Greedy

Adjusting smallest and largest values

Trying every split point for min difference

🌍 Real-world Relevance

Signal strength tuning in networks

Product dimension adjustments in manufacturing

Balancing workloads in distributed systems

🥉 Brute Force Approach

Idea:
Try all ±k combinations for each tower, find min difference.

Time: O(2ⁿ) — infeasible for large n
Space: O(1)

🥇 Optimal Approach

Idea:
Sort array, set initial min/max after adding/subtracting k, then iterate to find smallest possible difference.

Time: O(n log n) — sorting dominates
Space: O(1)

📚 Detailed Learning Notes

Sorting first helps consider height changes in order.

Always check for negative heights before applying change.

A good example of reducing complexity using ordering.

💻 Code Snippet (Java)
import java.util.*;

class Solution {
    public int getMinDiff(int[] arr, int k) {
        int n = arr.length;
        Arrays.sort(arr);
        int ans = arr[n - 1] - arr[0];
        int s = arr[0] + k;
        int l = arr[n - 1] - k;
        
        for (int i = 1; i < n; i++) {
            int mi = Math.min(s, arr[i] - k);
            int ma = Math.max(l, arr[i - 1] + k);
            if (mi >= 0) ans = Math.min(ans, ma - mi);
        }
        return ans;
    }
}