# Quiz 050


## Code

```py
class Airlines:
    def __init__(self, flight_number, origin, destination, departure_time, duration):
        self.flight_number = flight_number
        self.origin = origin
        self.destination = destination
        self.departure_time = departure_time
        self.duration = duration

    def get_duration(self):
        h = self.duration[0]
        m = self.duration[1]
        s = self.duration[2]
        output = f"{h} hours {m} minutes and {s} seconds"
        return output

test1 = Airlines('ANA123', 'HND', 'NRT', "2024-02-19, 8:00AM", [1, 2, 3])
print(test1.get_duration())

test2 = Airlines('JAL501', 'NRT', 'KIX', "2024-05-01, 5:30AM", [16, 17, 18])
print(test2.get_duration())
```

## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 4 38 58 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b800f4d3-8663-48ed-bf6c-329bfa082c20">

## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/74254bf9-ddaa-4c67-843d-746b28660680)



