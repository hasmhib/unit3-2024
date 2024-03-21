# Quiz 054
<img width="1147" alt="Screenshot 2024-03-21 at 4 16 24 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b0436e59-4d55-4c34-a065-37cdc60c50e0">

## Code

```py
class RainDrops:
    def pour(n: int) -> str:
        result = ''
        if n % 3 == 0:
            result += 'Pling'
        if n % 5 == 0:
            result += 'Plang'
        if n % 7 == 0:
            result += 'Plong'
        return result if result else str(n)

# Testing the function with the given examples to verify correctness
test_cases = [28, 30, 34]
outputs = [RainDrops.pour(n) for n in test_cases]
print(outputs)
```

## Proof of work
