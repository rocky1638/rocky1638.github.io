---
created_at: 2022-11-23
type: leetcode
aliases: []
difficulty: 🟡
link: https://leetcode.com/problems/task-scheduler/
---

# 621. Task Scheduler

Given a characters array `tasks`, representing the tasks a CPU needs to do, where each letter represents a different task. Tasks could be done in any order. Each task is done in one unit of time. For each unit of time, the CPU could complete either one task or just be idle.

However, there is a non-negative integer `n` that represents the cooldown period between two **same tasks** (the same letter in the array), that is that there must be at least `n` units of time between any two same tasks.

Return _the least number of units of times that the CPU will take to finish all the given tasks_.

```python
class Solution:
    def leastInterval(self, tasks: List[str], n: int) -> int:
        # greedily run the most frequent task that is not on cooldown
        
        # priority queue that prioritizes:
            # availability first (cooldown time remaining, 0 means it can be ran now (min))
            # number of the task remaining (tasks with more remaining come first (max))
        
        counts = Counter(tasks)
        # [-numtasksremaining, task]
        heap_avail = []
        # [time_when_available, -numtasksremaining, task]
        heap_waiting = []
        for key in counts:
            heap_avail.append([-counts[key], key])
        
        # queue.append([time_available, -numtasksremaining, task])
        heapq.heapify(heap_avail)
        heapq.heapify(heap_waiting)
        
        t = 0
        while heap_avail or heap_waiting:
            if not heap_avail:
                # just advance because everything is on cooldown
                t += 1
            else:
                # use next heap_avail
                neg_count, task = heapq.heappop(heap_avail)
                count = -neg_count
                count -= 1
                
                if count > 0:
                    heapq.heappush(heap_waiting, [t+n+1, -count, task])
                t+=1
                
            # update heap_waiting, move any available now to heap_avail
            while heap_waiting:
                if heap_waiting[0][0] == t:
                    _, neg_count, task = heapq.heappop(heap_waiting)
                    heapq.heappush(heap_avail, [neg_count, task])
                else:
                    break
            
        return t
```

- the main thought process here is to greedily always perform the task that has the most instances left _(if it is not on cooldown)_.
- to do this, we use a [[priority-queue]] in the form of a [[heap]] to keep track of the frequency of the available tasks in order.
	- we also have to maintain a separate [[priority-queue]] of tasks that are on cooldown, so we can add them back to the queue of available tasks once the cooldown is over.

Categories:: [[greedy]], [[hashmap]], [[priority-queue]], [[heap]]
