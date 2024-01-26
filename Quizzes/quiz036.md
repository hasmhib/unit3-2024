# Quiz 036
<img width="max" alt="Screenshot 2024-01-14 at 4 43 45 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/e9d87bf1-cd4a-4bf1-9adf-680d4ee9cc4c">

## Code

```py
class Converter:
    def __init__(self):
        self.roman_digits = {100: "C", 90: "XC", 50: "L", 40: "XL", 10: "X", 9: "IX", 5: "V", 4: "IV", 1: "I"}

    def convert_to_roman(self, number):
        if 0 < number <= 100:
            output = ""
            for value in [100, 90, 50, 40, 10, 9, 5, 4, 1]:
                p = self.roman_digits[value]
                q = number // value
                number = number % value
                output += p * q
            return output
        else:
            return "Invalid input"

converter = Converter()
print(converter.convert_to_roman(34))
```

## Proof of work
<img width="max" alt="Screenshot 2024-01-14 at 7 41 02 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/e5354117-cbe4-429c-996b-4fefefa67a60">
