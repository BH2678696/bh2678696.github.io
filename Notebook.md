# My Coding Notebook

## Table of Contents
- [Flutter Notes](#flutter-notes)
  - [What is Flutter?](#what-is-flutter)
  - [Key Terms](#key-terms-and-definitions)
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
| Column           |                        vertical layout                          |                                           |
| Row              |                        horizontal layout                          |                                           |
| Container        |                        wraps content with padding, margin, or color                          |                                           |
| Text             |                     displays text                             |                                           |
| Image.network    |                        displays images from a URL                          |                                           |
| Padding           |                      adds space around a widget                            |                                           |
| Center           |                           centers its child                       |                                           |
| main()           |                         The function that runs the app                        |                    Found in main.dart                       |
---


### 🎨 Layout and Design Widgets
- How do you center a widget?
- How do you align something to the left or right?
- What widget adds space around content?


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
