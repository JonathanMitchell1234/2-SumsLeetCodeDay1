Explanation:

Iterate through the array with an outer loop using i as index

For each i, iterate through the rest of array using j

check sums of nums[i] and nums[j] = target

if true, return indicies
if false, return null

Optimized Solution with Hash Map: 

```function twoSum(nums, target) {
    const numToIndexMap = new Map();

    for (let i = 0; i < nums.length; i++) {
        const complement = target - nums[i];

        if (numToIndexMap.has(complement)) {
            return [numToIndexMap.get(complement), i];
        }

        numToIndexMap.set(nums[i], i);
    }

    return null; // No solution found
}
```# 2-SumsLeetCodeDay1
