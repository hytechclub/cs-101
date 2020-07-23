# Hello World!
In this lesson, create a simple application to show a message in the console using C#. **C#** is an object-oriented programming language, often used to make desktop applications.

## Getting Started with a New Repl Account
Follow the [Repl Setup guide](../ReplSetup.md) to create an account and a new Repl project.

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