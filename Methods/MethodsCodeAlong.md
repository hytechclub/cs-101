# Methods Code-Along
Build a simple program to draw bunnies to the C# console using methods.

## Part 1 - Basic Code
Start by adding `Console.WriteLine` statements to draw an ASCII art bunny in the `Main` method. The bunny should look something like this:

```
() ()
(* *)
(u u)
```

### Code
```cs
using System;
					
public class Program
{
	public static void Main()
	{
		Console.WriteLine();
		Console.WriteLine(" () ()");
		Console.WriteLine(" (* *) ");
		Console.WriteLine(" (u u) ");
		Console.WriteLine();
	}
}
```

## Part 2 - Making the Code into a Method
Next, _define_ a new method named `drawBunny`. The body of the `drawBunny` method should contain the code that prints the bunny to the console. Once the method has been defined, remove the code from the `Main` method. Instead of using the `Console.WriteLine` statements in the `Main` method, _call_ the `drawBunny` method a few times.

### Code
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
		Console.WriteLine(" (* *) ");
		Console.WriteLine(" (u u) ");
		Console.WriteLine();
	}
}
```

## Part 3 - Updating the Method
Now, if there is some change required to the bunny drawing, it is easy to change it! Update the method so that the bunny has dots for eyes instead of stars. 

### Code
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