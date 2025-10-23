# My Coding Notebook

## Table of Contents
- [Flutter Notes](#flutter-notes)
  - [What is Flutter?](#what-is-flutter)
  - [Key Terms](#key-terms-and-definitions)
  - [Layout and Design Widgets](#layout-and-design-widgets)
  - [Flutter Definitions with Structures](#flutter-definitions-with-structures)
- [Code Definitions](#code-definitions)
- [Notebook Style Guide](#markdown-style-guide-for-coding-notebooks)

## Flutter Notes

### What is Flutter?
- Definition: A framework made by Google for building apps that work on web, Android, and iOS- with one codebase. 
- Why is it useful? It saves lots of time and money because you write the code and build the app one time and it displays on all three.

---

### Key Terms and Definitions

| Term             | Definition                                      | Example / Notes                          |
|------------------|--------------------------------------------------|-------------------------------------------|
| Widget           |                          Basic building block of a Flutter app. Everything is a widget.                        |                    Text, Image, Container, Column                       |
| MaterialApp      |                         The root of the app. Sets up routes and themes.                         |                  Found in main.dart                         |
| Scaffold         |                        Provides basic visual layout- like a header, body, floating button                          |                     Each screen uses it                      |
| StatelessWidget  |                       A widget that doesn't change                           |                     Most of screen files                      |
| Named Routes  |               Predefined paths to navigate between screens                                   |                   '/', '/page2', '/page3', etc.                        |
| StatefulWidget   |                      A widget that can change over time                            |                      Used in MyHomePage()                     |
| Navigator        |                         Manages screen transitions                         |                   Navigator.pushedNamed(context, '/page2');                        |
| AppBar           |                       Top navigation bar                           |                  Title of each page appears here                         |
| Column           |                        vertical layout                          |                     A list of things                      |
| Row              |                        horizontal layout                          |                    Describing the column (giving the information)                       |
| Container        |                        wraps content with padding, margin, or color                          |                     Borders to images                      |
| Text             |                     displays text                             |                    Text you see on the screen                       |
| Image.network    |                        displays images from a URL                          |                       Dog images in the flutter app                    |
| Padding           |                      adds space around a widget                            |                     Space around the image                      |
| Center           |                           centers its child                       |                     Center texts and images                      |
| main()           |                         The function that runs the app                        |                    Found in main.dart                       |

---


### Layout and Design Widgets
- How do you center a widget?
- How do you align something to the left or right?
- What widget adds space around content?


## Flutter Definitions with Structures

| Term | Definition and Description | Base Structure | Real Life Example | App Example |
|------|----------------------------|----------------|-------------------|-------------|
|   main()   | A function that runs when your app starts. It tells Flutter what app to show. | `void main() => runApp(MyApp());` | Opening an app on your phone | in main.dart, void main() => runApp(MyPortfolioApp()); |
|   MaterialApp   | The widget that sets up your whole app’s look and navigation. | `MaterialApp(...)` | The code that sets the graphics | in main.dart, return MaterialApp \n debugShowCheckedModeBanner: false, \n title: 'TSA Portfolio',|
|   Scaffold   | A widget that gives you the basic layout: background, navigation bar, floating button, etc. | `Scaffold(...)` | Base app structure |in showcase.dart, return Scaffold( \n body: Column( |
|   Column   | A widget that holds and displays your content in a straight line from top to bottom. | `Column(...)` | A list | in showcase.dart, body: Column( \n mainAxisAlignment: MainAxisAlignment.start, |
|   Row   | A widget that shows things side-by-side. | `Row(...)` | Defining or explaining the column | in infocard.dart, child: Row( \n children: [ \n ClipRRect( |
|   Container   | A box that holds other widgets. You can add color, padding, borders, or size. | `Container(...)` | Borders of pictures | in infocard.dart, return Container( \n margin: const EdgeInsets.symmetric(vertical: 8, horizontal: 16), |
|   Text   | A widget to display text on the screen. | `Text('Hello')` | Words on the screen | in infocard.dart, child: Text( \n description, \n style: const TextStyle(color: Colors.white), |
|   Image.network   | A widget to show an image using a link from the internet. | `Image.network('https://...')` | User's profile pictures | in infocard.dart, child: Image.network(imageUrl, width: 100, height: 100, fit: BoxFit.cover), |
|   ElevatedButton   | A clickable button that floats above content. You choose what happens when it's clicked. | `ElevatedButton(onPressed: ..., child: ...)` | The button | in showcase.dart, ElevatedButton( \n onPressed: () => Navigator.pushNamed(context, '/alt'), \n child: const Text('Alternate Design'), |
|   onPressed   | The code that gets run when a button is tapped or something happens. | `onPressed: () => doSomething()` | What happens when you click a button | in showcase.dart,  onPressed: () => Navigator.pushNamed(context, '/alt'), \n child: const Text('Alternate Design'), |
|   StatelessWidget   | A class that creates widgets that never change. Good for static screens. | `class HomeScreen extends StatelessWidget` | Home Screen / Profile Page | in showcase.dart, class ShowcaseScreen extends StatelessWidget { \n const ShowcaseScreen({super.key}); |
|   StatefulWidget   | A class for widgets that can change while the app is running. | `class MyWidget extends StatefulWidget` | Like a game where the it changes (ping pong) | not found in the app (nothing in this app changes) |
|   Navigator   | Lets you move from one screen to another using route names. | `Navigator.pushNamed(context, '/about')` | Tapping on a user's profile to get to their page | in showcase.dart, Navigator.pushNamed(context, '/alt'), |
|   Padding   | Makes space around a widget inside its container. | `Padding(padding: EdgeInsets.all(8.0), child: ...)` | Adding space between posters | in showcase.dart, return Padding( \n padding: const EdgeInsets.all(4.0), |
|   Center   | Aligns content in the center of the screen or container. | `Center(child: ...)` | Put a poster on the center |in showcase.dart, textAlign: TextAlign.center,  |
|   Wrap   | Automatically puts widgets onto a new line when there's no space. | `Wrap(children: [...])` | Writing in google docs and it goes to the next line | in showcase.dart, Wrap(alignment: WrapAlignment.center, children: puppyUrls.map((url) => puppyImage(url)).toList()), |
|   @override   | This marks a method as one that’s replacing a method in a parent class. | `@override` | Modifying a game such as changing a character's ability (make them jump higher or run faster) | in showcase.dart, @override \n Widget build(BuildContext context) { \n final List<String> puppyUrls = [ |
|   Build   | Required in every widget class to describe what to show. | `build` | The plan to build a car | in showcase.dart, Widget build(BuildContext context) { \n final List<String> puppyUrls = [ |
|   BuildContext   | A variable that helps the widget know where it is and lets it communicate with the app. | `BuildContext context` | You're in class and you know where you have been already and where you need to go next | in showcase.dart, build(BuildContext context) |
|   Super.key   | A keyword used to pass a value to the parent widget. | `super.key` | Reordering items in a to-do list | in showcase.dart, const ShowcaseScreen({super.key}); |
|   Const   | A keyword that means the value won't change and is set once. | `const` | Fixed texts and icons | in showcase.dart, const ShowcaseScreen({super.key}); |


## Code Definitions

| Term | Definition | Base Structure / Syntax | Real Life Example | App Example |
|------|------------|--------------------------|-------------------|-------------|
|   Variable   | A named container used to store a value that may change. | `var x = 5;` | XP/Points in a game, X Y Z Values | in main.dart, debugShowCheckedModeBanner: false, |
|   Constant   | A fixed value that cannot change once set. | `const PI = 3.14;` | Configuration settings | in main.dart, appBarTheme: const AppBarTheme( |
|   Data Type   | The kind of value a variable holds, like numbers or text. | `int`, `String`, `bool` | Numbers, letters, characters | in showcase.dart, Widget puppyImage(String url) { |
|   String   | A sequence of characters used to represent words or text. | `"Hello World"` | Texts on our phones | in showcase.dart, Widget puppyImage(String url) { |
|   Integer   | Whole number values. | `int age = 16;` | 1, 2, 3, 4... | in background.dart, const SizedBox(height: 8), |
|   Double   | Number values with decimals. | `double age = 16.2;` | 1.1, 1.2, 1.3, 1.4... | none found |
|   Boolean   | A value that can be true or false. | `bool isLoggedIn = false;` | Lights (on and off) | in main.dart, debugShowCheckedModeBanner: false, |
|   List   | A collection of values in a specific order. | `List<String> names = [];` | Real life lists | in showcase.dart, final List<String> puppyUrls = [ |
|   Null   | A special value that means “nothing.” | `String? name = null;` | New contant with no name yet, empty schedule | none found |
|   Function   | A reusable block of code that performs an action. | `void sayHi() { print("Hi"); }` | Typing on a keyboard | in main.dart, class MyPortfolioApp extends StatelessWidget { |
|   Parameter   | The information passed into a function to change how it works. | `greet(String name)` | Entering your username and password | in main.dart, debugShowCheckedModeBanner: false, |
|   Return   | The result a function gives back. | `return total;` | An error screen/code or getting an answer out of a calculation| in main.dart, return MaterialApp( |
|   Scope   | Where a variable or function can be used. | (No set syntax — concept-based) | IDs, gift cards, passwords, etc. | in main.dart, void main() => runApp(MyPortfolioApp()); |
|   Class   | Blueprint for creating objects with specific structure and behavior. | `class Dog {}` | Everything | in main.dart, class MyPortfolioApp extends StatelessWidget { |
|   Object   | A specific version of a class. | `Dog myDog = Dog();` | Template for creating objects | in main.dart, appBarTheme: const AppBarTheme( |
|   Property   | A variable that belongs to a class/object. | `String name;` | What shirt you're wearing or what's in your backpack | in main.dart, displayLarge: TextStyle(fontSize: 36, color: Colors.white, fontWeight: FontWeight.bold), |
|   Method   | A function that belongs to a class. | `void bark() {}` | What a student chooses to do (like stand up, read, listen etc.) | in main.dart (build is in MyPortfolioApp), Widget build(BuildContext context) { |
|   Constructor   | A special function used to set up a class when it’s created. | `Dog(this.name);` | Creating a new account in a social media app / Creates a thing| in main.dart (Class name followed by parentheses like HomeScreen()), '/': (context) => const HomeScreen(), |
|   Abstraction   | Hiding the inner workings of code so users only interact with what they need. | (Concept — not specific code) | Typing on a keyboard because what you're typing is binary. | All the code in the app because every pixel/picture we see is based on the code behind it. |
|   Override   | Changing how a built-in or inherited function behaves. | `@override` | Modifying a game such as changing a character's ability (make them jump higher or run faster) | in main.dart, @override \n Widget build(BuildContext context) { |
|   Void   | A function that does not return a value. | `void printMessage() {}` | Turning on the light (you don't need anything else besides the light turning on) | in main.dart, void main() => runApp(MyPortfolioApp()); |
|   Scanner   | Creates a scanner object to take input from user | Scanner in = new Scanner(System.in); |  |  |
|   import Scanner   | Gives access to Scanner class, required at top | import java.util.Scanner; |  |  |
|   print line statement   | prints the content in the parenthesis, adds line after | System.out.println(""); |  |  |
|   print statement   | prints the content in the parenthesis | System.out.print(""); |  |  |
|   input nextLine   | reads in a String from the user | input.nextLine(); |  |  |
|   input nextInt   | reads in an int from the user | input.nextInt(); |  |  |
|   input nextDouble   | reads in a double (decimal) from the user | input.nextDouble(); |  |  |
|   input nextBoolean   | reads in a boolean (true/false) from the user | input.nextBoolean(); |  |  |





## Markdown Style Guide for Coding Notebooks

Follow this guide to keep your coding notebook **clear, consistent, and professional**.  
This ensures your notes are easy for you (and others) to read later.

---

## 🔹 Headings
**When to use:** Organize your notebook into sections (like days, topics, or projects).  
- `#` for the notebook title (use once at the top).  
- `##` for each day or major topic.  
- `###` for subsections (like "Notes", "Practice", "Reflections").  


✅ Example:

# My Coding Notebook
## Day 1
### Notes
### Practice
🔡 Text Formatting
When to use: Highlight important ideas or add emphasis.

Use bold for key terms or definitions.

Use italic for emphasis or side comments.

Use inline code for keywords, functions, or commands.

✅ Example:

**Class** = a blueprint for objects  
*Remember:* always test your code  
Use `System.out.println()` to print
💻 Code Blocks
When to use: Anytime you write multiple lines of code.

Inline code for short snippets.

Fenced code blocks with language for full examples.

✅ Example:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello World!");
    }
}
```
🧾 Lists
When to use: Organize steps, notes, or key points.

Numbered lists for sequences or steps.

Bulleted lists for unordered ideas.

✅ Example:

markdown
Copy code
1. Define the class
2. Write the main method
3. Test your program

- Variables
- Loops
- Conditionals
✅ Checklists
When to use: Track progress on assignments or tasks.

✅ Example:

- [x] Complete coding warm-up
- [ ] Finish project draft
- [ ] Reflect on learning
➡️ Blockquotes
When to use: Call out notes, reminders, or teacher comments.

✅ Example:

> 💡 Remember: Loops repeat code until a condition is false.
📊 Tables
When to use: Compare values, track progress, or organize data neatly.

✅ Example:

| Task        | Status   | Notes          |
|-------------|----------|----------------|
| Homework 1  | Done ✅  | Submitted      |
| Homework 2  | Pending  | Needs review   |
🔗 Links & Images
When to use: Add references, resources, or visuals.

✅ Example:

[Java Docs](https://docs.oracle.com/javase/8/docs/api/)  
![Markdown Logo](https://upload.wikimedia.org/wikipedia/commons/4/48/Markdown-mark.svg)
📂 Collapsible Sections
When to use: Hide solutions, extended notes, or extra details.

✅ Example:

<details>
  <summary>Click to reveal solution</summary>
  
System.out.println("Answer: 42");

</details>
📝 Footnotes
When to use: Add references or side notes without cluttering the page.

✅ Example:

This concept is related to object-oriented programming.[^1]

[^1]: See "Objects and Classes" in your textbook.
🎯 Style Rules
Consistency matters more than creativity

Always use headings to structure your notes.

Always use code blocks for multi-line code.

Clarity first

Bold key terms.

Use lists instead of long sentences when outlining steps.

Professional tone

Don’t mix casual notes with formal work in the same section.

Use blockquotes for reflections or teacher feedback.

Track your learning

Use checklists to mark what’s done.

Use collapsible sections if you want to hide answers until review time.

✅ Bottom Line:

Headings = Structure

Bold/Italic = Emphasis

Code blocks = Code

Lists = Steps/Ideas

Tables = Organization

Checklists = Progress

Blockquotes = Notes/Tips

Collapsible = Hide/Show detail

Keep it simple, consistent, and clear.
