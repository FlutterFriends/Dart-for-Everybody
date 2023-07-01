# Flow Control

# **The Flow Control Fiesta**

Ladies and gentlemen, hold on to your keyboards because we're about to embark on a wild, thrilling ride through the Dart programming language's carnival of control flow! Here, we have an amazing array of attractions that help us steer the logic of our programs.

## **Conditional Statements: The Mystical "if-else" Labyrinth**

Imagine stepping into a labyrinth where every turn you take is based on a true-or-false condition. That's our dazzling **`if-else`** maze!

Here's our brave contestant **`weatherIsNice`**, set to either **`true`** or **`false`**.

```dart
bool weatherIsNice = true; // It's a sunny day!
```

Based on this adventurous variable, our contestant will decide which turn to take:

```dart
if (weatherIsNice) {
    print("Let's go for a picnic!"); // If the weather is nice, we're going on a picnic!
} else {
    print("Let's stay home and code."); // If the weather is not nice, more time for coding!
}
```

Just remember, our **`if-else`** labyrinth never leads you astray!

## **Loop-a-Loop Roller Coaster: The Fabulous "for" Loop**

Next, brace yourself for the exhilarating Loop-a-Loop roller coaster, where repetition reigns supreme!

```dart
for (int rideCount = 1; rideCount <= 5; rideCount++) {
    print("This is ride number $rideCount!");
}
```

The **`for`** loop is like a roller coaster ride with three important parts:

- **The Seat Belt Check (`int rideCount = 1`):** This is where we prepare for the ride. We set our **`rideCount`** to 1, indicating we're about to embark on the first ride.
- **The Safety Bar (`rideCount <= 5`):** This is our safety constraint. We continue riding as long as **`rideCount`** is less than or equal to 5. Once we exceed 5 rides, safety regulations dictate that it's time for a break!
- **The Exciting Loop (`rideCount++`):** This is the thrilling part where we go around the loop. After each ride, we increment **`rideCount`** by 1, marking off another exhilarating loop on our ride.

Strap in as you watch **`rideCount`** go from 1 to 5 in the blink of an eye, taking you through the loop each time!

## Waiting in line: the for-in loop

Now, let's step deeper into the magical world of Dart looping and meet **`for-in`**, a spellbinding variation of **`for`** that's more commonly known as **`each`** in other programming lands. The **`for-in`** loop graciously invites every item in a list to a fabulous dance, one at a time.

```dart
var rollerCoasterRiders = ['Anna', 'Bob', 'Charlie'];

for (var rider in rollerCoasterRiders) {
    print('$rider is ready to ride the Loop-a-Loop roller coaster!');
}
```

Our **`for-in`** loop is like a carnival barker, calling each eager roller coaster rider from the **`rollerCoasterRiders`** list to take their turn on the Loop-a-Loop roller coaster. Isn't it just enchanting? Dart certainly knows how to host a spectacular code carnival!

## **The Never-ending Carousel: The Whirling "while" Loop**

Don't forget to take a whirl on our Never-ending Carousel! As long as a condition holds true, you're going for another spin!

```dart
int lollipopCount = 10;
while (lollipopCount > 0) {
    print("Eating a lollipop...");
    lollipopCount--;
}
print("All lollipops are gone. Time for another ride!");
```

Our hero here keeps devouring lollipops until there are none left, making for a delicious and dizzying journey.

## **Do...While Loops: the at-least-once loop**

Just like how some carnival games might keep you hooked until you win a prize, a do-while loop performs a task at least once, and then keeps doing it as long as a certain condition holds true. Let's put this in a Dart context:

```dart
int gamesPlayed = 0;
do {
  print("Playing game number ${gamesPlayed + 1}... Let's win that stuffed unicorn!");
  gamesPlayed++;
} while (gamesPlayed < 5);
```

In this example, **`gamesPlayed`** keeps track of the number of games we've played. We're committed to playing at least one game (gotta win that stuffed unicorn!), so the code inside the **`do`** block executes first. After each game, the **`gamesPlayed`** counter increases. If the number of games is less than 5, we go for another round, if not, we're finally out of the do-while funhouse!

## **Break: The Safety Hatch**

The **`break`** statement is like a shortcut to escape the dizzying rides. If you're riding the carousel and start feeling dizzy, you would want to hop off right away, even if the ride isn't over. Let's check this out with some Dart code:

```dart
for (int carouselRides = 1; carouselRides <= 10; carouselRides++) {
  if (carouselRides > 5) {
    print("Oh no! We've had too much spinning on the carousel. Time to stop.");
    break;
  }
  print("Enjoying carousel ride number: $carouselRides");
}
```

In this example, **`carouselRides`** starts at 1 and, for each loop, we add another ride. But when we've ridden more than 5 times, the world starts spinning a bit too much! This is where the **`break`** statement comes in, allowing us to jump off the carousel right away.

## **Continue: Next Ride Please**

The **`continue`** statement is like skipping a ride you don't like. If you come across a ride that you're not particularly fond of (like that too-scary haunted house), you can skip it and continue to the next one. Here's how we can do that in Dart:

```dart
List<String> carnivalRides = ['Ferris Wheel', 'Carousel', 'Haunted House', 'Roller Coaster', 'Bumper Cars'];

for (var i = 0; i < carnivalRides.length; i++) {
  var currentRide = carnivalRides[i];
  if (currentRide == 'Haunted House') {
    print("Oh, no! The Haunted House is too scary. Let's skip it.");
    continue;  // If Haunted House is encountered, skip to the next iteration
  }
  print("Enjoying the $currentRide!");
}
```

In this example, we're looping through a list of **`carnivalRides`**. When we encounter the 'Haunted House', we decide it's a little too spooky and skip it, moving straight to the next ride.

## **The Magical "Switch" House of Mirrors**

Last but not least, step into the mysterious House of Mirrors where the magical **`switch`** statement takes the center stage. Each mirror reflects a different case, and our reflection hops from one mirror to another based on its value!

```dart
String dartLevel = 'beginner';

switch (dartLevel) {
    case 'beginner':
        print('Welcome, young apprentice! Your journey has just begun.');
        break;
    case 'intermediate':
        print('You have come a long way, young warrior!');
        break;
    case 'expert':
        print('Ah, Master Coder, you have mastered the Dart side of the Force!');
        break;
    default:
        print('Hmm, an unidentified entity you are. Keep practicing Dart, you must.');
}
```

## **Wrap-up**

Well folks, that was a fantastic journey through Dart's Flow Control Fiesta! Each of these attractions, from the **`if-else`** Labyrinth to the **`switch`** House of Mirrors, helps guide the story of our Dart code. So, practice hard, and remember - in the magical world of Dart, you're the ride operator!

Stay tuned for our next fun-filled chapter, and until then, code on amigos and amigas!

Let’s move on to:

[Functions](functions.md)