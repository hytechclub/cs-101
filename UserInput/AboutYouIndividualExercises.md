# About Me - Individual Exercises
Complete each of the exercises below to practice using `Console.ReadLine` and `Convert.ToInt32`.

## 1. More Questions
Ask the user for the following information, and then print it out:
- Phone Number
- Birth Year
- Hometown
- Height in Inches
  - CHALLENGE: Convert the inches given to feet!
- Wears Glasses (true/false)
- GPA

Consider the data type to use for each piece of information. For each one, it should look something like this:

```cs
Console.WriteLine("What is your phone number?");
int phoneNumber = Console.ReadLine();

Console.WriteLine("You can call me at " + phoneNumber);
```

Add as many questions as possible. Note that in some cases, it may be necessary to use `Convert.ToInt32`, but in some cases it may not.

## 2. CHALLENGE: Multiple People
Instead of keeping information about one person, ask the user for information about multiple people. This will be very similar to the original questions, but do not copy and paste! Practicing manually will help build muscle memory and make coding feel more comfortable.

## 3. CHALLENGE: Mad Libs
Create an entirely new Repl project for this challenge. The goal will be to make a project that runs through a [mad libs](https://www.madlibs.com/) story.

### Non-Code Setup
First, prepare a mad libs story on paper.

1. On paper (or in a text file or document), write a short story - it should be a few sentences long
1. Pick a few key words in the story, and replace them with blanks
1. Figure out the part of speech for each replaced word (noun, verb, adjective, etc)

Now the story should be ready for the program!

### Code
Make the story into a playable C# game. Create a new C# Repl Project, and write code that does the following:

1. For each blank in the story, ask the user to input a word of the proper part of speech
1. Store each word in its own variable
1. Display the full story, but replace the blanks with the words in the variables

Run the program. Enter as many words as required, and read the customized story at the end!