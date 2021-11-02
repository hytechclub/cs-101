# Choose Your Adventure Game - Part 3
For the next part of the game, change what happens in the program based on the user's input. This code-along covers `if`/`else` statements.

## Starting Point
For this code-along, start from the ending point of [part two](CodeAlong2.md). If needed, fork [this Repl](https://replit.com/@HylandOutreach/ChooseYourAdventurePartTwo) project to begin.

## Going to the Barn
If the user decides to go to the barn, they should find a potion. They should also gain one health point.

1. At the bottom of the main block, make a new line
1. Create an `if` structure using `if () { }`
1. For the condition, check if the user typed in "barn"
1. For the body, display a message saying the player found a potion
1. Also in the body, set `health` to be itself plus one

Run the program, and verify that it is possible to visit the barn. The message should only appear _if_ the player types in "barn" when prompted! The code should look something like this:

```cs
if (go == "barn")
{
    Console.WriteLine("You go into the barn and find a potion. +1health");
    health = health + 1;
}
```

## Going to the Tree
Next, if the user decides to go to the tree, they should find some bees. They should also _lose_ one health point.

1. Under the `if` block `}`, make a new line
1. Create an `else if` structure using `else if () { }`
1. For the condition, check if the user typed in "tree"
1. For the body, display a message saying the player found some bees
1. Also in the body, set `health` to itself minus one

Run the program, and verify that it is possible to visit the tree. The new message should only appear _if_ the player types in "tree" when prompted! The new code should look something like this: 

```cs
else if (go == "tree")
{
    Console.WriteLine("You check out the tree and find some bees. -1health");
    health = health - 1;
}
```

## Going down the Path
The last option is this: going down the path. In this case, the player should face the monster and lose _five_ health points.

1. Under the `else if` block `}`, make a new line
1. Create an `else if` structure using `else if () { }`
1. For the condition, check if the user typed in "path"
1. For the body, display a message saying the player faced the monster
1. Also in the body, set `health` to itself minus five

Run the program, and verify that it is possible to visit the path. The new message should only appear _if_ the player types in "path" when prompted! The new code should look something like this: 

```cs
else if (go == "path")
{
    Console.WriteLine("You go down the path and face the monster.");
    health = health - 5;
}
```

## Going Somewhere Invalid
Now the player can successfully visit all of the places, but they might type in something else. Handle this case by telling them they entered an invalid option.

1. Under the `else if` block `}`, make a new line
1. Create an `else` structure using `else { }`
  - Note that there is no condition for an `else`
1. For the body, display a message saying invalid option

Run the program, and verify that the message appears when it should. The new message should only appear _if_ the player types in something other than "barn", "tree", or "path" when prompted! The new code should look something like this: 

```cs
else
{
    Console.WriteLine("Invalid option.");
}
```

## End Result
Lastly, the player's final health will determine whether or not they survive. Print out a message with this information at the end of the program.

1. Make a new line at the bottom of the main block
1. Create an `if`/`else` structure using `if () { } else { }`
1. For the `if` condition, check if the `health` variable is less than `1`
1. In the body of the `if`, print out "You have died."
1. In the body of the `else`, print out "You make it out of the woods."

Run the program, and verify that the proper message appears based on the user choice! If the user goes down the path, they should die. Otherwise, they should live. The new code should look something like this:

```cs
if (health < 1)
{
    Console.WriteLine("You have died.");
}
else
{
    Console.WriteLine("You make it out of the woods.")
}
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

    if (go == "barn")
    {
      Console.WriteLine("You go into the barn and find a potion. +1health");
      health = health + 1;
    }
    else if (go == "tree")
    {
      Console.WriteLine("You check out the tree and find some bees. -1health");
      health = health - 1;
    }
    else if (go == "path")
    {
      Console.WriteLine("You go down the path and face the monster.");
      health = health - 5;
    }
    else
    {
      Console.WriteLine("Invalid option.");
    }

    if (health < 1)
    {
      Console.WriteLine("You have died.");
    }
    else
    {
      Console.WriteLine("You make it out of the woods.")
    }
  }
}
```