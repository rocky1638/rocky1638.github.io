---
created_at: 2023-01-16
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/hand-of-straights/
---

# 846. Hand Of Straights

Alice has some number of cards and she wants to rearrange the cards into groups so that each group is of size `groupSize`, and consists of `groupSize` consecutive cards.

Given an integer array `hand` where `hand[i]` is the value written on the `ith` card and an integer `groupSize`, return `true` if she can rearrange the cards, or `false` otherwise.

```python
class Solution:
    def isNStraightHand(self, hand: List[int], groupSize: int) -> bool:
        """
        - sort the hand.
        - go through, if number fits on a group of consecutive,
          greedily add it.
        - else, start a new hand.
        - O(nlogn) time, O(n) space.
        """

        if groupSize == 1: return True

        # can't divide if not divisible
        if len(hand) % groupSize != 0:
            return False
        
        hand.sort()
        total_formed = 0
        # groups[cur_largest_value] =
            # maxheap(lengths of sequences that end with this value)
        groups = {}
        for num in hand:
            # there are existing sequences that end with num
            if num-1 in groups:
                group_size = -heapq.heappop(groups[num-1])
                group_size += 1
                if group_size == groupSize: # we're done a group
                    total_formed += groupSize
                else:
                    if num in groups:
                        heapq.heappush(groups[num], -group_size)
                    else:
                        groups[num] = [-group_size]

                if len(groups[num-1]) == 0:
                    del groups[num-1]
            else:
                if num in groups:
                    heapq.heappush(groups[num], -1)
                else:
                    groups[num] = [-1]

        return total_formed == len(hand)
```

- the idea is to sort the hand, and then just always add the next card to an available consecutive group if it’s available.
	- we always add to the longest existing group possible, because that gives us the greatest chance to complete a group (greedy).
- the tricky part is storing the work-in-progress groups.
	- i decided to key the groups by their largest current value, and then store the lengths of existing groups in a max heap.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[greedy]], [[heap]], [[hashmap]], [[array]]
