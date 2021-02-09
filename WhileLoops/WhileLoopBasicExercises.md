# While Loop Basic Exercises
After completing the [code-along](FactorialFollowAlong.md), complete these exercises.

## 1. Print Fifty Smiles
Using `while` loops, it is possible to repeat things a certain number of times. Rather than copying and pasting the same code over and over, a `while` loop makes it possible to write code once and execute it any number of times.

For this exercise, print out fifty smiley face emoji: 😊

1. Create a [new C# Repl project](https://repl.it/new/csharp)
1. Name it "Fifty Smiles"
1. In the **main.cs** file, in the `Main` body, print a welcome message
1. Under that, declare a new `int` variable named `i`
1. Set the `i` variable to `0`
1. Under that, create a `while` loop structure
    - `while` keyword
    - Parentheses
    - Curly brackets
1. For the `while` condition (between the parentheses), check if `i` is less than `50`
1. For the `while` body (between the curly brackets), print out a smiley face
1. Under that, still within the `{` and `}`, increment `i` by 1: `i++`

Run the program, and verify that 50 smiley faces appear!

## 2. Print Twelve Eggs
Any number of statements can go within the body of a `while` loop. In this exercise, print out 12 eggs using ASCII art. Each egg can be drawn to the screen with these commands:

```cs
Console.WriteLine("  ,''`.");
Console.WriteLine(" /     \\");
Console.WriteLine(":       :");
Console.WriteLine(":       :");
Console.WriteLine(" `.___,'");
Console.WriteLine("");
```

1. Create a [new C# Repl project](https://repl.it/new/csharp)
1. Name it "A Dozen Eggs"
1. In the **main.cs** file, in the `Main` body, print a welcome message
1. Under that, declare a new `int` variable named `i`
1. Set the `i` variable to `0`
1. Under that, create a `while` loop structure
    - `while` keyword
    - Parentheses
    - Curly brackets
1. For the `while` condition (between the parentheses), check if `i` is less than `12`
1. For the `while` body (between the curly brackets), use the `Console.WriteLine`s to print an egg
1. Under that, still within the `{` and `}`, increment `i` by 1: `i++`

Run the program, and verify that a dozen eggs appear!

## 3. Annoying Bot
It is also possible to use `while` loops more dynamically. Instead of repeating a specific number of times, the loop can repeat until any condition is met. For example, a loop could repeat until the user entered a certain phrase.

In this exercise, pester the user until they respond in a very particular way.

1. Create a [new C# Repl project](https://repl.it/new/csharp)
1. Name it "Annoying Bot"
1. In the **main.cs** file, in the `Main` body, print a welcome message
1. Under that, declare a new `string` variable named `answer`
1. Set the `answer` variable to `""`
1. Under that, create a `while` loop structure
    - `while` keyword
    - Parentheses
    - Curly brackets
1. For the `while` condition (between the parentheses), check if `answer` is equal to `"You are not annoying"`
1. In the `while` body (between curly brackets), add a `Console.WriteLine` statement
1. Make the statement print out "Am I annoying you yet?"
1. Under that, still within the `{` and `}`, create a new line
1. On that line, set the `answer` variable to a `Console.ReadLine()`
1. Under that, use an empty `Console.WriteLine` to print out an empty line
1. Outside of the `while` loop, print out a "Goodbye" message

Run the program, and enter a few responses. Verify that the loop continues forever, _unless_ the message of "You are not annoying" is entered.

## 4. Rainbow Road Forever
It is also possible to make a `while` loop that continues forever. Note that an infinite loop _can_ be a serious code error, but it can also be used for a useful purpose.

In this exercise, create a program that infinitely prints out a rainbow road.

1. Create a [new C# Repl project](https://repl.it/new/csharp)
1. Name it "Rainbow Road"
1. In the **main.cs** file, in the `Main` body, print a welcome message
1. Under that, create a `while` loop structure
    - `while` keyword
    - Parentheses
    - Curly brackets
1. For the `while` condition (between the parentheses), simply put `true`
1. In the `while` body (between curly brackets), set the text color to red
    - `Console.ForegroundColor = ConsoleColor.Red;`
1. Under that, still within the `{` and `}`, add a `Console.WriteLine()`
1. In the `WriteLine`, print out `"|   ||   |"`
1. Under that, add a second `Console.WriteLine` printing the same thing
1. Repeat the three lines of code from above, updating the color for each of these colors:
    - `ConsoleColor.DarkYellow`
    - `ConsoleColor.Yellow`
    - `ConsoleColor.Green`
    - `ConsoleColor.Cyan`
    - `ConsoleColor.Blue`
    - `ConsoleColor.Magenta`

Run the program, and verify that a rainbow road rolls on forever! There should be a total of 21 statements within the `while` loop body.