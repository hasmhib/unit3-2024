# Quiz 054
<img width="1147" alt="Screenshot 2024-03-21 at 4 16 24 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b0436e59-4d55-4c34-a065-37cdc60c50e0">

## Code

```py
class RainDrops:
    def pour(n: int) -> str:
        divisible = []
        result = ""

        if n % 3 == 0:
            divisible.append('3')
            result += "Pling"
        if n % 5 == 0:
            divisible.append('5')
            result += "Plang"
        if n % 7 == 0:
            divisible.append('7')
            result += "Plong"

        if not divisible:
            return f"{n} is not divisible by 3, 5, or 7, so the result would be {n}"

        divisible_num = ' and ' .join(divisible)
        return f"{n} is divisible by {divisible_num}, so the result would be {result}"


print(RainDrops.pour(28))
print(RainDrops.pour(30))
print(RainDrops.pour(34))
```

## Proof of work
<img width="max" alt="Screenshot 2024-03-21 at 5 00 40 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/d7f9c593-92dc-4c3d-8a5b-430f19e064b6">


## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/64c2be81-1d8c-4869-8578-c292d744afb4)
