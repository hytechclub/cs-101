# User Input Recap
```cs
string userResponse = Console.ReadLine();
```

The computer waits until the user has type in any text and an enter key. `Console.ReadLine` will then return the text provided, as a string value.

In this example, we choose to store the string as the value of the variable `userResponse`. 

If we want to store the data returned as a variable who's datatype is not a string, then we need to convert it the desired datatype, using `Convert.To`.

Here are some examples:

```cs
Console.WriteLine("What is your Age?");	
string ageResponse = Console.ReadLine();
int myAge = Convert.ToInt32(ageResponse);

// the double and bool converts works the same
string baResponse = Console.ReadLine();
double battingAverage = Convert.ToDouble(baResponse);

string snowingResponse = Console.ReadLine();
bool isSnowing = Convert.ToBoolean(snowingResponse);
```

In the `int` example, we have a `string` variable, `ageResponse`, that we need to convert to an integer. Suppose we want to do math with the value, we will need a datatype, like an `int`, to be able to do it. So we pass the string to `Convert.ToInt32`, and it returns an integer value if it can. Above we can see, the returned `int` is stored in a new variable, `myAge`. We have to use a different variable, because the datatype is not string!