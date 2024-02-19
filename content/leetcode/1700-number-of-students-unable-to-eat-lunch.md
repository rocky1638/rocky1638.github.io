---
created_at: 2023-01-27
type: leetcode
aliases: []
difficulty: 🟢
link: https://leetcode.com/problems/number-of-students-unable-to-eat-lunch/
---

# 1700. Number Of Students Unable To Eat Lunch

The school cafeteria offers circular and square sandwiches at lunch break, referred to by numbers `0` and `1` respectively. All students stand in a queue. Each student either prefers square or circular sandwiches.

The number of sandwiches in the cafeteria is equal to the number of students. The sandwiches are placed in a **stack**. At each step:

- If the student at the front of the queue **prefers** the sandwich on the top of the stack, they will **take it** and leave the queue.
- Otherwise, they will **leave it** and go to the queue's end.

This continues until none of the queue students want to take the top sandwich and are thus unable to eat.

You are given two integer arrays `students` and `sandwiches` where `sandwiches[i]` is the type of the `i​​​​​​th` sandwich in the stack (`i = 0` is the top of the stack) and `students[j]` is the preference of the `j​​​​​​th` student in the initial queue (`j = 0` is the front of the queue). Return _the number of students that are unable to eat._

```python
class Solution:
    def countStudents(self, students: List[int], sandwiches: List[int]) -> int:
        q = deque(students)
        sandwiches.reverse()
        
        skipped = 0
        
        while True:
            if skipped == len(q) or len(sandwiches) == 0:
                return len(q)
            
            if q[0] == sandwiches[-1]:
                q.popleft()
                sandwiches.pop()
                skipped = 0
            
            else:
                q.append(q.popleft()) # move to back of line
                skipped += 1
        
        return len(q)
```

- pretty basic dealing with stacks and queues.

```dataview
table without id file.inlinks as Backlinks
where file.name = this.file.name
```

## Related.

## References.

Categories:: [[array]], [[stack]], [[queue]]
