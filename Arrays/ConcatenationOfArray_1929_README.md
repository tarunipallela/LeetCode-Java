# 🧩 LeetCode Problem 1929: Concatenation of Array

🔗 **Problem Link**: [https://leetcode.com/problems/concatenation-of-array/](https://leetcode.com/problems/concatenation-of-array/)

---

## 📝 Problem Statement

Given an integer array `nums` of length `n`, you want to create an array `ans` of length `2n` where:

- `ans[i] == nums[i]`  
- `ans[i + n] == nums[i]`  
  for `0 <= i < n`.

Return the array `ans`.

---

## 🧪 Example 1

**Input:**
nums = [1, 2, 1]

**Output:**
[1, 2, 1, 1, 2, 1]

**Explanation:**  
We repeat the array twice:  
→ First half: [1, 2, 1]  
→ Second half: [1, 2, 1] (again)

---

## 🧪 Example 2

**Input:**
nums = [1, 3, 2, 1]

**Output:**
[1, 3, 2, 1, 1, 3, 2, 1]
---

## 💡 Approach

1. Create a new array `ans` of size `2n` where `n` is the length of `nums`.
2. Loop through `nums` using index `i` from `0` to `n - 1`.
3. For each element `nums[i]`, assign:
   - `ans[i] = nums[i]`
   - `ans[i + n] = nums[i]`
4. Return `ans`.

---

## ✅ Java Code

```java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int n = nums.length;
        int[] ans = new int[2 * n];
        for (int i = 0; i < n; i++) {
            ans[i] = nums[i];
            ans[i + n] = nums[i];
        }
        return ans;
    }
}
📊 Time & Space Complexity
Complexity	Description
⏱️ Time	O(n) — We loop through the array once
🧠 Space	O(2n) → O(n) — New array created
