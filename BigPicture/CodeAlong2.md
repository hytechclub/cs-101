# Choose Your Adventure Game - Part 2
For the next part of the game, get some input from the user. This code-along covers `Console.ReadLine`.

## Starting Point
For this code-along, start from the ending point of [part one](CodeAlong1.md). If needed, fork [this Repl](https://replit.com/@HylandOutreach/ChooseYourAdventurePartOne) project to begin.

## Asking for the Name
Start by customizing the game based on the user's name.

1. Make a new line in the code _above_ where the `name` variable is set
1. Use a `Console.WriteLine` statement to ask the user for their name
1. Under that, use `Console.ReadLine` to get the name the user puts in
    - Replace the `name` variable value with `Console.ReadLine`

Run the code, and verify that it is possible to enter a name! The name should then be used to greet the user.

The code should look something like this:

```cs
Console.WriteLine("What is your name?");
string name = Console.ReadLine();
```

## Asking Where to Go
Next, it's time to start making the game more interactive. So far, the program lists the player's surroundings, but does not let them do anything with them. In this section, ask the user where they would like to go.

1. Make a new line under the line that prints the user's health
1. Use `Console.WriteLine` to ask the user where they want to go
    - List the options: barn, tree, path
1. Make a new line under that, and create a new `string` variable named `go`
1. Set the `go` variable to a `Console.ReadLine()` value

Run the code, and verify that it is possible to enter an interaction! Nothing should happen with it yet, though.

The code should look something like this:

```cs
Console.WriteLine("\nWhere do you go? (barn, tree, path)");
string go = Console.ReadLine();
```

## Showing Where to Go
Now the user has chosen where to go, so the program can show them what they chose. In the future, the program will be able to do different things based on the user's choice. For now, just print out a message with the choice.

1. Make a new line under the existing lines
1. Use `Console.WriteLine` to display a message showing the value of the `go` variable

Run the code, and verify that the program can show the user where they choose to go! The code should look something like this:

```cs
Console.WriteLine("\nYou go to the " + go);
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
    Console.WriteLine("You see a barn, a big tree, and a path through the woods.\n");

    Console.WriteLine("What is your name?");
    string name = Console.ReadLine();
    int health = 5;

    Console.WriteLine("\nHello " + name);
    Console.WriteLine("Your health is " + health);

    Console.WriteLine("\nWhere do you go? (barn, tree, path)");
    string go = Console.ReadLine();

    Console.WriteLine("\nYou go to the " + go);
  }
}
```