# Numeric Computing

# Chapter: Numeric Computing in Dart - The Celestial Harmony

> "As an astronomer, I don't just explore the universe through a telescope. I explore it through numbers. I am the composer of the cosmos, writing symphonies in algorithms and equations."
> 

Welcome, future space explorers! In this chapter, we will journey across the cosmic plains of numeric computing in Dart. With the `dart:math` library as our spaceship, we'll uncover the mysteries of the universe and the harmonic symphony it plays.

## The Basics: Cosmic Constants and Astronomical Arithmetic

```dart
import 'dart:math' as math;

void main() {
  print('Pi: ${math.pi}');
  print('Euler\\'s number: ${math.e}');
  print('Golden ratio: ${(1 + math.sqrt(5)) / 2}');
}
```

Our universe dances to the tunes of some significant constants. Pi, the ratio of a circle's circumference to its diameter, and Euler's number, the base of natural logarithms, are the melodies that govern the elliptical orbits of planets around stars. The golden ratio? It's everywhere, from spiral galaxies to the arrangement of sunflower seeds!

## Spherical Trigonometry: A Harmonious Trio of Sin, Cos, and Tan

```dart
double radianToDegree(double radian) => radian * (180 / math.pi);

void main() {
  double angle = 60; // Let's say the angle is 60 degrees

  double angleInRadians = math.radians(angle); // Convert it to radians

  print('Sin(60): ${math.sin(angleInRadians)}'); // 0.86602540378
  print('Cos(60): ${math.cos(angleInRadians)}'); // 0.5
  print('Tan(60): ${math.tan(angleInRadians)}'); // 1.73205080757
}
```

The universe's orchestra plays in the language of trigonometry. When mapping the night sky or calculating the path of a comet, `sin`, `cos`, and `tan` help us describe the universe's spherical geometry. They're the basis of our cosmic sheet music.

## 3. Celestial Harmonics: Power and Logarithms

```dart
void main() {
  print('2^10: ${math.pow(2, 10)}'); // 1024.0
  print('Log(100): ${math.log(100)}'); // 4.605170185988092
}
```

Ever wonder why star brightness is measured on a logarithmic scale? It's because the energy they produce, seen as light, is enormously varied. By using logarithms, we can make sense of this vast spectrum. As for `pow`, well, it's how we calculate the incredible energies involved when stars go supernova!

## 4. Random Constellations: Dart's Random Class

```dart
void main() {
  var rng = math.Random();
  for (var i = 0; i < 10; i++) {
    print(rng.nextInt(100)); // Generate a random integer between 0 and 99
  }
}
```

Just like how we discover unexpected patterns in the night sky, Dart's `Random` class adds an element of surprise to our code. Remember, while the universe might seem chaotic, there's always an underlying pattern or principle — a hidden harmony.

## For all humanity

Whether you're calculating the gravitational interaction of galaxies or plotting the lifecycle of a star, Dart's numeric computing capabilities and the `dart:math` library are like your scientific calculators. Just remember, every time you crunch a number, you're playing a note in the grand symphony of the universe. So, don't just code. Compose! Create your cosmic concerto with Dart and uncover the hidden harmonies in the cosmos.

Remember to keep your workspace clean by:

[Organizing Your Code](numeric_computing.md)