# Hello World!
In this lesson, create a simple application to show a message in the console using C#. **C#** is a general purpose, multi-paradigm programming language designed by Microsoft. Developers use C# to make web servers, desktop applications, games, and much more.

![](https://preview.redd.it/j0gld2s2skq31.jpg?auto=webp&s=0f76300784177a603a9743a369a5f39be86c1ec4)

## Getting Started with a New Replit Account
Follow the [Replit Setup guide](../ReplitSetup.md) to create an account and a new Repl project.

## Using `Console.WriteLine`
The default code in the new Repl project should look something like this:

```cs
using System;

class MainClass {
  public static void Main (string[] args) {
    Console.WriteLine("Hello World");
  }
}
```

The important line is `Console.WriteLine("Hello World");`. In C#, that line of code will display a message of "Hello World" in the console. Try to change the message from "Hello World" to something else!

## Setting the Console Colors
It is possible to change the colors of the C# console. There is a [limited set](https://docs.microsoft.com/en-us/dotnet/api/system.consolecolor?view=netframework-4.8) of colors, but they can make the console a little bit more fun.

At the top of the body of the `Main` method, add the following code:

```cs
Console.BackgroundColor = ConsoleColor.Cyan;
Console.ForegroundColor = ConsoleColor.DarkBlue;
Console.Clear();
```

This will set the colors, and then clear the existing console so that the colors apply to everything. Make sure the capitalization is consistent!

Try out a few different colors to see what works.