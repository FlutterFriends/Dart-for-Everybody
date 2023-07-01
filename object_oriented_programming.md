# Object-Oriented Programming

****Dart of Justice - The League of OOP Superheroes****

In our journey through the programming universe, we've met many characters - from loops to conditionals, from data structures to functions. Now, it's time to meet the League of Superheroes - the Object-Oriented Programming (OOP) team.

### **What is OOP?**

Picture this: an Avengers movie, but instead of heroes like Thor, Black Widow, or Black Panther, you have... wait for it... Classes and Objects. They are our real superheroes, the true Avengers in the programming universe!

OOP is a paradigm where everything revolves around Classes and Objects, just like a comic book centers around its superheroes and their mighty exploits. It allows us to encapsulate data (properties of superheroes, perhaps?) and methods (their superpowers, obviously) into reusable and interactive packages known as classes. Sounds exciting, right? Let's dive in.

### **Classes and Objects**

Imagine a superhero template, a blueprint, if you will, where you just fill in the characteristics and powers and voila, you have your hero. That's exactly what a **class** is - a blueprint from which objects are created.

```dart
class Superhero {
  String name;
  String power;

  Superhero(this.name, this.power);
}
```

The real superheroes are **objects**, instances of the class. For example, Spiderman is an instance of the **`Superhero`** class.

```dart
var spiderman = Superhero('Spiderman', 'Web-slinging');
```

### **Constructors, and the `this` keyword**

When a superhero is born (or, ahem, created), they come with their own unique characteristics. This happens in our class via a **constructor** - a special method that brings our object to life.

In Dart, constructors share the same name as the class and use the **`this`** keyword to refer to the current instance of the class. **`this`** is like our superhero pointing to their own chest saying, "Hey, this is me!"

```dart
class Superhero {
  String name;
  String power;

  Superhero(this.name, this.power);
}
```

### **Getters and Setters**

Think of getters and setters as the superhero's PR team. They control how the public gets information about the hero (getter) and how they can change it (setter). If a setter isn't set, no one can change the information. For instance, no one but Peter Parker can change the fact that he is Spiderman!

```dart
class Superhero {
  String name;
  String power;

  Superhero(this.name, this.power);

  String get identity => name;
  set identity(String identity) {
    name = identity;
  }
}
```

### **Inheritance and the `super` keyword**

Just like how superheroes sometimes pass on their mantle to successors (think Batman -> Robin), classes can inherit properties and methods from other classes. The class being inherited from is the superclass, and the inheriting class is the subclass. The **`super`** keyword is used to refer to the superclass.

```dart
class Speedster extends Superhero {
  int speed;
  
  Speedster(String name, this.speed) : super(name, 'Super Speed');
}
```

### **Polymorphism**

In a superhero team-up, each hero uses their powers in their own unique way, right? This is exactly what polymorphism is. The same method behaves differently in different classes. We call this method overriding.

```dart
class Speedster extends Superhero {
  //...
  void showPower() {
    print('$name runs at $speed mph!');
  }
}
```

### **Composition**

Composition is like our superhero stepping into a high-tech chamber, with various traits and abilities available at the touch of a button. Each trait is represented by a different class, and our superhero can pick and choose the ones they want to embody. From super hearing to chameleon camouflage, each super-trait becomes part of the hero's whole toolkit. Let's see it in action:

```dart
class SuperSpeed {
  void runFast() {
    print('Running at lightning speed!');
  }
}

class SuperStrength {
  void liftHeavy() {
    print('Lifting a mountain, no big deal!');
  }
}

class SuperSneeze {
  void superSneeze() {
    print('A-choo! There goes the neighborhood...');
  }
}

class CustomHero {
  SuperSpeed speed;
  SuperStrength strength;
  SuperSneeze sneeze;

  CustomHero(this.speed, this.strength, this.sneeze);
  
  void showOff() {
    speed.runFast();
    strength.liftHeavy();
    sneeze.superSneeze();
  }
}

var myHero = CustomHero(SuperSpeed(), SuperStrength(), SuperSneeze());
myHero.showOff();
```

In the world of OOP, composition lets us make our code more dynamic, just like our custom superhero who can now run faster than a cheetah, lift heavier than a Hercules, and... sneeze harder than a gale-force wind? Well, we never said all superpowers had to be serious!

## Design patterns

**The Superpowers of our League**

---

Design patterns are just like the special abilities of our superheroes - tried and true techniques that come in handy when faced with recurring coding challenges. They are templates or blueprints that can be reused in many different situations. Let's take a look at a few.

