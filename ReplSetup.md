# Repl Setup for <span>C#</span>
Create a `repl.it` account in order to save and share C# projects.

1. Click the "sign up" button on [repl.it](https://repl.it)  
    ![](https://i.imgur.com/auGMhGe.png)
1. Fill out a username, email, and password, and click the "Sign up" button  
    ![](https://i.imgur.com/nXfLkbD.png)
1. If necessary, prove your humanity to verify the account
1. Open your email, and click the "Complete Verification" link  
    ![](https://i.imgur.com/MY2u6o9.png)
1. On your [repls](https://repl.it/repls) page, click the "+ new repl" button  
    ![](https://i.imgur.com/dexmyq8.png)
1. Select "C#" from the Language list
1. Enter a name for the Repl, like "HelloWorld"
1. Click the "Create Repl" button to create the new project!  
    ![](https://i.imgur.com/8c8V8Uy.png)

## Repl Overview
**`repl.it`** is a website that allows developers to _write_ and _run_ code right from a web browser!

![](https://i.imgur.com/7jhKrt9.png)

- **Code Editor** - This is where developers write code
- **Run Button** - Developers click this button to _execute_ the code
- **Run Area** - This is where the developer sees the results of the code

In the new Repl, click the "run" button to see the code _execute_!

### TIP - C# Script Structure
In the code, there is a lot of boiler-plate code that sets up the program. These parts of the code may be outside of the scope of this lesson. All that matters for simple scripts is the code between the `{` and `}` where the `Console.WriteLine` is now. This part is called the **body** of the `Main` method. All the rest can be ignored to start.

```cs
using System;

class MainClass {
	public static void Main (string[] args) {
		// IMPORTANT STUFF GOES HERE
	}
}
```

### TIP - Specific Syntax
Make sure every piece of code is **exactly** correct. C# is very particular, and if one letter is wrong, the whole program could crash.

Here are some basic rules that can help deal with these errors:
- Statements should end with semi-colons (`;`)
- Any text to show the user should have an opening AND a closing quotation mark (`""`)
- Make sure capitalization is consistent
- Make sure parentheses open AND close (`()`)