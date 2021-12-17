# largestGapMobProgramming
https://binarysearch.com/problems/Largest-Gap

Given a list of integers nums, return the largest difference of two consecutive integers in the sorted version of nums.

Constraints

n ≤ 100,000 where n is the length of nums

## Solution:

```js

class Solution {
    solve(nums) {
        nums = nums.sort((a,b) => a - b)
        let count = 0
        nums.forEach((val, ind) => {
            if (ind < nums.length-1){
                if (nums[ind + 1] - val > count){
                    count = nums[ind + 1] - val
                }
            }
        })
        return count;
    }
}

```
