# Introduction to JavaScript for Seasoned Programmers
> This is the GitHub repository for Kayla Pringle's CS 330 Programming Language Project, which provides a tutorial on JavaScript for programmers experienced with other languages but not directly with JavaScript. All resources will be referenced via footnotes and can be found at the bottom of the page.

![Javascript Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/250px-Unofficial_JavaScript_logo_2.svg.png)

## History

JavaScript is a programming language that was created in May 1995 by Brendan Eich. Fun fact, it only took Eich ten days to develop the language! Originally named Mocha, the language was renamed to LiveScript and, in December 1995, renamed to the title we know and love today: JavaScript.[^1] It was initially developed to implement dynamic features on web pages on the user-side, meaning that anytime a website does more than sit there, JavaScript is involved. For developing websites, it is often used in conjunction with HTML and CSS. HTML provides the structure of a website's content, including paragraphs, headings, and embedding videos. I like to think of CSS as the "pretty language," as it allows you to style a page. JavaScript is the scripting language that enables features such as live-time content modification on a webpage, controlling multimedia, animating images, and many other applications.[^2] 

For information about this language, when it's time to start programming, this tutorial will use guidance from the [Geeks for Geeks JavaScript Tutorial](https://www.geeksforgeeks.org/javascript/javascript-tutorial/)![^3] We may also pull information from [W3Schools JavaScript Tutorial](https://www.w3schools.com/js/default.asp) as well, but this tutorial is for beginners+, as I like to call it, as I know you will have past coding experience.[^4] Finally, we will seek guidance from Dr.Dr. Axel Rauschmayer's book ["Exploring JavaScript"](https://exploringjs.com/js/book/index.html). Dr.Rauschmayer specializes in JavaScript, TypeScript, and web development.[^5] Though we will be using guidance from all of these excellent resources, this tutorial will still be individualized and created with originality; no time for plagiarism here, folks!

## Let's Get Started! 🏃💨

To begin, you must install JavaScript to run it. You can do so by visiting [Node.js](https://nodejs.org/en) and following the installation instructions. I think you should use the prebuilt Node.js for your respective system, as the installation wizard is efficient and installs all the additional tools you need! 

Although there is no recommended programming environment, Visual Studio Code (VS Code) is free, straightforward, widely used as a coding IDE, easily customizable, and I have the most experience using it, so we will be using that one for this tutorial. Now, the caveat is that you must install a Code Runner extension in order to actually run the code in VS Code, as you can create any JavaScript file you'd like, but VS Code does not have built-in support to do so. 

I suggest using the Code Runner extension with the extension ID found [here](formulahendry.code-runner). I recommend it as it supports a multitude of languages and has a straightforward installation process. I have also linked it [here](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner), and it should be the first extension at the top of the list when you search for "Code Runner" in the extensions tab in VS Code. I would suggest that you install it directly in VS Code via the extension ID to avoid any issues. I have included a screenshot below to ensure that you can correctly identify the extension, as I have also been confused about which ones to install for different languages myself. You will then need to shut down VS Code entirely, close any open files, and open a new window for the extension to function correctly. Now you are ready to start programming! 

#### Screenshot of Recommended Code Runner:
![Code Runner Screenshot](https://github.com/kay-pringle/CS-330-PLP-Kay-Pringle/blob/94a976b7b9182109812430fa4441a67bc658dd0d/Code%20Runner%20Screenshot.png)

## Writing Comments📝
We know how critical comments are for collaborating on code with others and just generally giving a good understanding of what the heck is going on in a code segment for ourselves. Similar to many languages that share C-like syntax, you can write ` // <insert text here> ` for single lines and ` /* <insert text here> */ ` for multiline comments so that they will appear as below:

````
// this comment is a single line!

/* This comment
  is a multiline comment */
````
Don't forget to comment as much as possible to help keep yourself and others informed about what's happening in your code flow. I know it can be an annoying extra step, but it helps in the long run.

## Writing Hello World✍️

We are finally ready to begin the classic starter exercise to help review language syntax: you love it and you know it well - printing out "Hello World!". To print out "Hello World" in JavaScript, we only need one line of code:

````
console.log("Hello World!");
````
Please note that, like other messages you may be familiar with, all lines must end with a semicolon. Now, let's get a bit deeper into JavaScript as a whole!

## Data Types and Naming Conventions

Now it's time to move on to naming conventions and the various data types that JavaScript has. We will cover a lot in this section, so please buckle up!

### Naming Conventions
First and foremost, here is an example of the variety of variables with correct syntax to serve as a reference as we go along to explore the various datatypes and naming conventions in the below coding example:

### Coding Example 1
````
var xNumber = 5;
const tNumber = 7;
let yNumber = 2.2;
let z = 75;
z = 80;
let myGoal = " to teach"
let isTeaching = true;
let newArray = [1, "two" , 3]
const theMap = new Map();
k = true + 1

````

I'm aware this is a lot, so let's break all of this down! Similar to other languages, when it comes to naming conventions for variables, camelCase is the the way to go, not mandated by the compiler but more adopted by the commmunity. You should ensure that the first letter of the name is lowercase, and allowing the use of numbers, underscores, and uppercase letters following the lowercase letter. 

Now, before doing creating data types in JavaScript, it is important to note there are several reserved words that should be used when declaring a variable. These include var, let, and const. The keyword "var" seen in ` xNumber ` is used to declare a variable in a global scope, meaning that if one wanted to re-assign a value to that variable, one could do so at a later time, but is less common in relation to the word "let", which has become more standardized in practice. 

The main two keywords when naming a variable you will see is "let" and "const". One would use the keyword "let" at the beginning of a variable declaration if you wanted a variable that could change values, as seen in the ` z ` variable listed above. When you want an unchanging values such as the ` tNumber `, you would use the word "const" at the beginning of the variable declaration. 

Now, to make things a bit easier, we are going to run through some discussion questions to help give as much clear information about Javascript as possible!
 
#### 1. Does your language have keywords or reserved words? How many?  

Javascript has numerous keywords, with the exact amount being highly debatable as there are words that are known as future keywords, which do not have current functions but may in the future so they are unable to be used as identifiers. The approximate number of current active words is approximately 39 [^6].

#### 3. Is your language statically or dynamically typed; Strongly typed or weakly typed; Explicitly typed or implicitly typed? 

Javascript is a weakly, dynamically, and implicily typed language as you don't have to list a declared type for variables and variables are able to change quickly as type is not checked until runtime.

#### 6. Are some variables mutable while others are immutable? 

Primitive varaibles and strings in Javascript are immutable as they can only be reassigned, not changed or added [^7]. However, with objects, they are able to be changed and are therefore mutable.

#### 7. What are the operators available for each data type? 

For each data type, the operators is as follows:

Numbers: ```` + - * / % ** ++ -- ````

Strings: ```` + (concatenation), template literals `Hello ${name}````

Booleans: ```` && || ! ````

Objects/arrays: ```` property access (obj.key, arr[0]), spread/rest (...) ````

To summarize, there are Arithmetic Operators, String concatenation Operators, Assignment Operators, Comparison Operators, and Logical Operators [^8].

#### 8. Are mixed type operations allowed? If so, how are they accommodated? 

This and the following question are tied together so it will be answered below.

#### 9. At what point are identifier names and operator symbols bound in your language? For example if you declare a (variable, class name, function name), when is it bound to the type, address? When are operators (+,*, etc.) bound to their operations?  

EXAMPLE OF (one) ILLUSTRATIVE EXAMPLE:  
If you put this line (or something similar) in a program and try to print x, what does it do? 
```` x = "5" + 6 ```` 
````x = "5" - 2 ````

Identifier names (variables, functions) are bound at run time. However, operators are bound at language definition time. The above example is a mixted type operation which we can use to demonstrate this point. When you do the above first operation, you would get the result "56", with x being converted to a string. However, when you do the second operation, the string would be converted to the number 4 due to when the operators are bound. The + sign is special as it's made for both string concatenation, so in the scenarios of addition will be overtaken by converting to string.

#### 10. Describe the limitations (or lack thereof) of your programming language as they relate to the Are there other restrictions or pitfalls that the documentation mentions that you need to be aware of? 

Javascript is able to mix types as seen in the coding example 1, however there will be areas that can cause some confusion. We already know about string concatenation, but there is also boolean addition, arrays that can hold mixed types and data type conversion that can be implicit.

Data type implicit example:

``` Number("826") = 826```
````Number ("826jkl") = error ````


#### 11. Are there built-in complex data types that are commonly used in your language? (hint: they’d probably appear fairly early in the documentation if so)







[^1]: https://www.geeksforgeeks.org/javascript/history-of-javascript/#
[^2]: https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/What_is_JavaScript
[^3]: https://www.geeksforgeeks.org/javascript/javascript-tutorial/
[^4]: https://www.w3schools.com/js/default.asp
[^5]: https://exploringjs.com/js/book/index.html
[^6]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#keywords
[^7]: https://www.codementor.io/@manik488/mutability-vs-immutability-in-javascript-1g9hwoeddd
[^8]: https://www.w3schools.com/js/js_operators.asp
