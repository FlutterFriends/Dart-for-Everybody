# Functions

## **The Fabulous World of Functions**

Once upon a time, in the enchanted land of Dart, there existed a magical guild known as "Functions." This extraordinary league of spells was capable of performing marvelous feats, often transforming inputs into outputs in the blink of an eye!

### **Meet the Functions**

Let's imagine functions as friendly magical creatures with various abilities. You call them by name, give them a task (your inputs), and *poof!* they work their magic, bringing you back a result (your output). For example, there could be a creature named **`sum`**, and if you ask **`sum`** to add 2 and 3, it'll return 5 with a twinkle in its eye. The code for such a function would look like this:

```dart
int sum(int a, int b) {
  return a + b;
}
```

Here, **`sum`** is the name of the function, **`int a`** and **`int b`** are the parameters (the tasks), and **`a + b`** is the magical result. The **`int`** in front of **`sum`** tells us that our magical creature always brings back an integer as a result. Remember, types are important in Dart!

### **A Function of Many Hats**

Sometimes, a function may take on different roles depending on the task it is given. In Dart, these are known as optional and named parameters. Picture a magical creature who can juggle, dance, and sing — but it only performs the tasks you specifically ask for. Check this out:

```dart
String introduce(String name, {String talent = 'nothing'}) {
  return '$name can do $talent';
}
```

If you only tell this function your name, it will assume you can do nothing (how rude!). However, if you specify your talent, it'll sing your praises!

### **Anonymous Functions: The Unknown Hero**

In the Dart magical universe, there are anonymous functions too. They're like the masked superheroes of the coding world - no names, just action! You'll often find them sneaking around in the world of higher-order functions (more on that later) or fluttering about in the Flutter framework, bringing life to buttons and various interactive elements. Here's how our anonymous hero might look:

```dart
var anonymousHero = (task) => 'Completing $task at lightning speed!';
```

### **Recursive Functions: The Magic Mirror**

In the hall of magic mirrors, a special kind of spell echoes endlessly. These are the recursive functions — functions that call themselves in their own definition. It's a bit like a magical creature casting a spell to clone itself, then the clone casting the same spell, and so on, until a certain condition is met. Here's an example:

```dart
int factorial(int n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
}
```

It calculates the factorial of a number (n!) by continually multiplying **`n`** by the factorial of **`n - 1`**, until **`n`** is 1.

### **Higher-Order Functions: The Superstars**

Lastly, we have the superstars of the function world: higher-order functions. These are functions that have learned to tame other functions. They can take other functions as gifts (parameters), or they can spawn new functions to do their bidding (return a function).

```dart
Function makeAdder(int addBy) {
  return (int i) => addBy + i;
}
```

his function creates a new function that can add any number to **`addBy`**.

So, there you have it! In the enchanted land of Dart, functions aren't just ordinary lines of code. They are magical creatures, full of wonder and whimsy, ready to transform inputs into outputs, work magic anonymously, echo in eternity, and even control other functions. As you continue your journey, these magical creatures will be your most loyal companions, always ready to perform feats of code at your behest!

Next up, we'll be delving into the realm of Dart's mythical beasts: the data structures. Stay tuned, brave adventurer!

Let’s learn about:

[Working With Data](../working_with_data.md)