# Bitwise

### **The Binary Circus: Bitwise Operators**

Ladies and gentlemen, robots and AI, prepare yourselves for a dazzling dive into the digital depths of Dart. A realm where 0s and 1s juggle, tumble, and twist into patterns of pure logic. Welcome to the grand show of Bitwise Operators!

Imagine a grand binary ballet, where each 0 and 1 pirouettes gracefully at the command of these mystical operators. There are six primary dancers in this ballet:

- **`&`** The **Bitwise AND Operator**: It's like the picky eater of the group. This operator looks at the matching bits of two numbers and only takes a bite when both are 1. Otherwise, it starves (returns 0).

```dart
int firstNumber = 170;  // Binary: 10101010
int secondNumber = 240; // Binary: 11110000
int result = firstNumber & secondNumber; // Result: 160 (Binary: 10100000)
```

**`|`** The **Bitwise OR Operator**: The exact opposite of our AND operator, this one's the foodie. If either of the matching bits is 1, it chomps down, satisfied.

```dart
result = firstNumber | secondNumber; // Result: 250 (Binary: 11111010)
```

**`^`** The **Bitwise XOR Operator**: XOR is the rebel - it thrives on difference. It takes a peek at the matching bits, and only when they're different it munches (returns 1).

```dart
result = firstNumber ^ secondNumber; // Result: 90 (Binary: 01011010)
```

**`~`** The **Bitwise NOT Operator**: This is the dramatic one. It takes a binary number and flips all its bits in a grand gesture.

```dart
result = ~firstNumber; // Result: -171 (Binary: 01010101)
```

**`<<`** The **Left Shift Operator**: Imagine a marching band where every time the drum rolls, everyone takes a step to the left. That's what the left shift operator does, but with bits.

```dart
result = firstNumber << 2; // Result: 680 (Binary: 1010100000)
```

**`>>`** The **Right Shift Operator**: As you'd guess, this operator is all about marching to the right. A drumroll, and all bits step right.

```dart
result = firstNumber >> 2; // Result: 42 (Binary: 00101010)
```

With these bitwise operators, you can choreograph your own binary ballets, creating more intricate patterns and magical performances within your Dart code. So, take the stage, and let the binary ballet begin!

Next:

[Comparison](Comparison%204df87e2b33c046afac1928e1a993db2a.md)