# Print Smileys: Code-Along
Create a program that will print some smiley faces based on a user's input. Start from a [new C# Repl project](https://replit.com/new/csharp) named "Print Smileys" and follow the instructions below.

The code for the final program is available, but try to complete the exercise before checking the solution.

## Part 1 - Defining the smiley face method
The smiley face method should print a certain number of smiley faces based on a parameter.

1. Define a new method named `PrintSmiley` in the **main.cs** file
    - The method should take in one `int` parameter (`numSmileys`)
    - The method should return `void` (nothing)
1. In the body of the `PrintSmiley` method, create a `while` loop
    - The `while` loop should execute `numSmileys` times
1. In the body of the `while` loop, print a smiley face (`:)`)

<input type="checkbox" id="reveal1" class="reveal-checkbox" />

<label for="reveal1" class="reveal-label">Click to Reveal Code</label>

```cs
public static void PrintSmileys(int numSmileys)
{
    int i = 0;
    while (i < numSmileys)
    {
        Console.WriteLine(":)");
        i++;
    }
}
```

## Part 2 - User input
The main program should ask the user how many smileys to print. If they enter a number less than zero, the program should display an error message.

1. In the `Main` method, display a message asking the user how many smileys they would like
1. Convert their input into an `int`, and store it in a variable
1. Use an `if` statement to check if the number they entered is positive
    - If it is positive, call the `PrintSmiley` method with the number as an argument
    - If it is not positive, display a message saying "Please enter a positive number"

<input type="checkbox" id="reveal2" class="reveal-checkbox" />

<label for="reveal2" class="reveal-label">Click to Reveal Code</label>

```cs
Console.WriteLine("How many smileys would you like?");
int num = Convert.ToInt32(Console.ReadLine());

if (num > 0)
{
    PrintSmileys(num);
}
else
{
    Console.WriteLine("Please enter a positive number");
}
```