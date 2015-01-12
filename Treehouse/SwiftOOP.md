# From Structs to Classes

synthezied initializers?

# Designated Initializer

stored properties vs instance 

If you define the variables in the class as var instead of let, even if you define the instance as a let, you will still be able to change the values because the class defines them as a var.

# Classes and Their Methods
Methods are simply functions associated with classes or structs.

# Overriding Methods

Overriding parents methods require that you have the same method signature for both. Meaning, the override func has to have the same name, parameters, and return type.

You can specify a default value for a parameter and make it optional by putting an underscore in front of it - 
override func discountedPrice(_ percentage: Double = 10.0) -> Double { // do something }

# Convenience Initializers

https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/Initialization.html


# Computed Properties
Don't store any value directly.
Must always be a var and not a let.
Read-only property. Can't store anything. Unless you use a setter method.

# Getter and Setter methods
## Example
get a value / Getter
product.title

set a value / Setter
product.title = "Silly String"

# Structs vs Classes
All the basic value types are built from structs: Int, Double, String, etc...

Creating value types should probably be the default type you choose. Easier to manage than reference types. 

# Value vs Reference Types
## Value advantages
no dependencies
copying is cheap over time
comparison is easy

# Final Exam
let for Shape










