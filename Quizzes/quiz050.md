# Quiz 050
<img width="max" alt="Screenshot 2024-02-20 at 7 16 08 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/52753a08-3e4d-4f8f-95f5-c25a47efa6d1">

## 1. Create the method get_duration() that returns the duration as a string “5 hours 30 minutes and 3 seconds”

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

## 2. Create two objects of the Flight class and demonstrate how to use the class to represent flights offered by an airline. 

```.py
# Codes are same

flight1 = Airlines("AA123", "New York", "Los Angeles", "10:00 AM", [5, 30, 3])

print("Flight 1 Details:")
print(f"Flight Number: {flight1.flight_number}")
print(f"Origin: {flight1.origin}")
print(f"Destination: {flight1.destination}")
print(f"Departure Time: {flight1.departure_time}")
print(f"Duration: {flight1.get_duration()}")

flight2 = Airlines("BA456", "London", "Tokyo", "10:00 PM", [11, 45, 0])
print("\nFlight 2 Details:")
print(f"Flight Number: {flight2.flight_number}")
print(f"Origin: {flight2.origin}")
print(f"Destination: {flight2.destination}")
print(f"Departure Time: {flight2.departure_time}")
print(f"Duration: {flight2.get_duration()}")
```

## Proof of work
<img width="max" alt="Screenshot 2024-02-20 at 7 31 56 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/767f9313-d45d-43b6-bdc6-6c6f7a9f3758">


## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/74254bf9-ddaa-4c67-843d-746b28660680)



