# Choose Your Adventure Game - Part 4
For the next part of the game, make it repeat the options until the end. This code-along covers `while` loops.

## Starting Point
For this code-along, start from the ending point of [part three](CodeAlong3.md). If needed, fork [this Repl](https://replit.com/@HylandOutreach/ChooseYourAdventurePartThree) project to begin.

Note that for this activity, a lot of the code will need to move around. This can be challenging because the code already exists, it just needs to be moved to a different place. Make sure everything goes where it should!

## An Infinite Loop
Start by creating a simple loop structure that will keep going forever.

1. Make a new line under the `health` variable declaration
1. Create a new `bool` variable named `keepGoing` set to `true`
1. Under that, create a `while` loop structure with `while () { }`
1. For the `while` condition, use `keepGoing`
1. For now, in the body of the `while` loop, display a message of `"\nHello" + name`

At this point, running the code should print out "Hello" infinitely. Eventually, this should be fixed, but for now, that is the intended result! The code for this part should look something like this:

```cs
int health = 5;
bool keepGoing = true;

while (keepGoing)
{
    Console.WriteLine("\nHello " + name);
}
```

## Looping Options
Now that the loop is set up, it's time to make it loop the options infinitely. Instead of simply infinitely printing out "Hello", it should keep asking the user what to do, and respond appropriately. The code is already there, it just needs to go in the right place.

1. Find the `Console.WriteLine("\nHello " + name);` line in the code
1. Find the `else { Console.WriteLine("Invalid option."); }` block in the code
1. Highlight and copy all of the code between those parts
1. Paste all that code into the body of the `while` loop
1. Indent the pasted code for readability
1. Remove the code that was copied from its original place

Now, running the program should infinitely print out options for the player. The `health` value should update each time through the loop, as long as a valid option is entered. The code should look something like this:

```cs
while (keepGoing)
{
    Console.WriteLine("\nHello " + name);
    
    /* copied code */
}

if (health < 1)
{
    /* continued */
}
```

## Stopping the Loop
The loop should not actually be infinite - there should be a way to get out of it. The game should end when the player decides to go down the path.

1. Find the `else if` checking if the player decides to go down the path
1. Make a new line in the body of the `else if`, at the bottom
1. There, set the `keepGoing` variable to `false`

Run the program again, and verify that it is possible to exit the loop when choosing to go down the path! The player should now be able to win or lose based on what they do prior to going down the path.

The code for this part should look like this:

```cs
else if (go == "path")
{
    /* ... */
    keepGoing = false;
}
```

Now the game is starting to feel a bit more game-y. There are different outcomes in a more long term way.

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
    bool keepGoing = true;

    while (keepGoing)
    {
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
        Console.WriteLine("You walk down the path and face the monster.");
        health = health - 5;
        keepGoing = false;
      }
      else
      {
        Console.WriteLine("Invalid option.");
      }
    }
    
    if (health < 1)
    {
      Console.WriteLine("You have died.");
    }
    else
    {
      Console.WriteLine("You make it out of the woods.");
    }
  }
}
```