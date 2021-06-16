# Method Parameters Exercises
After completing the [calculator](CalculatorIndividualInstructions.md), work on these exercises to practice using method parameters and returns.

## Setup
1. Create a [new Repl project](https://replit.com/new/csharp)
1. Name the project "Parameters Practice"
1. Print a welcome message saying "Parameters Practice"

Now the **main.cs** file should be ready to go. For each exercise, the goal will be to _define_ a method in the class body (outside of the `Main` method body, inside of the `MainClass` body), and then _call_ the method from within the body of the `Main` method. It may seem somewhat tedious, but it should help with retention.

Code solutions are available for several of the exercises, but try to complete them before checking.

## 1. Emphasis
For this exercise, create a method that puts an emphasis on some text by surrounding the text with greater-than and less-than signs. For example, if the text were `"This is Important"`, the result would be `">This is Important<"`.

### Defining the Method
Start by finding the proper place in the code to _define_ the method. It should be under the `}` from the `Main` method body, above the `}` from the class block. Once there, add code to define the method.

#### Method Information
- Name: `emphasize`
- Return type: `string`
- Parameters: `string text`

#### Steps
1. Start with the `public` keyword
1. Add the `static` keyword
1. Next, add the return type
1. After that, the method name, followed by parentheses
1. Between the parentheses, add any parameters
1. Make a new line
1. Add curly brackets, and press **Enter** between them to make some space
1. In the _body_ of the method (between the curly brackets), add a `return`
1. Return the following things added together:
    - `">"`
    - `text`
    - `"<"`

<input type="checkbox" id="reveal1" class="reveal-checkbox" />

<label for="reveal1" class="reveal-label">Click to Reveal Code</label>

```cs
public static string emphasize(string text)
{
    return ">" + text + "<";
}
```

### Calling the Method
Now the method has been defined, but it is not actually doing anything yet. It's time to _call_ the method. Start by finding the body of the `Main` method (between its curly brackets), and making some space. Once there, add some code to call the method and handle the result.

1. Create a new `string` variable named `newText`
1. Set `newText` to equal a call to the `emphasize` method
1. Pass in `"This is Important"` as the argument for the `emphasize` method
1. Under that, add a `Console.WriteLine` statement
1. Make the `WriteLine` print out the `newText` variable

Run the code, and verify that the properly emphasized text appears in the console!

<input type="checkbox" id="reveal2" class="reveal-checkbox" />

<label for="reveal2" class="reveal-label">Click to Reveal Code</label>

```cs
string newText = emphasize("This is Important");
Console.WriteLine(newText);
```

## 2. Millionaire Check
For this exercise, create a method that checks if someone has over a million dollars in the bank. For example, if the amount were `9987754.00`, the result would be `"You are a millionaire!"`. If the amount were `890283.00`, the result would be `"You are poor :("`.

### Defining the Method
Start by finding the proper place in the code to _define_ the method. It should be under the `}` from the previous method body, above the `}` from the class block. Once there, add code to define the method.

#### Method Information
- Name: `millionCheck`
- Return type: `string`
- Parameters: `double amount`

#### Steps
1. Start with the `public` keyword
1. Add the `static` keyword
1. Next, add the return type
1. After that, the method name, followed by parentheses
1. Between the parentheses, add any parameters
1. Make a new line
1. Add curly brackets, and press **Enter** between them to make some space
1. In the _body_ of the method (between the curly brackets), create an `if`/`else` structure
1. For the `if` condition, check if `amount` is greater than or equal to `1000000.00`
1. In the body of the `if`, `return` a message saying `"You are a millionaire!"`
1. In the body of the `else`, `return` a message saying `"You are poor :("`

<input type="checkbox" id="reveal3" class="reveal-checkbox" />

<label for="reveal3" class="reveal-label">Click to Reveal Code</label>

```cs
public static string millionCheck(double amount)
{
    if (amount >= 1000000.00)
    {
        return "You are a millionaire!";
    }
    else
    {
        return "You are poor :(";
    }
}
```

### Calling the Method
Now the method has been defined, but it is not actually doing anything yet. It's time to _call_ the method. Start by finding the body of the `Main` method (between its curly brackets), and making some space. Once there, add some code to call the method and handle the result.

1. Create a new `string` variable named `millionaire`
1. Set `millionaire` to equal a call to the `millionaireCheck` method
1. Pass in `10.00` as the argument for the `millionaireCheck` method
1. Under that, add a `Console.WriteLine` statement
1. Make the `WriteLine` print out the `millionaire` variable

Run the code, and verify that the proper message appears in the console!

<input type="checkbox" id="reveal4" class="reveal-checkbox" />

<label for="reveal4" class="reveal-label">Click to Reveal Code</label>

```cs
string millionaire = millionCheck(10.00);
Console.WriteLine(millionaire);
```

## 3. Bitcoin to Dollars
>Note: This exercise provides a little less guidance, but it should be very similar to the previous exercises

For this exercise, create a method that converts Bitcoin to Dollars. For the purposes of this activity, use a conversion rate of `44000`. For example, if the amount were `1.1` bitcoin, the result would be `48400` dollars.

### Defining the Method
Start by finding the proper place in the code to _define_ the method. It should be under the `}` from the previous method body, above the `}` from the class block. Once there, add code to define the method.

- Name: `btcToDollars`
- Return type: `double`
- Parameters: `double btcAmount`
- Return: the `btcAmount` parameter multiplied by `44000`

<input type="checkbox" id="reveal5" class="reveal-checkbox" />

<label for="reveal5" class="reveal-label">Click to Reveal Code</label>

```cs
public static double btcToDollars(double btcAmount)
{
    return btcAmount * 44000;
}
```

### Calling the Method
Now the method has been defined, but it is not actually doing anything yet. It's time to _call_ the method. Start by finding the body of the `Main` method (between its curly brackets), and making some space. Once there, add some code to call the method and handle the result.

- Variable name to store the result: `dollars`
- Argument to pass: `0.0001`
- Print: `"You have $"` + the result

Run the code, and verify that the proper message appears in the console!

<input type="checkbox" id="reveal6" class="reveal-checkbox" />

<label for="reveal6" class="reveal-label">Click to Reveal Code</label>

```cs
double dollars = btcToDollars(0.0001);
Console.WriteLine("You have $" + dollars);
```

## 4. Kelvin to Celsius
>Note: This exercise provides a little less guidance, but it should be very similar to the previous exercises

For this exercise, create a method that converts a temperature in Kelvin to Celsius. For the purposes of this activity, Celsius can be Kelvin minus `273`. For example, if the temperature were `290` in Kelvin, the result would be `17` in Celsius.

### Defining the Method
Start by finding the proper place in the code to _define_ the method. It should be under the `}` from the previous method body, above the `}` from the class block. Once there, add code to define the method.

- Name: `kelvinToCelsius`
- Return type: `int`
- Parameters: `int kTemp`
- Return: the `kTemp` parameter minus `273`

<input type="checkbox" id="reveal7" class="reveal-checkbox" />

<label for="reveal7" class="reveal-label">Click to Reveal Code</label>

```cs
public static int kelvinToCelsius(int kTemp)
{
    return kTemp - 273;
}
```

### Calling the Method
Now the method has been defined, but it is not actually doing anything yet. It's time to _call_ the method. Start by finding the body of the `Main` method (between its curly brackets), and making some space. Once there, add some code to call the method and handle the result.

- Variable name to store the result: `cTemp`
- Argument to pass: `295`
- Print: `"The temperature is "` + the result

Run the code, and verify that the proper message appears in the console!

<input type="checkbox" id="reveal8" class="reveal-checkbox" />

<label for="reveal8" class="reveal-label">Click to Reveal Code</label>

```cs
int cTemp = kelvinToCelsius(295);
Console.WriteLine("The temperature is " + cTemp);
```

## 5. Inches to Feet
>Note: This exercise does not have a code solution

For this exercise, create a method that converts a height in inches to feet. For example, if the height were `61` in inches, the result would be `5.08` in feet.

### Defining the Method
Start by finding the proper place in the code to _define_ the method. It should be under the `}` from the previous method body, above the `}` from the class block. Once there, add code to define the method.

- Name: `inchesToFeet`
- Return type: `double`
- Parameters: `int inches`
- Return: the `inches` parameter divided by `12.0`

### Calling the Method
Now the method has been defined, but it is not actually doing anything yet. It's time to _call_ the method. Start by finding the body of the `Main` method (between its curly brackets), and making some space. Once there, add some code to call the method and handle the result.

- Variable name to store the result: `height`
- Argument to pass: `63`
- Print: `"You are "` + the result + `" feet tall"`

Run the code, and verify that the proper message appears in the console!

## 6. Exclaim
>Note: This exercise does not have a code solution

For this exercise, create a method that adds a bunch of exclamation points to a message. For example, if the message were `"Hello"`, the result would be `"Hello!!!!!"`.

### Defining the Method
Start by finding the proper place in the code to _define_ the method. It should be under the `}` from the previous method body, above the `}` from the class block. Once there, add code to define the method.

- Name: `exclaim`
- Return type: `string`
- Parameters: `string message`
- Return: the `message` parameter plus `"!!!!!"`

### Calling the Method
Now the method has been defined, but it is not actually doing anything yet. It's time to _call_ the method. Start by finding the body of the `Main` method (between its curly brackets), and making some space. Once there, add some code to call the method and handle the result.

- Variable name to store the result: `yelling`
- Argument to pass: `hey`
- Print: the `yelling` variable

Run the code, and verify that the proper message appears in the console!

## Challenges
After completing these exercises, try to work on the [challenges](MethodsChallenges.md).