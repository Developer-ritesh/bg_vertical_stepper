# Vertical Stepper with Dotted Line in Flutter :+1:

`bg_vertical_stepper` is a useful widget to display a process from one step to another in a vertical manner. It is particularly useful for showing progress in multi-step processes, such as forms, checkouts, or onboarding flows.

## Features

- Customizable stepper with vertical orientation.
- Dotted line connecting each step.
- Easy to integrate and use in your Flutter projects.

## ScreenShots

<div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 10px;">
  <div style="width: 100%; height: auto;">
    <img src="https://github.com/Developer-ritesh/bg_vertical_stepper/raw/main/images/1.png" alt="Image 1" style="width: 100%; height: auto; display: block;">
  </div>
  <div style="width: 100%; height: auto;">
    <img src="https://github.com/Developer-ritesh/bg_vertical_stepper/raw/main/images/2.png" alt="Image 2" style="width: 100%; height: auto; display: block;">
  </div>
  <div style="width: 100%; height: auto;">
    <img src="https://github.com/Developer-ritesh/bg_vertical_stepper/raw/main/images/3.png" alt="Image 3" style="width: 100%; height: auto; display: block;">
  </div>
</div>


## Installation

To use this package, add `bg_bg_vertical_stepper` as a dependency in your project's `pubspec.yaml` file:

```yaml
dependencies:
  flutter:
    sdk: flutter
  bg_vertical_stepper: ^1.0.0 # Use the latest version available
  ```

Then, run `flutter pub get` to install the package.


## Usage
Here's a basic example of how to use the `bg_bg_vertical_stepper` package in your Flutter project:

```dart
import 'package:flutter/material.dart';
import 'package:bg_vertical_stepper/src/step.dart' as step;

void main() => runApp(MaterialApp(
      debugShowCheckedModeBanner: false,
      home: HomePage(),
    ));

class HomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    //Create a list of stepper

    List<step.Step> stepper = [
      step.Step(
        shimmer: false,
        title: "first",
        iconStyle: Colors.green,
        content: Align(
          alignment: Alignment.centerLeft,
          child: Text("Content 1"),
        ),
      ),
      step.Step(
        shimmer: false,
        title: "second",
        iconStyle: Colors.green,
        content: Align(
          alignment: Alignment.centerLeft,
          child: Text("Content 2"),
        ),
      ),
      step.Step(
        shimmer: false,
        title: "third",
        iconStyle: Colors.green,
        content: Align(
          alignment: Alignment.centerLeft,
          child: Text("Content 3"),
        ),
      ),
      step.Step(
        shimmer: false,
        title: "fourth",
        iconStyle: Colors.green,
        content: Align(
          alignment: Alignment.centerLeft,
          child: Text("Content 4"),
        ),
      ),
      step.Step(
        shimmer: false,
        title: "fifth",
        iconStyle: Colors.red,
        content: Align(
          alignment: Alignment.centerLeft,
          child: Text("Content 5"),
        ),
      ),
      step.Step(
        shimmer: false,
        title: "Last",
        content: Align(
          alignment: Alignment.centerLeft,
          child: Text("Content 6"),
        ),
      )
    ];

    //Pass the list of steppers into VerticalStepper class

    return Scaffold(
        body: Padding(
      padding: const EdgeInsets.fromLTRB(10, 130, 10, 2),
      child: step.VerticalStepper(
        steps: stepper,
        dashLength: 2,
      ),
    ));
  }
}

```

## Testing
To run tests for the `bg_vertical_stepper` package, use the following command:

```dart
flutter test
```

Make sure to write comprehensive tests to cover all functionalities of the stepper.

## Contributing
Contributions are welcome! If you find any issues or have suggestions for improvements, please create an issue or submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

