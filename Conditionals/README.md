# Conditional Statements

## Overview
Introduce the concept of adding logic to applications using `if` statements. Students will be introduced to the structure of the logic: "if something is true (or false) then do this." Since `if` statements assess some type of conditional statement, students will need to learn the simple Boolean operators: `<`, `>`, `==`, `<=`, `>=`. These conditional statements take a set of values or parameters and equate them to a `true` or `false` value. Starting conditionals use `==`.

After students have some exposure to `if`, introduce them to `else if` and the catch-all `else`. Students should develop an understanding of when an `if`, `else if`, `else` logic tree executes the code in each segment (why some blocks may be skipped) and why using a series of `if` statements might not work. 

## Warmup - Variables & User Input Review Kahoot
Re-run the previous [Kahoot quiz](https://create.kahoot.it/share/1604df76-071b-4777-92e3-1f13559d874c) to review concepts covered thus far.

## Lecture
Present the [Conditional Statements](ConditionalStatements.pptx) PowerPoint.

## Group Activity: Code-Along
Follow these steps to show the students some conditional statements in action:

1. Construct basic `if` statement (plug in `true`) that runs a `WriteLine()`
2. Next, gather user input (what grade are you in?) and run a conditional statement: `if (grade <= 5) {}`
3. Add the else if statement: `else if (grade <= 8) {}`
4. Add the else statement: `else {}`

### Code
```cs
/*
if(true)
{
    Console.WriteLine("I'm inside the 'if' statement!");
}
*/

Console.WriteLine("What grade are you in?");
int studentGrade = Convert.toInt32(Console.ReadLine());

if (grade <= 5)
{
    Console.WriteLine("Elementary");
}
else if (grade <= 8)
{
    Console.WriteLine("Middle School");
}
else
{
    Console.WriteLine("High School")
}
```

## Individual Exercises
Students should complete the [Conditional Exercises](ConditionalExercises.md).

## Challenges
If a student has completed the individual exercises, they should work on the [Challenges](ConditionalChallenges.md).