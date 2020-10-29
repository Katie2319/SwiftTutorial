# **SCOPE IN SWIFT** 

[see code labeled PLP6] 

## Scope of Variable:

Once x is declared in the main body of the program:
 
`var x: Int
x = 2`

It doesn’t change if a variable with the same name is also declared in other areas of code, including inside a for loop and inside a function. Indicating essentially two variables exist with the same name, one is only accessible within the for loop/function and one is accessible outside these pieces of code. 

Within the for loop or function the new ‘x’ value can be changed, but whatever value it is once the for loop or function completes execution is not passed to the x value outside of the for loop/function. 

However if ‘x’ is not redeclared within the for loop whatever actions taken to change the value of x are passed to the x that sits outside the for loop. 

The same thing happens with functions. Changing the value of x within the function ultimately gets passed to the variable ‘x’ which exists outside the function if it was not redeclared within the function. 


## Globally Accessible Variables

Globally accessible variables can created by using a struct with format: 

`struct Book {
   static let title: String="Harry Potter"
   static let pageCount: Int = 356
}`

In order to then reference these variables the form (Book.title) is used. 

A variable is also globally accessible if it is labeled as a var. For example:  
`var name: String = "katie"`

name will = “katie” within program control logic including loops and functions, indicating that it is a globally accessible variable. 
 
## Passed By Value/Passed By Reference

In Swift the most common (only) pass-by-reference type is a class. Creating two instances of a class and setting them equal to each will ensure that they both point to the same location in memory. This means that making a change to the attributes for one instance will also cause the same change to be present in the other instance of the class as well. 

In Swift, primitive types (Int, String, Boolean etc.) are pass by value along with pretty much any other kind of type (struct, enum, tuple, array). This means that when these values are set equal to each other, they still point to two separate instances of the class. Making a change to one of the values only affects that one and does not cause a change to occur for the other value. 


## Test Code 

`var charListA: Array<Character> = ["c", "a", "t"]`
`var charListB: Array<Character> = ["d", "o", "g"]`

`charListA=charListB`

`charListB[0] = "u"`

`print (charListA); //returns 'd' 'o' 'g'`
`print (charListB); //returns 'u' 'o' 'g'`

These results indicate that Swift handles arrays as pass-by-value. This is because if it were pass-by-reference. The statement `charListA=charListB`
 Would indicate that both charListA and charListB point to the same value and changing the value of `charListB[0]`, would cause the same change to happen in charListA. Because this did occur based on the results, instead of the equals statement pointing two references to the same place, two separate values are created. 

## Sources:

Raywenderlich.com https://www.raywenderlich.com/9481-reference-vs-value-types-in-swift  Accessed 29 October 2020. 

Tutorialspoint.com https://www.tutorialspoint.com/how-to-create-and-use-global-variable-in-swift   Accessed 27 October 2020. 
