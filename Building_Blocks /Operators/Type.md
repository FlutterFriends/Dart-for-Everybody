# Type

### **All Aboard the Type Test Express: `is` and `is!`**

Buckle up, coding comrades! We're about to embark on a thrilling journey aboard the Type Test Express, the one-stop solution to avoid the pitfalls of type confusion. Dart's type test operators are like the friendly conductors checking tickets, making sure everyone (or in our case, every variable) is in the right place.

There are two conductors in our train analogy, **`is`** and **`is!`**, and they handle our passengers - variables - with care and precision.

- **`is`** The **Identity Inspector**: This operator, like an attentive conductor, checks if a variable is of a certain type. If it is, it responds with a courteous nod (returns **`true`**). But if it's not, it shakes its head (returns **`false`**).

```dart
var aTrainTicket = 'Choo Choo!';
print(aTrainTicket is String); // True! This ticket is indeed a string.
```

**`is!`** The **Non-Identity Inspector**: This operator has an edgier approach. Instead of checking if a variable is of a certain type, it checks if it is not of a certain type. If the variable's type does not match, it gives a triumphant thumbs-up (**`true`**). But if it does match, it frowns in disappointment (**`false`**).

```dart
print(aTrainTicket is! int); // True! Our ticket is no integer, it's a string!
```

These conductors, **`is`** and **`is!`**, are here to keep our code on track, making sure that all variables are precisely what we expect them to be. Just remember, when in doubt, give a shout out to **`is`** and **`is!`**.

So, as we pull into our next station, the Land of Control Flow, remember to keep your variables in check and your types in order! Happy coding!

Onward to the next section of the book:

[Documentation](https://www.notion.so/Documentation-d1c06680c20f4ccfa963cd5ed96c447e)
