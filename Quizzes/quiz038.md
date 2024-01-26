# Quiz 038
<img width="max" alt="Screenshot 2024-01-26 at 4 57 07 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b087defc-09a6-444c-a6dd-92664627ab1a">


## Code

```py
import random
import matplotlib.pyplot as plt

class SalesmanMap:
    def __init__(self):
        self.x = []
        self.y = []
        self.names = None

    def set_names(self, base_names):
        self.names = base_names

    def get_map(self):
        for i in range(len(self.names)):
            self.x.append(random.randint(0, 100))
            self.y.append(random.randint(0, 100))

        for i, name in enumerate(self.names):
            plt.scatter(self.x[i], self.y[i])
            plt.text(self.x[i], self.y[i], name)

        plt.show()

c = SalesmanMap()
c.set_names(['Kobe', 'Sapporo', 'Nagoya', 'kawasaki', 'Kyoto', 'Fukuoka', 'Saitama', 'Yokohama', 'Osaka'])
c.get_map()

```

## Proof of work
<img width="max" alt="Screenshot 2024-01-26 at 5 01 44 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/8fccf8fa-9a5c-45ab-9933-1712f407e088">


## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/87fe9c51-07a4-41ea-b665-e5333eee2e90)

