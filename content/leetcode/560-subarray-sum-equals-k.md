# 560. Subarray Sum Equals K

```python
class Solution:
    def subarraySum(self, nums: List[int], k: int) -> int:
        ans = 0
        # count the number of times each prefix sum appears
        d = collections.defaultdict(int)
        d[0] = 1
        tally = 0
        for i, num in enumerate(nums):
            tally += num
            ans += d[tally-k]
            d[tally] += 1
        return ans
```

- we use the idea of [[prefix-sum]] to more efficiently compute the sums of subarrays.
- initially, i thought to iterate through the prefix sums, and for each, to look back and see if any shorter prefixes could be subtracted to reach target $k$.
	- this would be $O(n^2)$.
- i then thought to optimize by using a [[hashmap]] to store the indices that had prefixes of certain values, then, when we iterate through the prefix array, we can check to see how many of the indices are before our current index.
	- This would require some sort of $O(n)$ or $O(\log n)$ operation, to find which indices were valid.
	- this would be $O(n\log n)$.
- we can further optimize this by building the [[hashmap]] and [[prefix-sum]] [[array]] while iterating through the array!
	- that way, the hashmap will only ever note earlier prefixes, and so indexes don’t even need to be stored, but instead just a count of how many prefix arrays sum to each value.
	- this is $O(n)$.