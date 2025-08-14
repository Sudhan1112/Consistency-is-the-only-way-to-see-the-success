📅 Date: 2025-08-14
🧠 Problem Title

Platform: GFG — Kadane’s Algorithm

📜 Problem Statement (Brief)

Find the maximum sum of any contiguous subarray in the given array.

🧩 Key Patterns & Concepts

Dynamic programming (prefix sums in disguise)

Local vs. global max tracking

Avoids recomputing sums

🌍 Real-world Relevance

Maximum profit/loss over continuous days

Best-performing segment in analytics data

Identifying optimal streak in gaming scores

🥉 Brute Force Approach

Idea:
Check all possible subarrays and track the largest sum.

Time: O(n²)
Space: O(1)

🥇 Optimal Approach

Idea:
Iterate once, updating current sum and global max. If current sum drops below current element, restart at that element.

Time: O(n)
Space: O(1)

📚 Detailed Learning Notes

Kadane’s skips negative carryover by restarting sum.

Works for arrays with negative numbers if handled carefully.

Also useful for circular array problems (modified version).

💻 Code Snippet (Java)
class Solution {
    int maxSubarraySum(int[] arr) {
        int ans = arr[0];
        int cur_s = arr[0];
        for (int i = 1; i < arr.length; i++) {
            cur_s = Math.max(arr[i], cur_s + arr[i]);
            ans = Math.max(ans, cur_s);
        }
        return ans;
    }
}
