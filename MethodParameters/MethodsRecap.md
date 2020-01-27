# Methods Recap
Methods are what we use so that we don't have to repeat sections of code. They allow us to reuse the same code over and over again throughout our program. 

## Defining a Method
When defining a new method we always have to include certain pieces of information.

We start with

```cs
public static
```

These two words will be at the beginning of all the methods you are likely to write in this course.

We follow public static with a return type, this tells other people what kind of information you will return. For instance:

```cs
public static long
```

The `long` above means that this method will return a `long`, meaning if we want to store the result of the method in a new variable, that variable must be of type `long`.

Any type we have learned in this class can be a return type but what if I don't want to return anything?

Not all methods need to return something in this case we would place the word void where we previously had the word long

```cs
public static void
```

You might recognize the `void` terminology from the `main` method in every program you have written thus far.

Next is the method name, we want to use descriptive names that tell a user at a glance what the method does.

```cs
public static double GetPerimeterOfRectangle
```

It should be obvious what `GetPerimeterOfRectangle` will give us a back the perimeter of some rectangle.

How does it know what the dimensions of the Rectangle are?

We have to tell it the dimensions, and we do this by defining the **Method Parameters**

```cs
public static double GetPerimeterOfRectangle(double sideA, double sideB, double sideC, double sideD)
```

Parameters are separated by commas and placed with Parenthesis next to the method name. A method may have any number of parameters including zero. The parameters are the only way to get information from another section of code.

Following the parameters we write the code that will run whenever this method is used inside of `{}`, making sure to use the keyword `return` before the value we want to return if this method returns a value

```cs
public static double GetPerimeterOfRectangle(double sideA, double sideB, double sideC, double sideD)
{
    int perimeter = sideA + sideB + sideC + sided;
    return perimeter;
} 
```

## Calling a Method
Finally when **calling** a method we have to make sure to place an equal number of values in parenthesis to the number of parameters the method accepts.

```cs
public static void Main()
{
    int rectangleSideOne = 4;
    int rectangleSideTwo = 6;
    int rectangleSideThree = 7;   
    int rectangleSideFour = 8;
 
    int perimeter = GetPerimeterOfRectangle(rectangleSideOne, rectangleSideTwo, rectangleSideThree, rectangleSideFour); 
}
```

Methods can be difficult to grasp but stick with it! The more you ask now the easier it will be when we pick this back up!