# Quiz 050
<img width="max" alt="Screenshot 2024-02-20 at 7 16 08 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/52753a08-3e4d-4f8f-95f5-c25a47efa6d1">


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

test1 = Airlines('AA123', 'New York', 'Los Angeles', "10:00AM", [5, 30, 3])
print(test1.get_duration())

```


## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 7 18 48 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/445f32e3-4647-412b-89f3-9afddd1d2f71">

## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/74254bf9-ddaa-4c67-843d-746b28660680)



