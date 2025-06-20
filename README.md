### OPPS CONCEPTS
   ##### CLASS
     
Today we write the code for class 

##### code 1

    class Dog:
    species = "Canine" 

    def __init__(self, name, age):
        self.name = name  
        self.age = age  

    dog1 = Dog("Buddy", 3)
    print(dog1.name) 
    print(dog1.species)
##### output

    Buddy
    Canine

##### code 2

    class Dog:
    species = "Canine"  

    def __init__(self, name, age):
        self.name = name  
        self.age = age  

    dog1 = Dog("Buddy", 3) 
    dog2 = Dog("Charlie", 5) 

    print(dog1.name, dog1.age, dog1.species) 
    print(dog2.name, dog2.age, dog2.species) 
    print(Dog.species)

    print(dog1.species)

##### output
    Buddy 3 Canine
    Charlie 5 Canine
    Canine
    Canine

##### Attributes and Methods:

code for Attributes and Methods:

##### code 1
    class animal:
    no_of_legs = 4
    food = "meat"
    def run(self):
        print("Running fast")
    def slowrun(self):
        print("Running slow")

    animal1= animal()

    animal1.no_of_legs=2
    animal1.food="grass"
    print(animal1.no_of_legs)
    print(animal1.food)

    animal2=animal()

    animal2.no_of_legs=6
    animal2.food="fish"
    print(animal2.no_of_legs)
    print(animal2.food)
##### output
    2
    grass
    6
    fish

##### code 2
    class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def eat(self):
        print(f"{self.name} is eating.")

    def make_sound(self):
        print(f"{self.name} makes a sound.")  

    my_animal = Animal("jack", "Dog")
    print(my_animal.name)
    my_animal.eat()
    my_animal.make_sound()
##### output
    jack
    jack is eating.
    jack makes a sound.

##### Inheritance
##### code
    class Animal:
    def __init__(self, name, species):
        self.name = name
        self.species = species

    def eat(self):
        print(f"{self.name} is eating.")

    def make_sound(self):
        print(f"{self.name} makes a sound.")
class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name, "Dog")
        self.breed = breed

    def bark(self):
        print(f"{self.name} barks.")            
    class Cat(Animal):
        def __init__(self, name, color):
            super().__init__(name, "Cat")
            self.color = color

        def meow(self):
            print(f"{self.name} meows.")            
    class Bird(Animal):
        def __init__(self, name, species):
            super().__init__(name, species)

        def fly(self):
            print(f"{self.name} is flying.")

    my_Dog = Dog("sam", "Golden Retriever")
    print(my_Dog.name, my_Dog.species, my_Dog.breed)
    my_Dog.eat()

    my_cat = Cat("pinky", "Tabby")
    print(my_cat.name, my_cat.species, my_cat.color)
    my_cat.eat()

    my_bird = Bird("leo", "Canary")
    print(my_bird.name, my_bird.species)
    my_bird.fly()

##### output
    sam Dog Golden Retriever
    sam is eating.
    pinky Cat Tabby
    pinky is eating.
    leo Canary
    leo is flying.