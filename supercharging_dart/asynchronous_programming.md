# Asynchronous Programming

## **Sip, Savor, and Async - Asynchronous Programming in Dart**

Welcome to our next exciting chapter. Remember the last time you and your friends decided to hit your favorite café? You walked into the smell of freshly ground coffee beans, the sound of the espresso machine, and an overwhelming choice of tempting treats.

Programming, my dear friend, is no different than this café. Just like you've got multiple things going on, from ordering your food to catching up with your friends, a computer program often needs to do several things at once. So, let's get caffeinated and dive right into the world of synchronous and asynchronous programming!

### **Synchronous vs Asynchronous Programming**

Imagine this scenario. You and your friends step into the café. You approach the counter to order. "One cappuccino, please," you say. The barista starts preparing your coffee right away. But until your coffee is ready, nobody else can order. Your friends have to wait until your coffee is done. Sounds pretty annoying, right? Well, this, my friends, is an example of synchronous programming.

In contrast, asynchronous programming would go a little like this: You place your order, the barista nods, and then you step aside. Your friends can place their orders too. The barista works on the orders as they came in. Everybody gets a buzzer that will notify them when their order is ready. In the meantime, you're all free to find a seat, chat, or scroll through your social media. Much better, isn't it?

### **Futures**

In Dart, the concept of a "future" is central to understanding async programming. In our café analogy, a future is like your buzzer. When you place an order, you're handed a buzzer. This buzzer is a promise that your order will be ready at some point in the future.

In Dart, when we have an operation that might take a while to complete (like querying a database, downloading a file, or in this case, preparing a delicious cappuccino), we represent this operation as a **`Future`**. When the **`Future`** completes, it'll either hold the result of the operation or an error, in case something went wrong.

```jsx
Future<String> makeCoffee(String order) async {
    var coffee = await barista.prepareCoffee(order);
    return 'Your $coffee is ready!';
}
```

### **Async and Await**

The **`async`** and **`await`** keywords are the superheroes of Dart's asynchronous programming. You can think of them as the digital version of your buzzer and you waiting for your coffee.

```jsx
void main() async {
    print('Placing order for cappuccino...');
    var coffee = await makeCoffee('cappuccino');
    print(coffee);
}
```

The **`async`** keyword tells Dart that some asynchronous operations are happening within that function, and **`await`** tells Dart to wait for a **`Future`** to complete and extract its value.

### **Error handling in Async programming**

Sometimes, things don't go according to plan. Maybe the café ran out of your favorite cinnamon rolls, or perhaps the barista accidentally spilled your coffee. When things go awry in asynchronous programming, you need to handle these errors gracefully.

```jsx
Future<String> makeCoffee(String order) async {
    try {
        var coffee = await barista.prepareCoffee(order);
        return 'Your $coffee is ready!';
    } catch (error) {
        throw 'Oh no, there was a problem making your $order!';
    }
}
```

### **Streams**

Lastly, let's talk about streams. Imagine you're sitting at your table, and you see your barista making drinks one after another, each one a different order. In Dart, a stream is a way to receive a sequence of events, one after another. You can think of it as having a front-row seat to watching the barista in action, with each completed order being an event in the stream.

```dart
class Order {
    String personName;
    String drinkName;
    Duration preparationTime;

    Order(this.name, this.drinkName, this.preparationTime);
}

class Barista {
    Future<Order> makeOrder(Order order) async {
        print('Preparing {$order.drinkName} for ${order.personName}...');
        await Future.delayed(order.preparationTime);
				print('Order is prepared.');
        return order;
    }
}

Stream<Order> baristaMakingOrders(Barista barista, List<Order> orders) async* {
    for (var order in orders) {
        yield await barista.makeOrder(order);
    }
}

void main() {
    var barista = Barista();
    var orders = [
        Order('Alice', 'Latte', Duration(minutes: 2)),
        Order('Bob', 'Mocaccino', Duration(minutes: 3)),
        Order('Charlie', 'Espresso', Duration(minutes: 1)),
    ];

    var subscription = baristaMakingOrders(barista, orders).listen(
        (Order order) {
            print('${order.beverageName} is ready for ${order.personName}');
        },
        onError: (err) {
            print('Oh no, there was a problem: $err');
        },
        onDone: () {
            print('The barista has finished all the orders!');
        }
    );
}
```

The code above models a café scenario where a barista is preparing drinks for a series of orders. It leverages Dart's asynchronous programming capabilities to simulate the process of making a drink, which takes a certain amount of time. This process is modeled using a **`Future`**, and the sequence of drink orders is represented as a **`Stream`**. Here is a more detailed breakdown of the different parts of this code:

**The `Order` class**: This class represents an order placed by a person in the café. Each **`Order`** object has a **`personName`** (the name of the person who placed the order), a **`drinkName`** (the type of drink ordered), and a **`preparationTime`** (the amount of time it takes to prepare the drink).

**The `Barista` class**: This class represents the barista who is preparing the drinks. The **`Barista`** class has a single method, **`makeOrder`**, which takes an **`Order`** as input. This method returns a **`Future<Order>`**, simulating the asynchronous process of making a drink. The **`makeOrder`** method first prints a message saying it's preparing the drink, then "waits" for a duration equal to the order's preparation time using the **`Future.delayed`** function. After the delay, it prints a message saying the order is prepared and returns the **`Order`**.

**The `baristaMakingOrders` function**: This is an asynchronous generator function that takes a **`Barista`** and a **`List<Order>`** as input. For each **`Order`** in the list, it waits for the **`Barista`** to finish making the order, then yields the **`Order`**. Because it uses the **`yield`** keyword, this function returns a **`Stream<Order>`**, which emits each completed order as soon as it's ready.

**The `main` function**: This function sets up the scenario and runs the simulation. It first creates a **`Barista`** and a list of **`Order`**s. Then, it calls the **`baristaMakingOrders`** function and subscribes to the resulting **`Stream<Order>`**. The **`listen`** method is called on the **`Stream`** to handle the **`Order`** events it emits. This function takes three arguments:

- A callback function that gets called whenever a new **`Order`** is ready. This function simply prints a message saying the drink is ready for the person who ordered it.
- An **`onError`** callback that gets called if there's an error while preparing an order. This function prints an error message.
- An **`onDone`** callback that gets called when all orders have been completed. This function prints a message saying the barista has finished all the orders.

This code provides a practical and relatable demonstration of asynchronous programming in Dart, showing how **`Future`**s and **`Stream`**s can be used to manage time-consuming tasks and sequences of events.

Wow! We’ve covered the foundations. Let’s take a quick look at:

[Regular Expressions](Regular%20Expressions%20dcb63c3bfa4f4090847458dbdfc6731e.md)