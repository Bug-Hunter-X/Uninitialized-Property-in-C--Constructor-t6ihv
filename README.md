# Uninitialized Property in C# Constructor

This example demonstrates a common issue in C# where a class property is not explicitly initialized in the constructor.  If a property doesn't have a default value assigned in its declaration or the constructor, it will be assigned a default value for its type (0 for integers, null for reference types, etc.). This might lead to unexpected behavior if you attempt to use the property before it's explicitly set.

## Bug:

The `ExampleClass` in `bug.cs` showcases this issue: The `MyProperty` is not given an initial value.  Attempting to use `MyProperty` before it is explicitly assigned will lead to unpredictable behavior.

## Solution:

The `bugSolution.cs` file provides the solution: Initialize the `MyProperty` in the constructor, explicitly setting it to a desired value to avoid undefined behavior.