# Collections

****A Roller Coaster Ride through Lists, Maps, Sets, and Queues****

Buckle up, dear reader! It's time to navigate the looping tracks and dramatic dips of Dart's data structures—Lists, Maps, and Sets. Picture these as thrilling rides in our programming carnival, bringing both order and excitement to our code.

## **Lists: The Ferris Wheel of Dart**

In Dart, a List is like a gigantic Ferris wheel, where each gondola carries a specific value or 'passenger.' Much like how Ferris wheels can carry all sorts of passengers—from the thrill-seekers, the lovebirds, to those just looking to enjoy the view—Dart lists can hold a variety of data types: numbers, strings, booleans, and yes, even other lists!

```dart
var shoppingList = ['eggs', 'milk', 'chocolate'];
var listOfMyMistakes = ['forgot semicolon', 'used = instead of ==', 'infinite loop'];
var listofMistakesIllProbablyMakeAgain = listOfMyMistakes;
var paradoxicalList = ['this sentence is false', 'list of lists not containing themselves'];
```

The Dart list is a programmer's dream-come-true Ferris wheel. No matter how high you want to go, there's a gondola ready to take you there! Each gondola is accessed by an index, starting from **`0`** (yes, we programmers start counting from zero—another charming quirk to add to the 'list of programming eccentricities').

## **Maps: The Treasure Hunt of Dart**

Now, let's move on to another exhilarating ride: Maps. A Map is like an exciting treasure hunt. Each treasure (value) in a Dart map is assigned a unique clue (key). To find the treasure, you simply follow the clue!

```dart
var pirateTreasure = {
  'golden coins': 1000,
  'precious gems': ['ruby', 'emerald', 'sapphire'],
  'mysterious map': 'leads to another adventure'
};
```

In our treasure hunt, **`'golden coins'`** is a clue that leads to a treasure of **`1000`**. Pretty cool, eh? Maps are superb when we want to link values together, just like connecting clues with treasures. Who knew coding could feel so much like a pirate adventure?

## **List and Map Methods: The Bag of Tricks**

While we've introduced Lists and Maps and their superpowers, it's time to take a deep dive into their toolboxes. You see, Lists and Maps in Dart aren't just storage units; they're like that handy multi-tool you take on a camping trip.

Let's consider a list **`shoppingList`** of items you want to buy.

```dart
List<String> shoppingList = ['toothpaste', 'shampoo', 'sponge', 'bananas'];
```

If you suddenly remember that you need bread, instead of creating a new list, you can use the **`add()`** method:

```dart
shoppingList.add('bread');
```

And voila! Your shopping list now includes bread. But let's say you've picked up a bread-making hobby, and you no longer need bread in your list. Simply use **`remove()`**:

```dart
shoppingList.remove('bread');
```

Similarly, Maps aren't just simple old treasure maps. They are more like GPS systems that come with a range of features. Given a map **`favoriteFoods`**:

```dart
Map<String, String> favoriteFoods = {
  'Alice': 'Pizza',
  'Bob': 'Pasta',
};
```

If we find out that Charlie loves Tacos, we don't need a new map. Just use **`putIfAbsent()`**:

```dart
favoriteFoods.putIfAbsent('Charlie', () => 'Tacos');
```

And there you have it! Charlie and his love for Tacos have officially made it to the **`favoriteFoods`** map!

## **Sets: The Unique Snowflakes**

Sets are a lot like the attendees of an exclusive party: no one likes duplicates! A Set is a collection of unique items. Think of it as a box where you put snowflakes. You wouldn't want two identical snowflakes now, would you?

In the following code, **Sets** are like that exclusive VIP lounge. There's no particular order, and no duplicate guests are allowed. Alice won't get in twice, even if she changes her disguise!

```dart
void main() {
  Set<String> vipLounge = {'Alice', 'Bob', 'Charlie', 'Alice'};

  print(vipLounge.length); // 3 party-goers in the VIP!
  print(vipLounge.contains('Alice')); // Alice made it into the VIP? Yes, she did!
  vipLounge.add('Dave'); // Dave's on the list, too!
  print(vipLounge); // Check out who's in the VIP lounge now!
}
```

### Set operations

Sets have some special powers that make them a bit different than other collections.

Imagine we're at a food court area now, and we have two friends, Alice and Bob. Each of them has a set of foods they want to try at the carnival.

Let's explore the union operation, which gives us a set of all unique items in both sets. In the context of our carnival, this will give us all unique food items that either Alice or Bob wants to try.

```dart

void main() {
  // Foods Alice wants to try
  Set<String> aliceFoods = {'Popcorn', 'Cotton Candy', 'Churros'};
  
  // Foods Bob wants to try
  Set<String> bobFoods = {'Hotdog', 'Popcorn', 'Nachos'};

  // Foods that either Alice or Bob wants to try
  Set<String> unionFoods = aliceFoods.union(bobFoods);

  print('Either Alice or Bob wants to try these foods: $unionFoods');
  // Outputs: Either Alice or Bob wants to try these foods: {Popcorn, Cotton Candy, Churros, Hotdog, Nachos}
}
```

As you can see, the **`union`** method returns a new Set that contains all the elements of both the original Sets. In this case, it's all the foods that either Alice or Bob wants to try. Notice how 'Popcorn' only appears once in the union set, despite both Alice and Bob wanting to try it. That's because Sets only contain unique items.

I hope this example gives you a better understanding of the **`union`** operation on Dart Sets. Enjoy your carnival treats!

## Queues

Now, imagine a **`Queue`** as the line for the hot dog stand. In this line, it's a strict "first come, first served" policy. The first one to line up will be the first one to get their hot dog!

```dart
import 'dart:collection';

void main() {
  Queue<int> hotDogLine = Queue();
  
  hotDogLine.addLast(1); // Customer No.1 joins the queue!
  hotDogLine.addLast(2); // Customer No.2 is next!
  hotDogLine.addLast(3); // Customer No.3 takes the last spot!
  
  print(hotDogLine.removeFirst()); // Customer No.1 gets his hot dog!
  print(hotDogLine); // Let's see who's still waiting for their hot dog!
}
```

## **Iterables and Loops: The Theme Park Ride**

Remember the roller coaster ride of loops we discussed earlier? Now, combine that with Lists and Maps, and you have an entire theme park of data to explore. You can loop over Lists and Maps, accessing and manipulating data as you whizz by!

All these tricks and tools make Lists, Maps, and Sets not just containers for storing data but multifunctional devices that can be manipulated and traversed in many ways. After all, programming isn't just about storing values; it's about playing with them!

## **Multi-Dimensional Lists, Sets, and Maps: The Rabbit Holes**

Just like in Alice in Wonderland, things can get much more complex in the world of Lists and Maps. Lists can store other lists, and maps can store other maps. Picture a giant matryoshka doll situation, except it's with data structures.

## **Conclusion**

Just like that, at our Dart Programming Carnival, we ensure a fun and fair time for all! The use of collections like **`List`**, **`Map`**, **`Set`**, and **`Queue`** can provide a structured way to juggle data, akin to juggling colorful juggling balls at this grand carnival!

In the land of Dart, Lists, Maps, and Sets are the kings and queens. They provide a multitude of options to store, access, and manipulate data. They're the powerful allies you want by your side as you embark on your programming journey. So keep practicing, and in no time, you'll become a data structure wizard! Remember, it's all just a bit of hocus-pocus with a dash of data.

A powerful world will be unveiled in:

[Supercharging Your Dart](../Supercharging%20Your%20Dart%20e2a60e83574f475281a6a674e00a93b2.md)