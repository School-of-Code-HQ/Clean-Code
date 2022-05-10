# Styling and Formatting Guide

<img src="images/soclogo.png"  width="150" height="150">

## Table of Contents

1. [Introduction](#introduction)
2. [Naming Conventions](#Naming_Conventions)
3. [Indentation & Spcacing](#Indentation_And_Spacing)
4. [Brackets & Colons](#objects-and-data-structures)
5. [Comments](#classes)
6. [Code Formatter](#Code_formatters)

## Introduction

In this article, we will look at how to format your code and why it's important.
\
Code Formatting is not necessary for functionality but well formatted code is easier to read not just by you but other developers. It can also help make errors in your code more obvious.
\
Good code should be self-explanatory, easy to understand and easy to change or extend.

## **Naming Conventions**

### Always use meaningful and descriptive names for variables and functions.

#### Function Names

**Bad:**

![variable_not_on_line](images/namingCodeBad.png)

**Good:**

![variable_not_on_line](images/namingCodeGood.png)

#### Variable Names

**Bad:**

![variable_not_on_line](images/variableNameBad.png)

**Good:**

![variable_not_on_line](images/variableNameGood.png)

**[⬆ back to top](#table-of-contents)**

## **Indentation-And-Spacing**

Always remember code is read more than they are written. Your code will run without indentation and spacing but it does makes your code easier to read and can help with finding errors in your code easier.

Below are some examples of how indentation and spacing is used with JavaScript. (CHECK WORDING)

### Variables

Variables should always start on the same line.

**Bad Indentation:**

![variable_not_on_line](images/variableNewLine.png)

**Good Indentation:**

![variable_not_on_line](images/variableOnsameLine.png)

### Functions

Also functions of the same level should alwasys start on the same line and keep spacing constant when writing code.

**Bad Indentation:**

![variable_not_on_line](images/adIndentation%20funtion.png)

**Good Indentation:**

![variable_not_on_line](images/goodIndentationFunction.png)

**Bad Spacing:**

![variable_not_on_line](images/bdFunct.png)

**Good Spacing:**

![variable_not_on_line](images/goodspacing.png)

## **Brackets-And-Semi_Colons**

### Brackets

There are three main types of brackets in javascript. They are parenthesis, square brackets and curly brackets. This section shows what they do and how you can use them.

#### Parenthesis ()

Parenthesis are mostly used to define function parameters but in some cases can also be used to define orders of evaluatin.

##### As you can see in the example below the parameters of the function are put in a parenthesis

When a function has a parameter it makes the function reuseable.

![variable_not_on_line](images/parenthesisFunction.png)

##### Parenthesis also define order of evaluation in calculations.

![variable_not_on_line](images/Parenthesis.png)
As you can see in the example above it evaluates 2+3 first (5) and then multiplies by 4 = 20.

##### Lastly, Parenthesis are required in For and While loops

The example below shows how parenthesis are used in both for and while loops.

For loop:
![variable_not_on_line](images/forloop.png)

While loop:
![variable_not_on_line](images/whileloop.png)

#### Square Brackets

Square brackets are often use to define an array and also get items from an array.

The examples below shows how square brackets are used in javascript.

Defining an Array:
![variable_not_on_line](images/array.png)

Getting an item in an Array:
![variable_not_on_line](images/arrayItem.png)

**[⬆ back to top](#table-of-contents)**

## **Comments**

### How to leave comments like a pro!

Comments save time, help other developers navigate through your code and help your future self understand what you had written.\
This is espically true when you are learning, although less is more when it comes to comments, as good code should be self-documenting.
\
In JavaScript — Create a single-line comment with // and multi-line comments using /_ and _/
\

#### As you can see from the examples below, comment overkill can be overwhelming and take to long to read through and understand.

**Bad:**

![variable_not_on_line](images/commentCodeBad.png)

**Good:**

![variable_not_on_line](images/commentCodeGood.png)

**[⬆ back to top](#table-of-contents)**

## **Code Formatters**

Code formatters automatically format code for you depending on the preferences you set.
Automatic formatting enables higher code quality, especially when you are working in teams and other people are reading the code you’ve written.
\
Many developers maintain standards of code formatting like 2-space or 4-space indentation or using single or double quotes. This helps with both readbility and finding errors.
\
One such formatter is Prettier.
\

#### Step 1 — Install the extension in VS Code

To do this, search for Prettier - Code Formatter in the extension panel of VS Code. If you’re installing it for the first time, you’ll see an install button instead of the uninstall button shown here:
<img src="images/prettier1.png">

#### Step 2 — Run Prettier on a file

1 - Open Files -> Preferences -> Settings (or Ctrl + , in Windows).
2 - Search for Editor: Default Formatter
3 - Select your default formatter as Prettier - Code Formatter;

<img src="images/prettierFormatDoc.png">

#### Step 3 — Automatically run Prettier when saving a file

1 - Open Files -> Preferences -> Settings (or Ctrl + , in Windows) to open the Settings menu.
2 - Search for Editor: Format on Save
3 - Click the check box under Format On Save;

<img src="images/prettierFormatOnSave.png">

#### Step 3 — Changing the Prettier Configuration Settings

Along with Prettier's default settings you can also customize your settings.

Open the Settings menu. Then, search for Prettier. This will show all of the settings that you can change:

<img src="images/prettierCustomSettings.png">

Here are a few of the most common settings:

1 "singleQuote" - Choose between single and double-quotes.
2 "semi" - Choose whether or not to include semicolons at the end of lines.
3 - Specify how many spaces you want a tab to insert.

#### step 4 — Creating a Prettier Configuration File

Create a new file called .prettierrc.extension with a js extensions. For example, to set up a JavaScript config file you would use: _.prettierrc.js_

NOTE: Since Prettier will run for all files, its config file goes at the root of the repo.

<img src="images/prettierConfigFile.png">

For more details on Prettier, click the link to the Documentation: https://prettier.io/docs/en/configuration.html
