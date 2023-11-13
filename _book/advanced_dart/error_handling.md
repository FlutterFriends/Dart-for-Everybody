# Error Handling

## **Error Handling: Beyond the Basics**

In our Dart programming journey, we might stumble upon more complicated issues, like difficult and unexpected traps in our treasure hunt. Let's equip ourselves with more advanced error-handling tools!

### **Custom Exceptions**

In Dart, we can create our own custom exceptions to represent specific error conditions. Let's say, for instance, you're trying to open a treasure chest, but it's locked. In the programming world, this could be a "ChestLockedException". Let's see how we could create and use this custom exception:

```dart
class ChestLockedException implements Exception {
  String cause = "The chest is locked!";
}

void main() {
  try {
    throw ChestLockedException();
  } catch(error) {
    print(error.cause); // Will output: The chest is locked!
  }
}
```

Here's what's happening in this code:

1. We define a class **`ChestLockedException`** that implements the **`Exception`** interface. This class has a string field **`cause`** that contains the message "The chest is locked!".
2. In the **`main`** function, we use a **`try-catch`** block to throw and catch this exception. Inside the **`try`** block, we throw a new instance of **`ChestLockedException`**.
3. The **`catch`** block then catches the thrown exception. Since we know that our exception has a **`cause`** field, we can access it using **`error.cause`** and print it out.

So, in plain language: we are simulating a scenario where we're trying to open a locked chest. As we expect, an error occurs (the chest is locked), so we throw a specific **`ChestLockedException`**. We then catch this exception and print out the reason the error occurred (the chest is locked).

### **Stack Traces**

When an error occurs, Dart gives you a stack trace, which is like a breadcrumb trail leading back to the origin of the error. This helps you track down the source of the error and fix it. Here's how you might see it:

```dart
void functionThatThrows() {
  throw Exception('This is an exception');
}

void main() {
  try {
    functionThatThrows();
  } catch(error, stackTrace) {
    print(error);
    print(stackTrace);
  }
}
```

In the code above, `stackTrace` is a StackTrace object that you can print out to see the sequence of method calls leading to the exception.

Here's a hypothetical example of what the **`stackTrace`** could look like:

```bash
Exception: This is an exception
#0      functionThatThrows (...dart_project/main.dart:2:3)
#1      main (...dart_project/main.dart:7:5)
#2      _startIsolate.<anonymous closure> (dart:isolate-patch/isolate_patch.dart:309:32)
#3      _RawReceivePortImpl._handleMessage (dart:isolate-patch/isolate_patch.dart:184:12)
```

The output of the **`stackTrace`** starts with the most recent method call (the source of the exception) and follows the path of execution back to the first method call.

Each line of the **`stackTrace`** typically includes:

- The index of the stack frame (starting with 0),
- The name of the method that was called,
- The path to the file where the method was defined,
- The line number and column where the method was called in that file.

In this case, the **`functionThatThrows`** (which is in your **`main.dart`** file on line 2, column 3) is the first method listed because it's where the exception was thrown. The following line is the **`main`** method (also in your **`main.dart`** file, but on line 7, column 5), which is where **`functionThatThrows`** was called. The last two lines are part of Dart's internal workings and show the steps Dart took to start your program.

This kind of traceback is incredibly useful in debugging because it tells you where the error occurred and how the program got there.

Next:

[Cascade Notion Operator](cascade_notion_operator.md)