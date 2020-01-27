# Method Parameters Unplugged Activity
This activity should tangibly show how method parameters work.

## Introduction
Start with broken code that tries to use variables out of method scope... have a student try their best to add two numbers in a method. They should not know how to do this yet; it illustrated the need for parameters.

## Activity
### Materials
- 2 Boxes - these represent methods
- Many Cups - different types of cups for different data types

### Side-notes
- Variables are nouns, methods are verbs
- Ask the students for everything as it goes along
- You can also call methods with different values multiple times

### Procedure
1. Two students hold one box each
1. One student writes a variable name on a cup (`numOne`) and then `numTwo`
1. Ask student for a double value, put it in a cup (variable). Instructor puts a secret value in the second cup. Both variables go in the main box (big box)
1. Write the whole method description on the second box.
1. The box 2 student should add numbers - but both boxes are closed.
1. Main box **calls** the method - the method does not know the numbers from the main method!
1.  How do you fix the closed boxes? Why does the small box need cups too? What does `addNumbers` do/use? Two doubles, added.
1. There should be doubles inside of the small box, so - cut a hole in the box! Box still closes the hole (cups)
    - The purpose of the holes is to put the double numbers in there. Variables transfer from one box to another.
1. Different numbers in the small box - different names on the cups. Cut hole and fit part of the cup in - leaving a space for values to sit in the cup. Variables belong to `addNumbers`. Then, when there are cups on the `addNumbers` method, `main` method has to call the `addNumbers` method, this time sending variables along.
1. Main method **duplicates** the numbers when it passes the arguments.
1. Then go back to show how to do it in code
    - Add parameters - special variables on the outside. Arguments get passed in - sets the variables

#### Return statements
Also talk about return statements; go back to unplugged. The method should have an output as well. `main` method asks for the answer - `addNumbers` should give back the sum. Add a "sum" cup to the main box.

```cs
int sum = addNumbers(numOne, numTwo);
```
- Cannot convert `void` to `int`. Look at the `void` in the `addNumbers` signature, what should it be? `int`.
- `main` method calls `addNumbers`, `addNumbers` writes something on a piece of paper, gives it back to `main`.
- Main can put stuff into the cups, and take stuff out of the slot.
- Where does it go in the `main` method? In the sum cup.

Back to code - add the `return` statement. Then output the sum, but also add it to another number - challenge