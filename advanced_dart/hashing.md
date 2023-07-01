# Hashing

# Chapter: The Magic Bakery: An Adventure in Hashing with Dart

"Step into the magic bakery of Dart, where each sumptuous treat is more unique than the last, just like our hashing concept. What's that? You've never heard of 'hashing' in a bakery? Oh, my friend, you're in for a delightful surprise! Welcome to the world where computer science meets the irresistible aroma of baked goodies!"

## 1. What is Hashing?

Imagine you walk into a bakery filled with mouthwatering pastries. But here's the thing - each pastry is one of a kind. How do we distinguish them all? Easy! The magic baker uses a special technique: each pastry is sprinkled with a unique mix of magic sugar that assigns a unique number, known as a 'hash code'. Just like our pastries, objects in Dart can have their own hash code too.

```dart
void main() {
  var cupcake = 'Strawberry Cupcake';
  print(cupcake.hashCode);  // Outputs a unique number, the hash code of 'Strawberry Cupcake'
}
```

Here, `hashCode` is like our magic sugar sprinkler, creating a unique hash code for the `Strawberry Cupcake`.

## 2. Why is Hashing Important?

Back in our bakery, imagine you have hundreds of unique pastries. You need to find a specific one - a delectable `Lemon Tart`. How would you find it amongst all these treats without tasting each one? The answer is the magic sugar, or hash code! It helps to quickly find and identify our `Lemon Tart`. Similarly, in programming, hashing helps us locate and access data swiftly and efficiently.

```dart
void main() {
  var magicBakery = { 'Strawberry Cupcake'.hashCode : 'Strawberry Cupcake', 'Lemon Tart'.hashCode : 'Lemon Tart' };
  var desiredTreatHashCode = 'Lemon Tart'.hashCode;
  print(magicBakery[desiredTreatHashCode]); // Outputs 'Lemon Tart'
}
```

In the code above, `magicBakery` is our Dart map, acting as the bakery catalogue. Each pastry is associated with its unique hash code. To find the `Lemon Tart`, we just look for its hash code!

## 3. Collision Course - When Two Treats Share the Same Magic Sugar

In a perfect bakery, each treat would have its own unique magic sugar. But sometimes, two treats end up with the same hash code - we call this a 'collision'. Fear not! Our wise baker always has a solution. He simply adds a tiny detail to the magic sugar mixture to make it unique again!

```dart
class Pastry {
  String name;
  String flavor;

  // Constructor
  Pastry(this.name, this.flavor);

  // Custom hashcode
  @override
  int get hashCode => name.hashCode ^ flavor.hashCode;
}
```

In this code, our `Pastry` class represents a unique pastry. In the rare case of a collision, we define a custom hash code. It combines the hash codes of `name` and `flavor` using the bitwise XOR operator (^), ensuring our hash code stays unique.

Ah, the magical world of hashing in Dart! A delightful blend of uniqueness and efficiency, much like our magical bakery. Remember, just as every delicious pastry can be found by its magic sugar, so too can every object be efficiently accessed by its hash code. Happy baking, my friend!

Define and identify new structures with:

[Records, Patterns, and Pattern Matching](records_patterns_and_pattern_matching.md)