Swift Datatypes

[Test out running these datatypes in the HelloWorld2.playground file]

Naming Requirements:

Variables can contain almost any character including Unicode characters. They can not contain whitespace characters, mathematical symbols, arrows, private-use Unicode scalar values or line-and box-drawing characters. Variables also cannot begin with a number, but a number can be contained elsewhere in the name. These restrictions are enforced by the compiler.

Traditionally variable are also written in camel case, with lowercase letter first and uppercase following. This is not enforced by the compiler and is considered a standard in the community. 

Declaring Variables:

Variables and constants declared in Swift do not immediately need to be declared a type. The syntax [ var varname =  value] can be used. Through type inference at compile time, Swift will try to deduce which type the user intends to save there.

To declare a variable as a datatype this syntax is used:

var varname: datatype 



Swift Special Datatypes:

Swifts also uses Tuples, which allow the user to group different types of values into one single value, similar to an array/list. 

let nameAge = (“Katie”, 21) 

Tuples can be decomposed: 

let (name, age) = nameAge;

So that individual elements can be accessed more easily. Elements can now be accessed individually by location or by name.

Swift also uses Optionals. These values can either indicate a value is there but hidden, or there isn’t a value. An optional value is represented by a ‘?’ following the datatype. It can be set to ‘nil’ if it has a valueless state. If you define an optional without providing a value, then it is automatically set to nil. 



Type Conversions:

Conversions are narrowing, and floating points will always be truncated to initialize a new integer value. 

In order to convert integers into other numeric types, it has to be done on a case-by-case basis. You must initialize a new variable of the desired type with the existing value.

X = “5” + 6  will not compile. The error returned will explain that type “String” cannot be converted to expected argument type “Int”. Nothing can be done to make this compile, unless the String 5, is changed to an Int 5. 



Quick Facts and Limitations:

•	Once a variable has been declared a type it cannot store variables of a different type. 

•	It is recommended that all general-purpose integer type variables are declared as Int, to prevent the need for type conversion.

•	Math functions can only be done between the same types (int + int or Float + Float etc.)

•	Arrays can only contain the same type (use a Tuple if you need to list different types) 

•	Swift is strongly typed. It will check to ensure that the value is the correct type. 

•	Swift is statically typed because this check happens at compile time. 

Overall, the Swift compiler will warn the user if they are making an error in naming a datatype, or in its use. It is meant to be intuitive and may flag an error early, even if the error will not affect running the program. This makes it easy to avoid these limitations and learn to code correctly in Swift. 



Sources: 

Developer.Apple.com https://developer.apple.com/documentation/swift/array Accessed Sept. 22, 2020. 

Developer.Apple.com https://developer.apple.com/documentation/swift/dictionary Accessed Sept. 22, 2020. 

Swift.org  https://swift.org/documentation/api-design-guidelines/ Accessed Sept. 22, 2020. 

Swift.org https://docs.swift.org/swift-book/LanguageGuide/TheBasics.html Accessed Sept. 22, 2020. 

