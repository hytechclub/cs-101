# Methods Exercises - Creating a Zoo
After completing the [code-along](MethodsCodeAlong.md) activity, complete the exercises to practice using methods. Use the same Repl project from the code-along. The goal of these exercises is to add several other animals to the program.

## Starter Code
To begin, the code in the **main.cs** file should look something like this:

```cs
using System;

public class Program
{
    public static void Main()
    {
        drawBunny();
        drawBunny();
        drawBunny();
    }

    public static void drawBunny()
    {
        Console.WriteLine();
        Console.WriteLine(" () ()");
        Console.WriteLine(" (. .) ");
        Console.WriteLine(" (u u) ");
        Console.WriteLine();
    }
}
```

Here, there are two method definitions: `Main` and `drawBunny`. The `drawBunny` method is _called_ within the body of the `Main` method. Note the placement of the curly brackets:

```cs
using System;

public class Program
{
    // All important stuff is in this class block
}
```

```cs
public static void Main()
{ // open
    drawBunny();
    drawBunny();
    drawBunny();
} // close

public static void drawBunny()
{ // open
    Console.WriteLine();
    Console.WriteLine(" () ()");
    Console.WriteLine(" (. .) ");
    Console.WriteLine(" (u u) ");
    Console.WriteLine();
} // close
```

Every additional method should be defined within the same class block, but outside of the other method blocks.

## 1. Drawing a Cat
Define and call a new method in the program that prints a cat to the console. The method should be named `drawCat`.

### Defining the Method
The first step is _defining_ the `drawCat` method.

1. Find the place in the code _under_ the closing `}` for the `drawBunny` method, _above_ the closing `}` for the class block
1. There, add the three keywords needed to define a basic method:
    - `public static void`
1. After that, make a space and add the name of the method:
    - `drawCat`
1. After that, add the opening and closing parentheses: `()`
1. Make a new line
1. Add the opening and closing curly brackets: `{}`
1. Press enter between them to open up the _body_ of the method
1. In the body (between the curly brackets), add code to draw a cat:  
    ```cs
    Console.WriteLine();
    Console.WriteLine(" /\\_/\\");
    Console.WriteLine("( o.o )");
    Console.WriteLine(" > ^ <");
    Console.WriteLine();
    ```

Now the method should be properly defined! But the program won't do anything new yet...

### Calling the Method
To actually use a method after it has been defined, it must be _called_ in the code.

1. Find the body of the `Main` method (between the curly brackets)
1. At the bottom, make a new line (above the closing `}`)
1. Type in the name of the method: `drawCat`
1. After that, type in opening and closing parentheses: `()`
1. Add a semi-colon to end the statement
1. Use the same code to call the method two more times

Run the program, and three cats should appear!

## 2. Drawing a Dog
Define and call a new method in the program that prints a dog to the console. The method should be named `drawDog`. This will be incredibly similar to the `drawCat` method - the only difference is the name of the method, and the text printed to the console.

### Defining the Method
The first step is _defining_ the `drawDog` method.

1. Find the place in the code _under_ the closing `}` for the `drawCat` method, _above_ the closing `}` for the class block
1. There, add the three keywords needed to define a basic method
1. After that, make a space and add the name of the method
1. After that, add the opening and closing parentheses
1. Make a new line
1. Add the opening and closing curly brackets
1. Press enter between them to open up the _body_ of the method
2. In the body, add code to draw a dog:  
    ```cs
    Console.WriteLine();
    Console.WriteLine("  __      _");
    Console.WriteLine("o'')}____//");
    Console.WriteLine(" `_/      )");
    Console.WriteLine(" (_(_/-(_/ ");
    Console.WriteLine();
    ```

Now the method should be properly defined! But the program won't do anything new yet...

### Calling the Method
To actually use a method after it has been defined, it must be _called_ in the code.

1. Find the body of the `Main` method 
1. At the bottom, make a new line
1. Type in the name of the method
1. After that, type in opening and closing parentheses
1. Add a semi-colon to end the statement
1. Use the same code to call the method two more times

Run the program, and three dogs should appear!

## 3. Drawing More Animals
Following the steps from the exercises above, define and call some new methods that draw new animals. Each student should have an opportunity to complete one of the parts below. The name of the method, along with the code for the _body_ of the method, is provided for each animal below.

### `drawFish` Method
```cs
Console.WriteLine();
Console.WriteLine("  _");
Console.WriteLine("><_>");
Console.WriteLine();
```

### `drawElephant` Method
```cs
Console.WriteLine();
Console.WriteLine("     __");
Console.WriteLine(" .--()°'.'");
Console.WriteLine("'|, . ,'");
Console.WriteLine(" !_-(_\\");
Console.WriteLine();
```

### `drawBat` Method
```cs
Console.WriteLine();
Console.WriteLine("   _   ,_,   _");
Console.WriteLine("  / `'=) (='` \\");
Console.WriteLine(" /.-.-.\\ /.-.-.\\"); 
Console.WriteLine(" `      '       `");
Console.WriteLine();
```

### `drawOwl` Method
```cs
Console.WriteLine();
Console.WriteLine(" ,_, ");
Console.WriteLine("(O,O)");
Console.WriteLine("(   )");
Console.WriteLine("-m-m-");
Console.WriteLine();
```

### `drawDuck` Method
```cs
Console.WriteLine();
Console.WriteLine("  __     ");
Console.WriteLine("<(o )___ ");
Console.WriteLine(" ( ._> / ");
Console.WriteLine("  `---'  ");
Console.WriteLine();
```