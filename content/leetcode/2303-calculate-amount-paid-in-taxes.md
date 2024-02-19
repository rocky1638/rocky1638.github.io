# 2303. Calculate Amount Paid in Taxes

```python
class Solution:
    def calculateTax(self, brackets: List[List[int]], income: int) -> float:
        tax = 0

        for i, (upper, percent) in enumerate(brackets):
            pay_to_consider = min(upper, income)
            if i > 0:
                pay_to_consider -= brackets[i-1][0]
                
            if pay_to_consider > 0:
                tax += pay_to_consider * percent / 100

        return tax
```

- simple [[math]] problem.

[[array]]