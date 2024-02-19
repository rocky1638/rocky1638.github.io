# 1396. Design Underground System

```python
class UndergroundSystem:

    def __init__(self):
        # store cumulative time and number of trips from s1 to s2
        # s1: { s2_1: [cum_time, numtrips], s2_2: [cum_time, numtrips], ... }
        self.average_times = defaultdict(lambda: defaultdict(lambda: [0, 0]))
        # store map of people currently on a train
        # id: (entryStation, timeEntered)
        self.people = {}

    def checkIn(self, id: int, stationName: str, t: int) -> None:
        self.people[id] = (stationName, t)

    def checkOut(self, id: int, stationName: str, t: int) -> None:
        entryStation, entryTime = self.people[id]
        # cumulative time
        self.average_times[entryStation][stationName][0] += t - entryTime
        # total trips
        self.average_times[entryStation][stationName][1] += 1

    def getAverageTime(self, startStation: str, endStation: str) -> float:
        return self.average_times[startStation][endStation][0] / self.average_times[startStation][endStation][1]
```

- we use two [[hashmap|hashmaps]].
	- one to keep track of all the people currently on a train, where and when they got on.
	- another to keep track of the total time and total number of trips between all pairs of stations.

[[string]], [[lc-system-design]]