# Quiz 051

<img width="max" alt="Screenshot 2024-03-21 at 3 10 10 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/b3c5f25f-f2cc-4e90-b0c8-0a57d8f81e38">

## Code

```py
class Aircraft:
    def __init__(self, model, capacity):
        self.model = model
        self.capacity = capacity

    def get_info(self):
        return f"Aircraft Model: {self.model}\nCapacity: {self.capacity}"

class Flight(Aircraft):
    def __init__(self, flight_number, origin, destination, departure_time, duration, model, capacity):
        super().__init__(model, capacity)
        self.flight_number = flight_number
        self.origin = origin
        self.destination = destination
        self.departure_time = departure_time
        self.duration = duration

    def get_duration(self):
        h, m, s = self.duration
        return f"{h} hours {m} minutes and {s} seconds"

    def get_info(self):
        return (f"Flight Number: {self.flight_number}\n"
                f"Origin: {self.origin}\n"
                f"Destination: {self.destination}\n"
                f"Departure Time: {self.departure_time}\n"
                f"Duration: {self.get_duration()}\n"
                f"{super().get_info()}")

aircraft = Aircraft("Boeing 737", 150)
flight = Flight("AA123", "New York", "Los Angeles", "10:00 AM", [5, 30, 0], "Boeing 737", 150)

print("Aircraft Details:")
print(aircraft.get_info())

print("\nFlight Details:")
print(flight.get_info())

```

## Proof of work
<img width="max" alt="Screenshot 2024-03-21 at 3 19 41 PM" src="https://github.com/hasmhib/unit3-2024/assets/142870448/3f3f982c-2059-479f-a009-cec7e7f7be5a">

## UML Diagram
![image](https://github.com/hasmhib/unit3-2024/assets/142870448/970b3563-add7-42c4-a789-e1c2f2e4d356)


