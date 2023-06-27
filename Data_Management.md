# Data Management

**Data Management and File Operations: The Life of a Data Detective**

We are on a mission. A mission to solve the mystery of data, but we don't just need detectives, we need Data Detectives. So dust off your magnifying glasses, slip into your trench coats, and let's solve this data mystery with Dart!

### **File I/O Basics**

First things first, in the real world, detectives deal with evidence - and in Dart, our evidence comes in the form of data. Usually, this data is stored in files. Unfortunately, DartPad doesn't support direct File I/O due to its web-based nature, but if you were running Dart on your local machine, here's a peek at how it would look.

```dart
import 'dart:io';

void main() {
  var file = File('evidence.txt');

  if (file.existsSync()) {
    print('We found the evidence!');
    var contents = file.readAsStringSync();
    print('The evidence says... $contents');
  } else {
    print('The evidence is missing!');
  }
}
```

*Note: DartPad doesn't support direct File I/O operations. The above code is just to give you an idea of how it works.*

### **Dealing with Different Data Formats**

Now that we've found our evidence, it's time to decode it. Evidence (or data) can be encoded in several formats such as plain text, CSV, JSON, or XML. Luckily for us, Dart has built-in support for JSON!

```dart
import 'dart:convert';

void main() {
  var jsonString = '{"name": "Alice", "age": 25}';
  
  Map<String, dynamic> user = jsonDecode(jsonString);
  
  print('Name: ${user['name']}');
  print('Age: ${user['age']}');
}
```

Let's say we got our evidence, and it was in JSON format. Easy-peasy, right? We just used Dart's **`jsonDecode`** method to convert the JSON string into a Dart Map. Similarly, you can use **`jsonEncode`** to convert a Dart object into a JSON string.

### **Simple In-Memory Database**

With more complex cases, a simple file might not be enough to hold all the evidence. We might need a database! Let's build a simple in-memory database.

```dart
class Record {
  String id;
  String data;
  
  Record(this.id, this.data);
}

class InMemoryDatabase {
  List<Record> _records = [];
  
  void insert(Record record) {
    _records.add(record);
  }
  
  Record find(String id) {
    return _records.firstWhere((record) => record.id == id);
  }
  
  void update(String id, String newData) {
    var record = find(id);
    if (record != null) {
      record.data = newData;
    }
  }
}

```

Here, we have a simple **`InMemoryDatabase`** that can store **`Record`** objects. We can **`insert`** new records, **`find`** a record by its id, and **`update`** the data of a record.

### **Error Handling**

As detectives, we have to be prepared for all sorts of contingencies. In the world of programming, that means handling errors.

```dart
void main() {
  var jsonString = '{"name": "Alice", "age": 25}';
  
  try {
    Map<String, dynamic> user = jsonDecode(jsonString);
    print('Name: ${user['name']}');
    print('Age: ${user['age']}');
  } catch (e) {
    print('Something went wrong: $e');
  }
}
```

Here, we've used a **`try-catch`** block to handle any potential errors that might occur when we try to decode a JSON string.

## Mystery solved!

That's it for now, my fellow detectives! With your new data management and file operation skills, you're well on your way to becoming a master Data Detective! Next, we'll tackle the mysteries of interacting with real-world latency. So keep your watch close at hand!

Next, see the big picture by

[Exploring Dart’s Ecosystem](Exploring%20Dart%E2%80%99s%20Ecosystem%205780f66528b34ded9f4521f1519bc21a.md)