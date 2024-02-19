---
created_at: 2023-01-03
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/car-fleet/
---

# 853. Car Fleet

There are `n` cars going to the same destination along a one-lane road. The destination is `target` miles away.

You are given two integer array `position` and `speed`, both of length `n`, where `position[i]` is the position of the `ith` car and `speed[i]` is the speed of the `ith` car (in miles per hour).

A car can never pass another car ahead of it, but it can catch up to it and drive bumper to bumper **at the same speed**. The faster car will **slow down** to match the slower car's speed. The distance between these two cars is ignored (i.e., they are assumed to have the same position).

A **car fleet** is some non-empty set of cars driving at the same position and same speed. Note that a single car is also a car fleet.

If a car catches up to a car fleet right at the destination point, it will still be considered as one car fleet.

Return _the **number of car fleets** that will arrive at the destination_.

```python
class Solution:
    def willCatchUp(self, backCar, frontCar, target):
        """
        a + sa * t = b + sb * t
        a - b = sb*t - sa*t
        t = (a-b) / (sb-sa)

        meeting location = a + sa * t
        """

        if backCar[1] > frontCar[1]: # will catch up eventually
            timeToMeet = (frontCar[0] - backCar[0]) / (backCar[1] - frontCar[1])
            meetingLocation = frontCar[0] + frontCar[1] * timeToMeet

            return meetingLocation <= target
        return False


    def carFleet(
	    self,
		target: int,
		position: List[int],
		speed: List[int]
	) -> int:
        combined = sorted(
	        [(pos, spd) for pos, spd in zip(position, speed)], key=lambda x: x[0]
        )

        stack = []

        for pos, spd in combined:
            while len(stack) and self.willCatchUp(stack[-1], (pos, spd), target):
                stack.pop()
            stack.append((pos, spd))
                
        return len(stack)
```

- the idea here is to use a monotonic stack to eliminate all cars that will catch up to another car before or at the `target` distance.
- we sort the array by starting position.
	- we append cars by their starting positions _(ascending)_.
	- when we append a car, we look through the stack to see if any cars starting at an earlier position will reach the current car.
		- _(the math for this is explained in the code comment)_.
		- if they will, then pop that previous car from the stack _(they will be part of the fleet led by the current car)_.
		- once all previous cars have been merged, we append the current car to the stack.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[stack]], [[array]], [[monotonic-stack]], [[sorting]]
