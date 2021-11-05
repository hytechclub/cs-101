# Choose Your Adventure Game - Part 5
For the next part, re-organize some code without changing the functionality of the game. This code-along covers basic methods.

## Starting Point
For this code-along, start from the ending point of [part four](CodeAlong4.md). If needed, fork [this Repl](https://replit.com/@HylandOutreach/ChooseYourAdventurePartFour) project to begin.

Note that for this activity, the game will not change. The code will change, but it will function the same. This is mostly for demonstrative purposes.

## Defining a New Method
Start by _defining_ a new method that will kick things off for the program by setting the colors and printing the messages.

1. Make a new line under the `Main` block
    - Make sure to be within the `Program` block still
1. Start with the three words to define a method: `public static void`
1. Next, put the method name: `PrintIntro`
1. After that, put parentheses and curly brackets: `() { }`

Run the code to make sure it works - it should not do anything different though. The code for this part should look something like this:

```cs
public static void PrintIntro()
{

}
```

## Filling In the Method Body
Next, it's time to make the method do something!

1. Find the line in the `Main` method that sets the foreground to white
1. Find the line in the `Main` method that prints the intro statements
1. Highlight and copy the six lines between
1. Paste the six lines into the body of the `PrintIntro` method
1. Remove the six lines from the `Main` method

Run the program, and verify that the console does not change colors and the opening statements are not printed. This may seem like a step back, but it is necessary to help move things forward.

The code for the method should now look something like this:

```cs
public static void PrintIntro()
{
    Console.ForegroundColor = ConsoleColor.White;
    Console.BackgroundColor = ConsoleColor.DarkRed;
    Console.Clear();

    Console.WriteLine("You awaken in a strange place.");
    Console.WriteLine("You see a barn, a big tree, and a path through the woods.\n");
}
```

## Calling the Method
Now, all that's left is to _call_ the method from the `Main` method. This will make it so that all the code in the body of the method is executed at the beginning of each program run.

1. Find the top of the `Main` method
    - Where the code from the `PrintIntro` body used to be
1. Make a new line
1. Call the method with the method name (`PrintIntro`) followed by parentheses `()`

Run the program, and verify that the console changes colors and the opening statements are printed again! The code should look something like this:

```cs
PrintIntro();
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
}
```