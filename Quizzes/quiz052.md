# Quiz 052
<img width="max" alt="Screenshot 2024-03-21 at 3 24 42 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/4081410b-9e66-4108-b159-f786d882260e">


## Code

```py
class Wheel:
    def __init__(self, size):
        self.size = size

    def get_size(self):
        return self.size

    def get_perimeter(self):
        return self.size * 3.14

    def get_km_per_rotation(self):
        # (1 inch = 0.0000254 km)
        return self.get_perimeter() * 0.0000254


class Bicycle:
    def __init__(self, wheel_size, frame_material):
        self.wheel = Wheel(wheel_size)
        self.frame_material = frame_material

    def ride(self):
        print(f"Bicycle with wheel size {self.wheel.get_size()}-inch and frame {self.frame_material}.")


bicycle = Bicycle(26, "aluminum")

bicycle.ride()

km_per_rotation = bicycle.wheel.get_km_per_rotation()
print(km_per_rotation)
```

## Proof of work
<img width="max" alt="Screenshot 2024-03-21 at 3 35 30 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/56f8cda6-5bf2-4adf-a78f-672dad199d52">


## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/929c5123-3797-4c43-8ecb-fe8a7648012d)


