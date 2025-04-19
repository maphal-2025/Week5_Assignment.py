Question 1
class Cow:
    def __init__(self, name, age, breed, milk_production):
        self.name = name
        self.age = age
        self.breed = breed
        self.__milk_production = milk_production 
    def make_sound(self):
        return f"{self.name} says 'Moo!'"
    def produce_milk(self):
        return f"{self.name} produces {self.__milk_production} liters of milk per day."
class MagicalCow(Cow):
    def __init__(self, name, age, breed, milk_production, magic_power):
        super().__init__(name, age, breed, milk_production)
        self.magic_power = magic_power  
   def make_sound(self):  # Polymorphism
        return f"{self.name} says 'Moo!' with magical echoes!"
    def use_magic(self):
        return f"{self.name} uses its magic power: {self.magic_power}"
cow1 = Cow(name="Bessie", age=5, breed="Holstein", milk_production=25)
magical_cow1 = MagicalCow(name="Moonbeam", age=3, breed="Mystic Holstein", milk_production=30, magic_power="Teleportation")

print(cow1.make_sound()) 
print(cow1.produce_milk())  
print(magical_cow1.make_sound()) 
print(magical_cow1.produce_milk())  
print(magical_cow1.use_magic())  

Question 2

class Vehicle:
    def move(self):
        Vehicle("Car", "Boat", "Plane")

class Car(Vehicle):
    def move(self):
        return "Driving "

class Plane(Vehicle):
    def move(self):
        return "Flying "

class Boat(Vehicle):
    def move(self):
        return "Sailing "

vehicles = [Car(), Plane()class Vehicle:
    def move(self):
        raise NotImplementedError("Subclasses must implement this method!")

class Car(Vehicle):
    def move(self):
        return "Driving "

class Plane(Vehicle):
    def move(self):
        return "Flying "

class Boat(Vehicle):
    def move(self):
        return "Sailing "

vehicles = [Car(), Plane(), Boat()]
for vehicle in vehicles:
    print(vehicle.move())
()]
for vehicle in vehicles:
    print(vehicle.move())



