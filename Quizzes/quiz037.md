# Quiz 037
<img width="max" alt="Screenshot 2024-01-26 at 4 50 10 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/87350df2-0204-4596-8e66-684e2141c01a">

## Code

```py
class CompoundInterest:
    def __init__(self, principal: int, rate: float, number_of_years: int):
        self.principal = principal
        self.rate = rate
        self.number_of_years = number_of_years

    def compound_interest_calculator(self):
        return self.principal * (1 + self.rate) ** self.number_of_years

class AccountingProgram(CompoundInterest):
    def __init__(self, principal: int, rate: float, number_of_years: int):
        super().__init__(principal, rate, number_of_years)

    def calculate_interest(self):
        return self.compound_interest_calculator()

test = AccountingProgram(principal=100, rate=0.1, number_of_years=20)
print(test.calculate_interest())

```

## Proof of work
<img width="max" alt="Screenshot 2024-01-26 at 4 55 49 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/700cb869-7a1c-4870-be1a-88e685642723">

## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/46378aaf-6079-43a1-9a3c-39d658a1408b)


