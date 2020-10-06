[See Code Labeled FoPCandLoops to run examples] 

[Conditionals:]

Swift supports if, else if, and else statements. These look like: 

if yesOrNo != true {

    print ("Its false part2!") }
    
else if yesOrNo != false  {

    print ("Its true part2!")
    
}
else {print ("Well.. something is wrong..") }


Conditionals can be one-condition or multi-condition. One-condition can look like == (equal to) or != (not equal too) and multi-conditions can look like && (and ) or || (or). 

var x: Int

    x = 11
    
if (x>10 && x < 20) {

    print ("x is between 10 and 20.")
    
}

if (x>10 || x<10){

    print ("x is not 10")
    
}


[Loops:] 

Swift supports while loops, repeat/while loops, for/in and switch/case loops. 

While loop: The condition is checked before the action completed. 

while num > 10  {

    num -= 1
    
    print ("The number is now: \(num)")
    
}

Repeat/while loop: Is similar in concept to a do/while loop. The action will done before the condition is checked. 

num = 30;

repeat {

    print ("we havent reached the number yet")
    
    num -= 1
    
}while num > 20


For -In loops: similar to foreach loop, because it iterates through a list.  

for num in emptyInt{

    print (num)
}

Switch/Case: is similar to switch/cases in other languages. EXCEPT it does not have an implicit fallthrough. This means a break statement isn’t necessary at the end of each case. Once a case has been evaluated to be true and the appropriate actions have taken place, then the Switch statement finishes it’s execution. 
However a Switch statement is required to be exhaustive, and a default case must always be supplied. 

word = "bobby"

switch word {

case "ellie":

    print ("the middle child")
    
case "katie":

    print ("the oldest child")
    
case "bobby":

    print ("the youngest child")
    
default: //default required

   break
   
}

If fall-through is required, fallthrough  can be added at the end of each case. This will force the switch/case loop to act more like a traditional and evaluate each case after the one where the fallthrough is used. 

Swift also supports a for loop through a range of numbers: 

for index in 1...10{ 

    print ("the index is going up: \(index)");
}


The range is inclusive and will include both 1 and 10. 

[Break/Continue:] 

A  break can be used both in a traditional loop and in a switch-case loop. In both cases it ends the execution immediately and transfers program control to the code outside the loops closing bracket ( } ). As previously stated, it is not needed in the switch/case loop. However, most commonly its used in the default case, which although required often is not desired to be used. 

A continue  will stop the loop and tell it begin back at the beginning. It’s a way of telling the program I am done with this ‘iteration’ of the loop but I am not done with the loop entirely.   
(see code for example) 

Short Circuit Evaluation: 

Short-Circuit Evaluation does occur in Swift 

Ex)

num = 3

if num < 5 || num > 20 {

   print ("Short circuit evaluation happens!")
}

if num < 5 && num > 20 {

   print ("Lets try with and")
}

The first if statement, with the ( || ) operator, only checks the first side of the statement, and evaluates that the number is less than 5 and the output will be the print statement. On the other hand, in the ( && ) statement it will not evaluate to be true, so the statement has been evaluated on both sides. 

“[Dangling Else” Problem:]

Swift handles the ‘dangling else’ problem by supplying the use of ‘else ifs’ which allow the if statements to be pseudo- nested. The code will allow you to write more than one ifs statements in a row with only one else. It will follow the flow of control in evaluating each if statement. If the last one is false, then the else statement will be printed. If the last if statement is true, the final else will not be evaluated.  (see end of code for example) 


[Sources:] 

Swift.org https://docs.swift.org/swift-book/LanguageGuide/ControlFlow.html. Accessed 4 Oct 2020. 

Swift.org https://docs.swift.org/swift-book/LanguageGuide/BasicOperators.html. Accessed 4 Oct 2020. 
