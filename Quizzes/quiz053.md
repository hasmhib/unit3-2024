# Quiz 053

<img width="max" alt="Screenshot 2024-03-21 at 3 38 50 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/97f21bd4-0e62-4748-8627-3da6890f4b7c">

## Code

```py
class palNum:
    def __init__(self, A, B):
        self.A = A
        self.B = B

    def get_pal_list(self):
        palindromic_numbers = [] 
        for num in range(self.A, self.B + 1):
            if str(num) == str(num)[::-1]:
                palindromic_numbers.append(num)
        return palindromic_numbers


pal_numbers = palNum(10, 199)
palindromic_numbers = pal_numbers.get_pal_list()
```

## Proof of work
<img width="max" alt="Screenshot 2024-03-21 at 3 49 03 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/e57765a7-279e-48aa-9aec-d19fb5fe2e91">

## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/6d53ebfe-4660-4fb2-a940-ee829d4dd652)
