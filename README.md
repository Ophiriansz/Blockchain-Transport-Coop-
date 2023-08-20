# urban-trece
Urban trece transport cooperative my 1st project
class TransportService:
    def __init__(self, name, capacity):
        self.name = name
        self.capacity = capacity
        self.passengers = []

    def add_passenger(self, passenger_name):
        if len(self.passengers) < self.capacity:
            self.passengers.append(passenger_name)
            print(f"{passenger_name} has been added to {self.name}.")
        else:
            print(f"{self.name} is full. {passenger_name} cannot be added.")

    def list_passengers(self):
        print(f"Passengers in {self.name}:")
        for passenger in self.passengers:
            print(passenger)

    def remove_passenger(self, passenger_name):
        if passenger_name in self.passengers:
            self.passengers.remove(passenger_name)
            print(f"{passenger_name} has been removed from {self.name}.")
        else:
            print(f"{passenger_name} is not in {self.name}.")

# Example usage:
bus = TransportService("Bus", 50)
bus.add_passenger("Alice")
bus.add_passenger("Bob")
bus.list_passengers()
bus.remove_passenger("Carol")
bus.list_passengers()
