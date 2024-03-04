---
title: 846. hand of straights
type: leetcode
aliases: 
difficulty: 🟡
link: https://leetcode.com/problems/hand-of-straights/
date: 2023-01-16
updated: 2024-02-28
tags:
  - greedy
  - array
  - sorting
---

Alice has some number of cards and she wants to rearrange the cards into groups so that each group is of size `groupSize`, and consists of `groupSize` consecutive cards.

Given an integer array `hand` where `hand[i]` is the value written on the `ith` card and an integer `groupSize`, return `true` if she can rearrange the cards, or `false` otherwise.

## solution

The idea is to sort the hand, and then just always add the next card to an available consecutive group if it’s available. We always add to the longest existing group possible, because that gives us the greatest chance to complete a group (greedy).

The tricky part is storing the work-in-progress groups.

The below solution keys the groups by their largest current value, and then stores the lengths of existing groups in a max heap.

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
		
		if groupSize == 1:
			return True
		
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
			if num - 1 in groups:
				group_size = -heapq.heappop(groups[num - 1])
				group_size += 1
				if group_size == groupSize:  # we're done a group
					total_formed += groupSize
				else:
					if num in groups:
						heapq.heappush(groups[num], -group_size)
					else:
						groups[num] = [-group_size]
			
			if len(groups[num - 1]) == 0:
				del groups[num - 1]
			else:
				if num in groups:
					heapq.heappush(groups[num], -1)
				else:
					groups[num] = [-1]
		
		return total_formed == len(hand)

```

Alternatively, we can also use a double-ended queue that stores in-progress straights as $(start, length)$. With each new card, we check from the start of this queue to see if we can add it to any existing in-progress straights, before starting a new hand.

This solution is theoretically slightly slower (we have a linear scan through the in-progress hands, instead of a constant time look up in the hash table).

```python
class Solution:
  def isNStraightHand(self, hand: List[int], groupSize: int) -> bool:
    if len(hand) % groupSize != 0:
      return False
    
    hand.sort()

    # hands_in_progress[i] = (start_val, length)
    hands_in_progress = deque()
    # greedily always try to finish/improve a hand
    # before starting a new hand
    for card in hand:
      added_to_existing_hand = False
      for i in range(len(hands_in_progress)):
        h = hands_in_progress[i]

        if card > h[0]+h[1]:
          return False

        if h[0]+h[1] == card:
          hands_in_progress[i][1] += 1
          added_to_existing_hand = True
          break
          
      if not added_to_existing_hand:
        hands_in_progress.append([card, 1])
      if hands_in_progress[0][1] == groupSize:
        hands_in_progress.popleft()
      
    return len(hands_in_progress) == 0

```

An even faster way to do this is to just greedily finish constructing each hand before moving onto the next one.

In the below solution, we construct a frequency dictionary of the values in `hand`, and then iterate through the `sorted` hand. One insight is that if we’re going to have a valid solution, we *must* have find a valid hand for the minimum value remaining in hand. For example, if we see a 1 when `groupSize` is 3, we know we must find the sequence `1,2,3` in `hand`.

Once we’re done constructing this hand, we continue looping through the sorted array until we find the next smallest unaccounted for number.

```python
class Solution:
	def isNStraightHand(self, hand: List[int], groupSize: int) -> bool:
	# Time: O(nlogn) + O(n*groupSize)
		counter = Counter(hand) # O(n)
		hand.sort() # O(nlogn)

		i = 0
		while i < len(hand):
			cur = hand[i]
			for j in range(groupSize): # O(groupSize)
				if cur+j not in counter:
					return False
				counter[cur+j] -= 1
				if counter[cur+j] == 0:
					del counter[cur+j]
			while i < n and hand[i] not in counter:
				i += 1
		return True
```