### **Singleton: The Immortal One**

This pattern restricts a class from instantiating multiple objects. There's only one instance of this class across your application, much like there's only one Immortal One!

```
class Singleton {
  static final Singleton _singleton = Singleton._internal();

  factory Singleton() {
    return _singleton;
  }

  Singleton._internal();
}

void main() {
  var s1 = Singleton();
  var s2 = Singleton();

  print(identical(s1, s2));  // prints: true
}

```

Here, the `Singleton` class has a private constructor, which means no other class can instantiate it. When we call `Singleton()`, we get the same instance every time, thus ensuring the immortality of the singleton object.

### **Factory: The Shapeshifter**

Factory pattern is about creating objects without specifying the exact class of object that will be created, just like the Shapeshifter can morph into anything!

```
abstract class Shape {
  void draw();
}

class Circle implements Shape {
  void draw() {
    print('Drawing a circle');
  }
}

class Square implements Shape {
  void draw() {
    print('Drawing a square');
  }
}

Shape shapeFactory(String type) {
  if (type == 'circle') return Circle();
  if (type == 'square') return Square();
  throw 'Can\\'t create $type';
}

void main() {
  var circle = shapeFactory('circle');
  circle.draw(); // prints: Drawing a circle

  var square = shapeFactory('square');
  square.draw(); // prints: Drawing a square
}

```

Here, `shapeFactory` returns a `Shape` object but the actual type is hidden from the client, allowing the Shapeshifter to transform into a `Circle` or `Square`.

### **Observer: The Mind Reader**

This pattern allows an object (the observer) to watch another object (the subject), and be notified when the subject changes state. Just like the Mind Reader is always in the know!

```
class Subject {
  List<Observer> observers = [];

  void addObserver(Observer observer) {
    observers.add(observer);
  }

  void notify(String message) {
    for(var observer in observers) {
      observer.update(message);
    }
  }
}

class Observer {
  void update(String message) {
    print('Received: $message');
  }
}

void main() {
  var subject = Subject();
  var observer1 = Observer();
  var observer2 = Observer();

  subject.addObserver(observer1);
  subject.addObserver(observer2);

  subject.notify('Something happened!');
}

```

Here, `Observer` classes get notified when the `Subject` calls `notify()`, keeping them up to date with the latest happenings. That's Mind Reader for you!

With these design patterns in your superhero toolkit, you're ready to face even the most villainous coding challenges head-on. Remember, with great power comes great responsibility, so use them wisely!

## Mixins

While we covered composition briefly in our chapter on object-oriented programming, there is a more conventional way of mixing and matching new combinations of code called Mixins.

Mixins are a way of reusing a class's code in multiple class hierarchies. Think of it as a magical tome of spells that any wizard can use, regardless of their school of magic. Here's an example:

```dart
mixin Agility {
  void dodge() {
    print("Dodged the attack!");
  }
}

class Player {
  void attack() {
    print("Attack!");
  }
}

class Rogue extends Player with Agility { }

void main() {
  var rogue = Rogue();
  rogue.attack();
  rogue.dodge();
}
```

In this code, the **`Rogue`** class has all the methods of the **`Player`** class and also the **`Agility`** mixin.

## Generics

Generics are a way of writing flexible, reusable code that works with different data types. They're like a magical key that can open any lock in our game! Here's a simple example:

```dart
class TreasureBox<T> {
  T content;

  TreasureBox(this.content);

  void open() {
    print("You've found $content!");
  }
}

void main() {
  var goldBox = TreasureBox<int>(500);
  goldBox.open(); // You've found 500!

  var gemBox = TreasureBox<String>('a rare gem');
  gemBox.open(); // You've found a rare gem!
}
```

In this example, **`TreasureBox`** is a generic class that can contain any type of content. **`T`** is a placeholder that you replace with the actual type when you create an instance of **`TreasureBox`**.

These are some of the advanced topics in Dart. Each of these topics can be a chapter in itself. Understanding these advanced features of Dart can make your code more robust, flexible, and efficient. As you continue your journey into Dart programming, be sure to explore each of these topics in more depth!

## **Let's wrap this up!**

So, just like how every superhero adds value to the Avengers, every concept in OOP is crucial in programming. And remember, with great coding power comes great bug-fixing responsibility! Next up, we'll be exploring the cosmic realms of Asynchronous Programming. Stay tuned!

Now, let’s extend your superpowers with some:

[Advanced Dart](advanced_dart.md)