# Choose Your Adventure Game - Part 6
For the next part, add a name checker. This code-along covers method parameters and returns.

## Starting Point
For this code-along, start from the ending point of [part five](CodeAlong5.md). If needed, fork [this Repl](https://replit.com/@HylandOutreach/ChooseYourAdventurePartFive) project to begin.

## Defining the Method
Start by _defining_ a new method that will check if a given name is good or not.

1. Make a new line under the `Main` block
    - Make sure to be within the `Program` block still
1. Start with the two words to define a method: `public static`
1. This method should return a true/false value, so put `bool` after
1. Next, put the method name: `NameCheck`
1. After that, put parentheses and curly brackets: `() { }`
1. This method should take in a name, so put `string name` in the parentheses

The code for the basic method definition should look something like this:

```cs
public static bool NameCheck(string name)
{

}
```

### Filling Out the Body
Now it's time to make the method actually do something! It should take the `name` parameter and check if it is a good name. For this game, a good name is either "Wirt" or "Greg".

1. In the body block of the `NameCheck` method, make a new `if`/`else`
1. For the `if` condition (between `(` and `)`), check if `name` is `"Wirt"` or `"Greg"`
1. If the name is Wirt or Greg, `return` a value of `true`
    - This should be in the body of the `if`
1. In all other cases, `return` a value of `false`
    - This should be in the body of the `else`

The code for the full method definition should look something like this:

```cs
public static bool NameCheck(string name)
{
    if (name == "Wirt" || name == "Greg")
    {
        return true;
    }
    else
    {
        return false;
    }
}
```

Note that running the program still will not do anything with this code yet!

## Calling the Method
The next step is to _call_ the `NameCheck` method.

1. Find the part of the code where the `keepGoing` variable is first declared
1. Make a new line under that
1. There, declare a new `bool` variable named `goodName`
1. Set `goodName` to a call of `NameCheck`
1. Pass in the `name` variable to the `NameCheck` call

The code for this part should look something like this:

```cs
bool goodName = NameCheck(name);
```

It still won't do anything new yet, but now the method code is running!

### Using the Result
The last step is to use the result for something interesting. The game should continue if the player has entered a good name, and stop otherwise.

1. Under the `goodName` variable declaration, create an `if`/`else` structure
1. For the `if` condition, use `goodName`
1. If the name is good, write a message to the console saying the name is good
    - This should go in the body of the `if`
1. If the name is no good, write a message saying the player cannot play
1. Also, set the `keepGoing` variable to `false`
    - Both of these should happen in the `else` body

Now, run the program, and verify that it is only possible to continue when a good name is entered! The code for this part should look something like this:

```cs
if (goodName)
{
    Console.WriteLine("That name is good...");
}
else
{
    Console.WriteLine("You cannot play.");
    keepGoing = false;
}
```

## Final Program
By the end of this code-along, the **main.cs** file should look something like this:

```cs
using System;

class Program {
  public static void Main (string[] args) {
    PrintIntro();

    Console.WriteLine("What is your name?");
    string name = Console.ReadLine();
    int health = 5;
    bool keepGoing = true;

    bool goodName = NameCheck(name);

    if (goodName)
    {
      Console.WriteLine("That name is good...");
    }
    else
    {
      Console.WriteLine("You cannot play.");
      keepGoing = false;
    }

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

  public static void PrintIntro()
  {
    Console.ForegroundColor = ConsoleColor.White;
    Console.BackgroundColor = ConsoleColor.DarkRed;
    Console.Clear();

    Console.WriteLine("You awaken in a strange place.");
    Console.WriteLine("You see a barn, a big tree, and a path through the woods.\n");
  }

  public static bool NameCheck(string name)
  {
    if (name == "Wirt" || name == "Greg")
    {
      return true;
    }
    else
    {
      return false;
    }
  }
}
```