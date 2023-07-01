# Enumerated Types

Enumerated types, also known as enums, are a special type of class in Dart used to represent a fixed number of simple values. Enums are incredibly useful when describing a value that can only take one out of a small set of possible values.

Imagine you're writing a program that deals with the days of the week. Sure, you could represent the days of the week as strings or integers. Still, then you'd constantly have to remember whether "Monday" is represented by "1" or "0", and there's a risk of accidentally assigning "8" to a variable that represents a day. Here's where enums come in.

```dart
enum DaysOfTheWeek {
  Monday,
  Tuesday,
  Wednesday,
  Thursday,
  Friday,
  Saturday,
  Sunday,
}
```

With this enum definition, you can now create variables that can only hold a valid day of the week:

```dart
DaysOfTheWeek today = DaysOfTheWeek.Monday;
```

Dart will prevent you from assigning any other value to **`today`**. This way, we avoid the risk of typo errors and make the code safer and easier to read. Enums improve code clarity and prevent errors by ensuring that variables can only take one of a fixed set of values.

Note that the enum's values (like **`DaysOfTheWeek.Monday`**) are full-fledged objects in their own right, with a **`index`** property that gets automatically assigned based on their position (starting from 0):

```dart
print(DaysOfTheWeek.Monday.index); // Output: 0
print(DaysOfTheWeek.Friday.index); // Output: 4
```

You can also retrieve a list of all the values in an enum using the **`values`** property:

```dart
print(DaysOfTheWeek.values); 
// Output: [DaysOfTheWeek.Monday, DaysOfTheWeek.Tuesday, DaysOfTheWeek.Wednesday, DaysOfTheWeek.Thursday, DaysOfTheWeek.Friday, DaysOfTheWeek.Saturday, DaysOfTheWeek.Sunday]
```

This can be useful for situations where you need to loop over all possible values of an enum.

And that's an introduction to enumerated types in Dart! As you can see, they're a simple yet powerful feature that can make your code safer and easier to understand.

Avoid interstellar surprises with:

[Sound Null Safety](sound_null_safety.md)