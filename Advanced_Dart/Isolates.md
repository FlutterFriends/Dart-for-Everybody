# Isolates

In the realm of Dart, each bit of code resides within an 'Isolate', an entity that is, quite aptly, isolated from all others. These Isolates don't share memory. It's as if each one is a different planet in our Dart galaxy, each having its own atmosphere (memory) and life-forms (code).

```dart
void broadcastMessage(String message) {
  print(message);
}

void main() {
  Isolate.spawn(broadcastMessage, 'Greetings from Planet Dart!');
}
```

In the stellar code above, **`Isolate.spawn`** forms a new planet (creates a new isolate) and broadcasts the **`broadcastMessage`** signal from that planet (runs the function in that isolate). The second argument to **`Isolate.spawn`** is the interstellar message transmitted to the new planet (isolate).

Think of it this way: You're creating a new planet and then broadcasting an interstellar message: 'Greetings from Planet Dart!'.

And the cool part? Each planet (isolate) exists in its own corner of the galaxy, unaffected by any cosmic disasters (errors) that might befall its neighbors. Isn't it fascinating? Welcome to the cosmic journey of Dart Isolates!

Be more meta with: 

[Metaprogramming](Metaprogramming%20e0de45742b34402cb3af6bf2a610827c.md)