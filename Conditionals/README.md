# Week 3: User Input and Conditional Statements

## Overview
In week 3 we will introduce the concept of adding logic to applications using if() statements. Students will be introduced to the structure of the logic, ‘if something is true (or false) then do this work’. Since if() statements assess some type of conditional statement,  students will need to learn the simple Boolean operators, <, >, =, <=, >=. These conditional statements take a set of values or parameters and equate them to a true or false value. Starting conditionals will be if and int == int or string == string. 

After students have some exposure with if(), introduce them to else if() and the catch-all else. Students should develop an understanding of when an if(), else if(), else() logic tree executes the code in each segment (why we skip blocks after we enter one) and why using a serious of if() statements doesn’t work. 

## Warmup - Variables Review Kahoot
https://create.kahoot.it/share/duplicate-of-c-101-data-types/9378165b-38f3-4a00-b266-8ca49976db1d

## Lecture
* Lecture: PowerPoint "Reading User Input"
    * Use `Console.ReadLine` to read input from the user
    * Use `Convert.ToInt32` to convert strings into integers

* Lecture: PowerPoint "Conditional Statements"
    * Use conditional statements to traverse different logic paths.
        * `if()`
        * `else if()`	
        * `else()`

    * Use simple Boolean operators to check conditional statements
        * `<`, `>`, `==`

## Group Activity
* Code Along
    1. Construct basic `if` statement (plug in `true`) that runs a `WriteLine()`
    2. Next, gather user input (what grade are you in?) and run a conditional statement. `if (grade >= 5 elementary)` 
    3. Introduce else statement `else if (grade >= 8 middle school)`
    4. Introduce else if statement `else (grade >= 12 highschool)`

```cs
/*
if(true)
{
    Console.WriteLine("I'm inside the 'if' statement!");
}
*/

Console.WriteLine("What grade are you in?");
int studentGrade = Convert.toInt32(Console.ReadLine());

if (grade >= 5)
{
    Console.WriteLine("Elementary");
}
else if(grade >= 8)
{
    Console.WriteLine("Middle School");
}
else if(grade >= 12)
{
    Console.WriteLine("High School")
}
```

## Individual Exercises
Read user input/ If/else logic exercises. There are also challenges.

## Kahoot
Use [Kahoot](https://play.kahoot.it/#/k/7bcbcc28-adaf-46d9-847b-0291f528e62a) as an exit evaluation 