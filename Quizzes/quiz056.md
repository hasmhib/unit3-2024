# Quiz 056
<img width="max" alt="Screenshot 2024-03-30 at 0 08 37 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/41511b6a-5a00-408c-94f4-fb33657e7a00">

## Code

```py
def secret_handshake(code):
    if not 1 <= code <= 31:
        return "Code must be between 1 and 31"

    actions = ["wink", "double blink", "close your eyes", "jump"]
    handshake = []

    for i in actions:
        if code % 2 == 1:
            handshake.append(i)
        code = code // 2

    if code > 0:
        handshake.reverse()

    return handshake

print(secret_handshake(9))
```

## Proof of work
<img width="max" alt="Screenshot 2024-03-30 at 2 08 39 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/3a7c7af8-3a21-4b32-8061-5890a93215e5">

