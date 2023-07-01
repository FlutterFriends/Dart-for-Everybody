# Regular Expressions

## 

The Treasure Hunt of The Secret Code Society

"Welcome, brave ones, to the Secret Code Society, a mysterious world where each symbol and character holds its own secret power. Regular expressions are our magic spells, weaving characters together to find the hidden treasures amidst the sea of text. So, put on your detective caps, and let's unravel the enigma of Dart's regular expressions."

## The Basics: The Map to the Treasure

```dart
void main() {
  var re = RegExp(r'\b[A-Z]\w*\b');
  print(re.allMatches('In The Secret Code Society, Every Clue Counts').length); // 8
}
```

This, my friends, is the map to your first treasure. Here, `\b[A-Z]\w*\b` is the cryptic instruction set by the society. It translates to "find every word starting with a capital letter". `\b` is the boundary between a word and a non-word, `[A-Z]` is any uppercase letter, and `\w*` is any word character (letter, number, or underscore) appearing zero or more times.

The magic spell, `re.allMatches`, reveals the number of treasures hidden in the sentence. Here, it unearths seven!

## The Number Riddle: Decoding Numerical Clues

```dart
void main() {
  var re = RegExp(r'\d+');
  print(re.hasMatch('Find The 7 Hidden Treasures')); // true
}
```

Here's a number riddle for you! Sometimes, the clues are hidden in the form of numbers. The spell `\d+` means "find one or more digits". It's like the society's secret number detector, sniffing out numerical secrets. `hasMatch` then checks if our riddle, 'Find The 7 Hidden Treasures', indeed contains such a secret. It joyfully returns `true` - yes, a hidden number was found!

## Word Puzzles: The Jigsaw of Characters

```dart
void main() {
  var re = RegExp(r'cl\w*');
  final match = re.firstMatch('In the Secret Code Society, every clue counts')!;
  print(match[0]);
}
```

At times, you'll encounter a jigsaw of characters. Here, `cl\w*` decodes to "find any word starting with 'cl'". It's like having a jigsaw piece and looking for the rest of the puzzle. `firstMatch` then tells us the first word it found to fit this puzzle in our sentence. And lo and behold, it found 'clue'!

## The Laughing Sphinx: Lighter Moments in The Society

Why don't secret agents use regular expressions?

Because they don't like anything that *captures*!

Ah, a little humor to brighten our cryptic journey! Remember, while regular expressions can appear baffling, they're nothing but a fun, coded treasure hunt. Each symbol, each character is part of the magic, forming patterns that unlock the mysteries of text.

So, keep your wits about you, Secret Code Society members, and enjoy this journey of unraveling Dart's regular expressions. Onwards to the next treasure!

Compute scientifically with:

[Numeric Computing](numeric_computing.md)