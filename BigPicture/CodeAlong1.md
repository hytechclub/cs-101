# Choose Your Adventure Game - Part 1
Build the introduction to your adventure game: change the colors, print some text, and create some variables!

## Getting Started
Fork [this Repl](https://replit.com/@HylandOutreach/ChooseYourAdventureStart) to begin. It is a simple C# program that prints out a message. Update the program so that it prints a new message; instead of "Hello World," it should say "You awaken in a strange place."

Run the program, and verify that the message appears in the console.

```cs
using System;

class Program {
  public static void Main (string[] args) {
    Console.WriteLine("You awaken in a strange place.");
  }
}
```

## More Lines
Next up, it's time to add a couple more lines to print in the console.

1. "You see a barn, a big tree, and a path through the woods"
1. An empty message - just for extra space

The code for the next two lines should look something like this:

```cs
Console.WriteLine("You see a barn, a big tree, and a path through the woods.");
Console.WriteLine();
```

## New Colors
Now the text is there, but the colors are still fairly boring. Luckily, it is possible to change the colors of the console in C# by setting _variables_.

1. Make a new line _above_ the existing `Console.WriteLine`
1. Set the `Console.ForegroundColor` variable to a value of `ConsoleColor.White`
1. Under that, set the `Console.BackgroundColor` variable to `ConsoleColor.DarkRed`
1. Under that, clear the console with `Console.Clear();`
    - This sets the whole console to the colors

Run the program and verify that the new colors appear in the console! The code should look something like this:

```cs
Console.ForegroundColor = ConsoleColor.White;
Console.BackgroundColor = ConsoleColor.DarkRed;
Console.Clear();
```

## Creating Variables
Next, add some more text. This time, create new _variables_ to track the information.

1. Create a new `string` variable named `name` set to `"Jules"`
1. Create a new `int` variable named `health` set to `5`
1. Under that, use `Console.WriteLine` to print out the `name` value
    - "Your name is " + `name`
1. Under that, use `Console.WriteLine` to print out the `health` value
    - "Your health is " + `health`

Run the program and verify that the new text appears in the console! The code should look something like this:

```cs
string name = "Jules";
int health = 5;

Console.WriteLine("\nYour name is " + name);
Console.WriteLine("Your health is " + health);
```

## Final Program
By the end of this code-along, the **main.cs** file should look something like this:

```cs
using System;

class Program {
  public static void Main (string[] args) {
    Console.ForegroundColor = ConsoleColor.White;
    Console.BackgroundColor = ConsoleColor.DarkRed;
    Console.Clear();

    Console.WriteLine("You awaken in a strange place.");
    Console.WriteLine("You see a barn, a big tree, and a path through the woods.");
    Console.WriteLine();

    string name = "Jules";
    int health = 5;

    Console.WriteLine("\nYour name is " + name);
    Console.WriteLine("Your health is " + health);
  }
}
```