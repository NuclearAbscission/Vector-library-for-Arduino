# Vector-library-for-Arduino
The Vector library provides a dynamic array implementation for Arduino that allows you to work with a collection of **elements of any type** (meaning you can store your custom defined objects in the vector). It is a flexible alternative to the standard fixed-size arrays in Arduino. 

## Features

- Dynamic resizing: The vector automatically adjusts its size as elements are added or removed.
- Access elements: You can access individual elements using the index operator.
- Range-based for loop: You can iterate over the vector using a range-based for loop.
- Customizable storage: The library supports vectors of custom objects.

## Installation

1. Download the Vector library by clicking on the "Download ZIP" button from the GitHub repository.
2. In the Arduino IDE, go to "Sketch" -> "Include Library" -> "Add .ZIP Library".
3. Select the downloaded ZIP file and click "Open".
4. The library should now be imported into your Arduino IDE.
Alternatively you can relocate the 'Vector.h' file in your project directory.

## Usage

1- Include the Vector library in your Arduino sketch:

```cpp
#include <Vector.h>
```

2- Create a vector of your desired type. For example, to create a vector of integers:

```cpp
Vector<int> myVector;
```

3- Use the vector functions to work with the vector:

```cpp
// Add elements to the vector
myVector.push_back(10);
myVector.push_back(20);
myVector.push_back(30);

// Access elements
int firstElement = myVector[0];    // Access by index
int lastElement = myVector.back(); // Access the last element

// Modify elements
myVector[1] = 50;                  // Modify element at index 1

// Get the size of the vector
size_t vectorSize = myVector.size();

// Iterate over the vector using a range-based for loop
for (const auto& element : myVector) {
  // Process each element
  // ...
}

// Clear the vector
myVector.clear();
```

4- Customize the library for your specific needs. You can modify the Vector class or create vectors of your custom objects by specifying the type when creating the vector.

```cpp
// Custom Object
class MyObject {
  // Add your custom object's properties and methods here
};

// Create a vector of MyObject
Vector<MyObject> myObjectVector;
```

# Acknowledgements

The Vector library was inspired by the standard C++ vector and aims to provide similar functionality for Arduino projects.
