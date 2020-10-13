# **Functions in Swift**

[see functions.playground to view/run example Swift functions]


## **How to declare a function:** 



`func greet(person: String) -> String`

`greet` = the name of the function and can be used to call the function later in the program 

`person:`  = the argument/parameter name, it is a String  type
 
`-> String` = return type is String 

The function can be called later in the program as: 

`greet(person: "katie")`

`"katie"` is being passed in as the argument here.


## **More About Functions:**

Swift does not require a main function or driver, so there is no specific place a function needs to be defined. It can even be defined after the function has been called and the program will be able to run and return the correct output. 

A function can accept multiple parameters, which can be different types. This would look like: 

`func mult(no1: Int, no2: Int) -> Int `

or 

`func greet(person: String, alreadyGreeted: Bool) -> String `

A function can return multiple values as tuple or array. When defining a return type as tuple it looks like:  

`func minMax(array: [Int]) -> (min: Int, max: Int) `

The benefit of using a tuple is that the return values can be named and accessed more easily outside the function. When defining a return type as an array it looks like: 

`func splitStr(fullStr: String) -> Array <String>`


## **Recursion:**

Recursion is possible in Swift. Like in other languages, the most important part of writing a recursive function in Swift is creating a condition that will insure the function will stop and not be an infinite loop. 

Example of recursive function: 

`func countDownToZero(num: Int) {
    print(num)
   if num > 0 {
       countDownToZero(num: num - 1)
    }
}
print("Countdown:")
countDownToZero(num:3)`

In this case the function will decrease the number each time running through the same function, and print this number to the screen. Once the number is less than zero however the function will end and program control would exit the function. 


## **Pass by Reference or Pass by Value:**

Swift is pass by reference but can be modified to work as pass by value. This happens through use of the ‘inout’ keyword. For example:  

`func swapTwoInts(a: inout Int, b: inout Int) {
   let temporaryA = a
   a = b
   b = temporaryA
}`

This ensures that the value will be accessed, modified and return as the modified value. In calling the function and passing values, the variables do not need to be declared as strings and literals, however a ‘&’ has to be used before the variable names. 


`swapTwoInts(a: &no, b: &co)`


Without the use of inout Swift operates as pass-by-reference and the memory address of the argument is copied to the corresponding parameter instead. 



# **Sources:**

Programiz.com https://www.programiz.com/swift-programming/recursion. Accessed 12 Oct 2020. 

Swift.org  https://docs.swift.org/swift-book/LanguageGuide/Functions.html. Accessed 12 Oct 2020.

Tutorialspoint.com https://www.tutorialspoint.com/swift/swift_functions.htm. Accessed 12 Oct 2020. 

