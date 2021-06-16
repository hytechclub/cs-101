# Choose Your Path
In this code-along activity, create a basic game that allows the player to choose from a number of possible paths. In the story, the player will make choices that will determine their fate. The game will track their `health`, which will change based on the choices. At the end, if the player survives, they will find a treasure. Otherwise, they will not be so lucky.

## Setup
First, do some basic setup for the game.

1. Create a [new C# Repl project](https://replit.com/new/csharp)
1. Name it "Choose Your Path"
1. In the **main.cs** file, in the `Main` body, set the text color:  
    ```cs
    Console.ForegroundColor = ConsoleColor.Red;
    ```
1. Under that, set the background color:  
    ```cs
    Console.BackgroundColor = ConsoleColor.White;
    ```
1. Under that, clear the console to make it a little cleaner:  
    ```cs
    Console.Clear();
    ```
1. Next, use `Console.WriteLine` to display a message saying "Welcome to the Path"
1. Under that, add an empty `Console.WriteLine` to make some extra space

Run the program, and verify that the message appears in the proper color.

```cs
using System;

class MainClass
{
    public static void Main (string[] args)
    {
        Console.ForegroundColor = ConsoleColor.Red;
        Console.BackgroundColor = ConsoleColor.White;
        Console.Clear();

        Console.WriteLine("Welcome to the Path.");
        Console.WriteLine("");
    }
}
```

## Using a Variable
The game should track the `health` of the player throughout the story. This will help determine the ultimate outcome.

1. In the **main.cs** file, find the bottom of the `Main` body
2. There, declare a new `int` variable named `health`
3. Set the `health` variable to `5`
4. Under that, display a message printing the current `health` value

Run the program, and verify that the proper `health` value appears.

```cs
int health = 5;
Console.WriteLine("Your current health level is: " + health);
```

## Asking a Question
Now it's time to display a choice for the player! This can be done using `Console.WriteLine` statements. For this question, say the player comes across a large pastry, and they have to decide whether or not to eat it.

1. Display a message asking the question
1. Display option `"A"`: eat the pastry
    - Add some space in front of the option text to make it a little more readable
1. Display option `"B"`: do not eat the pastry
1. Display an empty line just for some space

Run the program, and verify that the new messages appear in a readable format.

```cs
Console.WriteLine("You see a giant donut. What do you do?");
Console.WriteLine("  A. Eat it");
Console.WriteLine("  B. Ignore it");
Console.WriteLine("");
```

## Getting an Answer
Next, the player should be able to answer the question. This can be done using `Console.ReadLine`.

1. First, use `Console.Write` (not `WriteLine`) to show the user where to type: `"> "`
1. Create a new `string` variable named `choice`
1. Set the `choice` variable to the result of a `Console.ReadLine()`
1. Under that, use `Console.Clear()` to clean things up

Run the program again, and verify that it is possible to enter a choice!

```cs
Console.Write("> ");
string choice = Console.ReadLine();
Console.Clear();
```

## Handling the Player's Choice
Now comes the actual game part. The code should look at what the player chose, and do different things depending on the choice.

- If the player chose "A", their `health` should go down by `1`, and a message should say the pastry tasted good.
- If the player chose "B", their `health` should go down by `2`, and a message should say they are dealing with emotional pain.

This will be possible using conditional statements.

### `if` Setup
Start with an `if` statement. This statement should check _if_ the player chose "A" as their option.

1. Under the `Console.Clear()`, make a new line
1. Type in `if`
1. After that, type in parentheses `()`
1. After the parentheses, type in curly brackets `{}`
1. Press enter within the curly brackets to space them out
1. Within the `(` and `)`, add a boolean expression checking if the `choice` variable value is equal to `"A"`

```cs
if (choice == "A")
{

}
```

### `if` Body
Now the `if` condition is set up, but it needs to do something if the condition is `true`!

1. Within the `{` and `}`, make a new line
1. Add code to set the `health` variable to equal itself minus `1`
1. Under that, still within the `{` and `}`, add a `Console.WriteLine`
1. Make the `WriteLine` say that the pastry tasted good

Run the program, and verify that entering "A" as the choice will make the message display! Entering anything else won't do anything yet...

```cs
if (choice == "A")
{
    health = health - 1;
    Console.WriteLine("You eat the donut, and it is delicious.");
}
```

### `else if`
Now the `"A"` choice has been handled, but what about `"B"`? Use an `else if` clause to handle the second option.

1. Under the `}` from the `if`, type in `else if`
1. After the `else if`, add parentheses `()`
1. After the parentheses, add curly brackets `{}`
1. Make the `if` condition (between parentheses) check if `choice` is `"B"`
1. In the body (between curly brackets), set `health` to itself minus `2`
1. Under that, still in the `else if` body, add a `Console.WriteLine`
1. Make the `WriteLine` say that the player is dealing with emotional pain

Run the program again, and verify that entering either option will display the proper result!

```java
else if (choice == "B")
{
    health = health - 2;
    Console.WriteLine("You do not eat the donut, and the emotional pain takes its toll.");
}
```

## Another Question
Adding another question to the game will be very similar to the first question. For the next question, ask the player how they want to get to school.

1. Under the end of the `else if` block (after the `}`), make a new line
1. Display a blank line, and then print out the current `health` variable valuable
1. Under that, display the question - ask the player how they get to school.
1. Under that, display the `"  A. Walk"` option
1. Similarly, display the `"  B. Take the bus"` option
1. Display a new empty line
1. Write the `"> "` for the player to answer using `Console.Write`
1. Create a new variable named `choice2` of type `string`
1. Set the `choice2` variable to `Console.ReadLine()`
1. Clear the console to clean things up

Run the program again, and verify that the second question appears and they player can answer.

```cs
Console.WriteLine("");
Console.WriteLine("Your current health level is: " + health);

Console.WriteLine("You need to get to school. How do you get there?");
Console.WriteLine("  A. Walk");
Console.WriteLine("  B. Take the bus");
Console.WriteLine("");
Console.Write("> ");
string choice2 = Console.ReadLine();

Console.Clear();
```

## Handling the Player's Second Choice
So what should happen based on the answers? If the player walks to school, their health should go up because they get some exercise. If they take the bus, they will inevitably trip and everyone will laugh at them. Write code to handle these results.

1. Under the `Console.Clear`, create an `if` structure
    - `if` keyword
    - Parentheses
    - Curly brackets
1. For the `if` condition, check if `choice2` is `"A"`
1. In the body of the `if` (between curly brackets):
    - Set `health` to `health + 1`
    - Display a message saying that the exercise helped the health
1. After the `}`, create an `else if` structure
    - `else if`
    - Parentheses
    - Curly brackets
1. For the `else if` condition, check if `choice2` is `"B"`
1. In the body of the `else if` (between curly brackets):
    - Set `health` to `health - 3`
    - Display a message saying that the player tripped and people laughed

Run the program again, and verify that both questions can be answered!

```java
if (choice2 == "A")
{
    health = health + 1;
    Console.WriteLine("You get some exercise by walking.");
}
else if (choice2 == "B")
{
    health = health - 3;
    Console.WriteLine("You trip as you get on the bus, and everyone laughs.");
}
```

## The End
Now that the player has gone through a decent amount of their day, it's time to end the game. If the player's `health` value has dipped below `1`, they will lose the game. Otherwise, they wil find a bunch of money.

1. Under the `else if` structure, make a new line
1. Use `Console.WriteLine` to display an empty line
1. Under that, create an entire `if`/`else` structure
    - `if` keyword
    - Parentheses
    - Curly brackets
    - `else` keyword
    - Curly brackets
1. For the `if` condition, check if the `health` value is less than `1`
1. In the body of the `if`, print a message saying the player has lost the game
    - This will happen if the condition is `true`
1. In the body of the `else`, print a message saying the player has found some money
    - This will happen if the condition is `false`

Run the program, and verify that the proper results happen based on the choices made! The player should only lose if they choose not to eat the donut, and they choose to take the bus.

```cs
Console.WriteLine("");

if (health < 1)
{
    Console.WriteLine("You have died.");
}
else
{
    Console.WriteLine("When you get to school, you immediately find $500.");
}
```

## Final Code
```cs
using System;

class MainClass
{
    public static void Main (string[] args)
    {
        Console.ForegroundColor = ConsoleColor.Red;
        Console.BackgroundColor = ConsoleColor.White;
        Console.Clear();

        Console.WriteLine("Welcome to the Path.");
        Console.WriteLine("");

        int health = 5;
        Console.WriteLine("Your current health level is: " + health);

        Console.WriteLine("You see a giant donut. What do you do?");
        Console.WriteLine("  A. Eat it");
        Console.WriteLine("  B. Ignore it");
        Console.WriteLine("");

        Console.Write("> ");
        string choice = Console.ReadLine();
        Console.Clear();

        if (choice == "A")
        {
            health = health - 1;
            Console.WriteLine("You eat the donut, and it is delicious.");
        }
        else if (choice == "B")
        {
            health = health - 2;
            Console.WriteLine("You do not eat the donut, and the emotional pain takes its toll.");
        }

        Console.WriteLine("");
        Console.WriteLine("Your current health level is: " + health);

        Console.WriteLine("You need to get to school. How do you get there?");
        Console.WriteLine("  A. Walk");
        Console.WriteLine("  B. Take the bus");
        Console.WriteLine("");
        Console.Write("> ");
        string choice2 = Console.ReadLine();

        Console.Clear();

        if (choice2 == "A")
        {
            health = health + 1;
            Console.WriteLine("You get some exercise by walking.");
        }
        else if (choice2 == "B")
        {
            health = health - 3;
            Console.WriteLine("You trip as you get on the bus, and everyone laughs.");
        }

        Console.WriteLine("");
        
        if (health < 1)
        {
            Console.WriteLine("You have died.");
        }
        else
        {
            Console.WriteLine("When you get to school, you immediately find $500.");
        }
    }
}
```