# Testing your Dart Code

## Introduction to Testing

Imagine, if you will, that you're not just a junior software engineer at a prestigious space agency, but you've become the custodian of the code that keeps an actual spaceship flying. Now that's a lot of responsibility resting on your shoulders! Remember, in space, no one can hear you scream, "I should have tested my code!"

### The Importance of Testing

Testing your code is like the pre-flight checks performed before a rocket launch. You wouldn't want to discover a critical failure after the launch, would you? That would be a quick ticket to Unemploymentville rather than to Mars!

### Types of Testing

We have different types of testing like unit testing, integration testing, and system testing. Think of them as checking the spaceship's engines, making sure the crew's life support systems work together, and finally testing the whole spaceship.

## Unit Testing

### Introduction to Unit Testing

Unit tests are the nuts and bolts of your spaceship, the individual parts you check before putting everything together. It's like testing a single thruster before attaching it to the spaceship.

### Anatomy of a Unit Test

A unit test usually has three parts: Arrange, Act, Assert. It's like preparing your space helmet (Arrange), putting it on (Act), and checking if the oxygen flows correctly (Assert).

```
void main() {
  // Arrange
  var helmet = SpaceHelmet();

  // Act
  helmet.putOn();

  // Assert
  expect(helmet.oxygenFlow, isTrue);
}

```

### Writing Your First Unit Test

Our first unit test will be to check if the spaceship's thruster works as expected.

```
import 'package:test/test.dart';
import 'package:spaceMission/thruster.dart';

void main() {
  test('Check Thruster', () {
    // Arrange
    var thruster = Thruster();

    // Act
    var thrustPower = thruster.fire();

    // Assert
    expect(thrustPower, equals(1000));
  });
}

```

In this code, we're creating a Thruster, firing it, and then checking if the thrust power is as expected.

### Testing Edge Cases

Testing edge cases is like checking if the spaceship can handle an unexpected asteroid storm or the crew can survive on backup oxygen for a week. These are unusual, but they could happen!

```
void main() {
  test('Thruster fires even if fuel is low', () {
    // Arrange
    var thruster = Thruster();
    thruster.fuel = 1;

    // Act
    var thrustPower = thruster.fire();

    // Assert
    expect(thrustPower, isNot(0));
  });
}

```

In this test, we're making sure that even with low fuel, the thruster still fires. It might not give the full thrust power, but it shouldn't be zero either.

And that's a wrap for unit testing! Just remember, these are your front-line soldiers in the battle against bugs.

[... to be continued ...]

Note: Testing is not just a technical task, it's a way of life! Well, at least for us software engineers. And let's be honest, if you were the one on a spaceship built by your code, you'd want it tested to oblivion and back, right?

Now, work with real input by learning:

[Data Management](data_management.md)