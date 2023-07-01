# Extension Methods

Alright, let's spin this with a dance party theme! Extension methods are like adding new dance moves and expression to your repertoire - you're expanding your abilities, and adding a spark to the dance floor.

```
extension on String {
  String addSomeEnthusiasm() => toUpperCase() + '!!!';
}

void main() {
  print('let us dance'.addSomeEnthusiasm()); // LET US DANCE!!!
}

```

In the above code, we're busting out a new move, **`addSomeEnthusiasm`**, on the **`String`** class. Now, every string can add enthusiasm to the dance floor by converting the string to upper case and adding three exclamation marks - making your statements loud, proud, and dance-ready!

Think of extension methods as learning a new dance style to spice up your routine. You're not changing the fundamental steps - walking is still walking, and a String is still a String - but you're adding some flair to your execution. So get ready to shake things up and make the code dance to your rhythm with extension methods!

Allow specific values with:

[Enumerated Types](extension_methods.md)