# Quiz 055
<img width="max" alt="Screenshot 2024-03-30 at 0 06 13 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/4963c1d8-45fa-40a6-9aa1-2185a95830f5">

## Code

```py
class Darts:
    def __init__(self):
        self.outer_radius = 10
        self.middle_radius = 5
        self.inner_radius = 1

    def score(self, x, y):
        distance = (x**2 + y**2)**0.5

        if distance > self.outer_radius:
            return 0  # Outside the target
        elif distance > self.middle_radius:
            return 1  # Outer circle
        elif distance > self.inner_radius:
            return 5  # Middle circle
        else:
            return 10  # Inner circle


darts_game = Darts()
print(darts_game.score(0, 0))
print(darts_game.score(10, 0))
print(darts_game.score(8, 8)) 
```

## Proof of work
<img width="max" alt="Screenshot 2024-03-30 at 0 07 12 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/c605cd8b-fcf7-44fe-a759-302f3241f035">

