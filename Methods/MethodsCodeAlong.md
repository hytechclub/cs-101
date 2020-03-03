## Code-Along
### 1 - Basic Code
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

### 2 - Making the Code into a Method
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

### 3 - Updating the Method
This illustrates the usefulness of methods

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