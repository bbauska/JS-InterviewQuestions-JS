<h1>JS-InterviewQuestions-JS</h1>

![image](https://github.com/user-attachments/assets/bd34fe1f-532c-433b-8ebd-f24aae728f95)

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>341+ JS Interview Questions You'll Most Likely Be Asked</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<cite>First edition. November 20, 2017.</cite>

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>01. Understanding IIFEs</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>Explain the concept of IIFEs (Immediately Invoked Function Expressions) in JavaScript. 
Provide an example of how to create and use an IIFE and discuss why they are commonly used in 
JavaScript.</p>

<h4>Solution:</h4>
<p>IIFEs, or Immediately Invoked Function Expressions, are a common JavaScript design 
pattern. They are functions that are defined and executed immediately after they are created. 
IIFEs have the following syntax:</p>

<pre>
(function IIFE() {
  console.log("Hello!");
})(); // Hello!
</pre>

<h4>IIFEs are used for several reasons:</h4>

<h4>Encapsulation:</h4>

<p>They create a new scope for variables, preventing variable name clashes 
with other parts of the code. This helps avoid polluting the global scope.</p>

<h4>Data Privacy:</h4>

<p>Variables declared within an IIFE are not accessible from the outside, 
providing a level of data privacy. This is useful for hiding implementation details.</p>

<h4>Initialization:</h4>

<p>IIFEs can be used for initializing code, such as setting up configurations, 
loading modules, or performing any necessary setup before the rest of the code executes.</p>

<h4>Pollution Avoidance:</h4>

<p>They help prevent global scope pollution by limiting the exposure of
variables and functions.</p>

<h4>Module Pattern:</h4>

<p>IIFEs are often used to implement the Module Pattern in JavaScript, which
allows you to create encapsulated modules with private and public members.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>02. Discussing Data Types</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>Discuss the various data types available in JavaScript and provide examples of each.</p>

<h4>Solution:</h4>
<p>JavaScript offers a range of data types for storing values:</p>

<h4>String: A sequence of characters enclosed in quotes (single or double).</h4>
<pre>let myString = “Hello World”</pre>

<h4>Number: Numeric values, including integers and floating-point numbers.</h4>
<pre>let myNumber = 42;</pre>

<h4>Boolean: Represents true or false values.</h4>
<pre>let myBoolean = true;</pre>

<h4>Array: An ordered collection of values.</h4>
<pre>
let myArray = [1, 2, 3];
null:
</pre>

<h4>Intentionally represents no value.</h4>
<pre>let myNull = null;</pre>

<h4>Object: Holds key-value pairs.</h4>
<h4>Keys are strings, and values can be any data type.</h4>
<pre>let myObject = { name: “John”, age: 30 };</pre>

<h4>undefined: Signifies an uninitialized variable.</h4>
<pre>
let myUndefined;
console.log(myUndefined); // undefined
</pre>

<p>These JavaScript data types enable value storage and manipulation in various ways, forming the 
foundation for dynamic and versatile programming.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>03. Mixins and Achieving Multiple Inheritance</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>In JavaScript, there's no built-in multiple inheritance support, making it challenging
to share functionalities across different objects efficiently. Traditional class 
hierarchies can become complex and rigid, hindering code maintainability.</p>

<h4>Solution:</h4>
<p>Mixins offer a solution by enabling code reuse and achieving a form of multiple 
inheritance. A mixin is a way to incorporate methods and properties from one object into another. 
This enhances modularity and flexibility in code design.</p>

<h4>Implementation:</h4>
<p>To implement mixins, you can use the Object.assign() method to copy methods 
and properties from a source object to a target object.</p>

<h4>Here's a brief example:</h4>
<pre>
const greetingsMixin = {
  sayHello() {
    console.log("Hello from mixin");
  }
};
const objectA = {};
Object.assign(objectA, greetingsMixin);
objectA.sayHello(); // "Hello from mixin"
const objectB = {};
Object.assign(objectB, greetingsMixin);
objectB.sayHello(); // "Hello from mixin"
</pre>

<p>By applying mixins, you can achieve code reusability and avoid deep class hierarchies. However, 
be cautious of potential method conflicts and unintended overwrites when using multiple mixins.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>04. How to Implement Polymorphism</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>Polymorphism is a fundamental concept in Object-Oriented Programming that enables 
objects to take on multiple forms. In JavaScript, polymorphism can be achieved using function 
overloading, where a function can have multiple implementations based on the number and
type of arguments it receives.</p>

<h4>Polymorphism:</h4>
<p>Polymorphism is the ability of objects from different classes to respond to the same method call 
differently. It allows treating objects from different classes as if they were objects of the same base
class, simplifying design and interaction between objects.</p>

<h4>Here's a simple example illustrating how function overloading can be implemented in JavaScript:</h4>

<pre>
function greet(name, language
  = 'English') { 
  if (language === 'English') {
    console.log(`Hello ${name}`);
  } else if (language === 'Spanish') {
    console.log(`Hola ${name}`);
  } else if (language === 'German') {
    console.log(`Hey Nazi Fucker... ${name}`);
  } else if (language === 'French') {
    console.log(`Hey French Turd... ${name}`);
}<br>

greet('John');  // Hello John
greet('Juan', 'Spanish');  // Hello Juan
</pre>

<h4>Solution:</h4>
<p>In this example, the greet function accepts two arguments: name and language. 
The default value for language is set to English. If you call the function with only one argument, 
it will utilize the default language. However, when you call the function with two arguments, it 
will use the specified language.</p>

<p>This mechanism demonstrates how polymorphism can be achieved in JavaScript through function
overloading, allowing a single function to exhibit different behaviors based on the input provided.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>05. Change the title of the page</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>Changing Page Title</p>

<h4>Answer:</h4>
<p>Using <b>document.title Property</b></p>
<p>You can change the title of a webpage using the document.title property in JavaScript.</p>
<pre>document.title = "My New Title";</pre>

<p>This is a straightforward task in JavaScript. Changing the page title is as simple as assigning 
a new value to the document.title property. It's a basic operation that most web developers should 
be familiar with, making it an easy problem. However, it's still an important concept to understand 
when working on web development projects.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>06. Understanding JSON</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>Explain what <b>JSON (JavaScript Object Notation)</b> is and its purpose in web development.</p>

<h4>Solution:</h4>
<p>JSON, short for JavaScript Object Notation, is a lightweight data interchange format that is 
easy for humans to read and write, and easy for machines to parse and generate. It is often used 
for exchanging data between a server and a web application, as well as between different parts 
of an application.</p>

<p><span class="consolas">JSON</span> is represented as <b>key-value pairs</b>, where keys are strings 
and values can be strings, numbers, Booleans, arrays, or other JSON objects.</p>

<h4>The basic syntax of a JSON object looks like this:</h4>
<pre>
{
  "key1": "value1",
  "key2": 123,
  "key3": true,
  "key4": ["item1", "item2"],
  "key5": {
    "nestedKey": "nestedValue"
  }
}
</pre>

<p><span class="consolas">JSON</span> is widely used because of its simplicity, ease of use, and 
compatibility with various programming languages. It is a common format for sending and receiving 
data in web APIs, configuring applications, and storing configuration settings.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>07: What is JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p><span class="consolas">JavaScript</span> is a <b>scripting language</b> that 
adds interactivity to HTML pages.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>08: What kind of language is JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JavaScript is an <span class="consolas">interpreted language</span> that 
executes scripts without preliminary compilation.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>09: What is the official name of JavaScript and is it supported by all browsers?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The official name of JavaScript is <span class="consolas">ECMA (European Computer 
Manufacturer's Association)</span> and with it, Internet Explorer 4 and Mozilla Firefox 1.5 fully supported.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>10: What does JavaScript do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JavaScript is meant to be an easy <span class="consolas">scripting language</span> 
that helps the non-programmers with its simple syntax. JavaScript is smart enough that it can put 
dynamic text into HTML pages, it can react to events (like when a page has finished downloading), and it 
can read and write HTML elements, create cookies and so forth.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>11: Is JavaScript case sensitive?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Yes. Unlike HTML, JavaScript has to have all variables and function names (etc.) in capital 
letters.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>12: How do you place JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Scripts can be placed in the &lt;body&gt;, or in the &lt;head&gt; section of 
an HTML page, or in both. JavaScript in &lt;head&gt;. JavaScript may be inserted into code with 
the following syntax:</p>
<pre>&lt;script type="text/JavaScript"&gt;</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>13: Where do you place JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JavaScript may be placed in the &lt;head&gt; or &lt;body&gt; section of HTML code,
but it is usually a good practice to place it in &lt;head&gt; as to not hinder your code later on.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>STATEMENTS, COMMENTS AND VARIABLES</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>14: How do you terminate statements in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>In JavaScript, statements are terminated by <span class="consolas">semicolons (;)</span> 
and although they are not mandatory they are a good practice to pick up.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>15: Why are comments used in JavaScript and how are they inserted?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Usually comments are added to make the code more readable but they can
also be used to explain the code. They are inserted with // (for single line comments) 
and /* */ for multiple lines comments.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>16. Explain equality</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem: JavaScript has both strict and type–converting comparisons:</h4>

<p><b>Strict comparison (e.g., ===)</b> checks for value equality without allowing coercion.<br>
<b>Abstract comparison (e.g., ==)</b> checks for value equality with coercion allowed.</p>

<h4>Answer:</h4>
<pre>
const a = "42";
const b = 42;
console.log(a == b); // true
console.log(a === b); // false
</pre>

<p>Some simple equality rules: If either value (also known as side) in a comparison could be the 
true or false value, avoid == and use ===.</p>
<p>If either value in a comparison could be of these specific values (0, "", or [] — empty array), 
avoid == and use ===.</p>
<p>In all other cases, you’re safe to use ==. Not only is it safe, but in many cases, it simplifies 
your code in a way that improves readability.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>17: What are variables and how are they inserted?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p><span class="consolas">Variables</span> are storing containers used for 
holding expressions and values. They can have a short letter or a longer name and are 
inserted with the statement: var. Because the variables are loosely typed, they can hold 
any type of data.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>18: What does a variable of var y=10; and var catname= "Tomcat"; do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>With the execution of the above code, we have variables that hold values of 
10(for y) and Tomcat (for catname). Note that the inclusion of text warrants " " being used.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>19: How many statements types can we find in JavaScript? Give some examples?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The statement types found in JavaScript are: Expression statements, compound, 
empty and labeled statements.</p>

<h4>Example:</h4>
<p>break, continue, default, do, for, etc.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>20. Understanding Exponential Operator</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Problem:</h4>
<p>Explain the usage of the exponential (&ast;&ast;) operator in JavaScript, 
including when and how to use it to perform exponentiation calculations.</p>

<h4>Answer:</h4>
<p>The <span class="consolas">exponential operator (&ast;&ast;)</span> in JavaScript 
is used to perform exponentiation, which is raising a number to a power. It's a concise and intuitive 
way to perform such calculations.</p>

<h4>Here's how to use it:</h4>
<pre>
// Using the exponential operator
const result1 = 2 &ast;&ast; 3;  // raised to the power of 3 
console.log(result1);  // 8
const result2 = 4 &ast;&ast; 8.5;  // Square root of 4 
console.log(result2);  // 131072
const result3 = 10 &ast;&ast; -2;  // 10 raised to the power of -2
console.log(result3)  // 0.01
</pre>

<p>The exponential operator can be used with both integer and floating-point exponents. It's 
particularly useful when you need to perform exponentiation calculations in a clear and 
concise manner.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>21: What are conditional statements and how are they implemented in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Conditional statements are used to perform and act on different sets of 
conditions declared by the programmer. They are the following: if statement; if...else 
statement; if...else if...else statement and the switch statement.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>22: How will you determine a variable type in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>A variable type in JavaScript is determined using Typeof operator. When the 
object is String, Number, Function, undefined and Boolean, the operator returns the same type. 
And when the object is null and array, the operator returns “object”.</p>

<h4>Example:</h4>
<pre>
var count=100;
typeof count;  // (returns “number”)
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>23: What is the difference in evaluating [“8”+5+2] and [8+5+”2”]?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>In [“8”+5+2],”8” is a String. So anything that trail the string will be changed to string.<br>
Hence the result will be ”852”.<br>
In [8+5+”2”], 8 and 5 are integer, so it gets added up (13).And “2” is treated as String.<br>
Hence the concatenation takes place and the result will be “132”.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>24: Is it possible to assign a string to a floating point variable?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Yes. Any variable can be assigned to another data type. For example,</p>
<pre>
var a1=10.39;
document.write(a1);
10.39
a1=”hai”;
document.write(a1);
hai
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>25: Will variable redeclaration affect the value of that variable?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4> 

<p>No. The same value will be retained in the variable.</p>

<h4>Example:</h4>
<pre>
var status=”cool”;
document.write(“status”);  // cool
var status;
document.write(“status”);  // cool
status=”chill”;
document.write(“status”);  // chill
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>26: How will you search a matching pattern globally in a string?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>A matching pattern can be globally searched in a string using “g” modifier
in Regular Expression.</p>

<h4>Example:</h4>
<pre>
var p1=”First_Regular_ Expression_First”;
var q1=”/First/g”;
document.write(“Pattern_Match:” + p1.match(q1)); // Pattern_Match:First,First
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>27: How will you search a particular pattern in a string?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>A particular pattern in string can be searched using test function. If the
match is found it returns true, else false.</p>

<h4>Example:</h4></p>
<pre>
var my_pattern1=new RegExp(“pp”);
document.write(my_pattern1.test(“Happy_Days”);  // true
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>28: Which property is used to match the pattern at the start of the string?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>“^” symbol is used for position matching.</p>

<h4>Example:</h4></p>
<pre>
var p1=”First_Regular_ Expression_First”;
var q1=”/First/^”;
document.write(“Pattern_Match:” + p1.match(q1));  // Pattern_Match:First First_Regular
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>29: Which property is used to match the pattern at the end of the string?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>“$” symbol is used for end position matching.</p>

<h4>Example:</h4></p>
<pre>
var p1=”First_Regular_ Expression_First”;
var q1=”/First/$”;
document.write(“Pattern_Match:” + p1.match(q1));  // Pattern_Match:First Expression_First
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>OPERATORS AND FUNCTIONS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>30: What are operators? Which are the most important operators in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Operators in JavaScript are used to combine values that form expressions.
The most important are: = and +. The first is used to assign values and the second one is used 
to add values together.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>31: Why comparison and logical operators are used?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Comparison operators are used to determine if there is a difference between
variables, and also their equality, while the logical operators are used to determine the logic 
of variables.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>32: How many types of pop-up boxes does JavaScript have? What are those?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JavaScript has three types of pop-up boxes and they are: alert, confirm and prompt.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>33: Does creating an alert box prompt the user to respond with OK or Cancel?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>No. An alert box only gives the user the option of choosing OK to proceed.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>34: What are functions in JavaScript and where are they placed?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Functions contain code that is executed before an event thus stopping the
browser from loading a script when the page opens. Functions can be
placed both in the <head> or <body> section, but it is advised to place them
in the <head> section.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>VALUES, ARRAYS AND OPERATORS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>35: What does the keyword null mean in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The keyword null is a special value that indicates no value. It is unique
from other values and also fully distinct.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>30: What does the value undefined mean in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Undefined is a special value in JavaScript, it means the variable used in the
code does not exist or is not assigned any value or the property does not exist.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>31: Do the null and undefined values have the same conversion in Boolean, numeric and string context?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>No. The undefined value changes into Nan in numeric context and 
undefined in a string context. They share the same conversion in Boolean.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>32: What are Boolean values?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Boolean values are datatypes that only have two types of values: true or
false; a value of Boolean type only represents the truth: it says if it true or not.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>33: Can a Boolean value be converted into numeric context?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Yes. If it is converted into numeric context the true value becomes 1 and if
it is a false value it becomes a 0.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>34: What happens when a number is dropped where a Boolean value is expected to be?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The number is converted into a true value, but only if it not equal to 0 or
NaN which in turn is converted into a false value.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>35: What are objects in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Objects are collections of named values that most of the times are referred
to as properties of an object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>36: What is an array in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>An array is a collection of data values which can handle more than one
value at a time, the difference being that each data in an array has a number or index.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>37: From which version forward has JavaScript stopped using ASCII character set?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>From v.3 JavaScript started using Unicode character sets: identifiers can
now contain letters and digits from the Unicode complete character set.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>38: What is the scope of a variable in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The scope of a variable is the region in which your program in which it is 
defined. Thus a global variable has a global scope meaning it is defined everywhere in your 
JavaScript code. The local variables have a local scope meaning they are defined only in the 
body section of your code.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>39: In the body of the code which variable with the same name has more importance over the 
other: the local or the global variable?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>In the body of a function a local variable will always take precedence over a
global variable hiding it all together.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>40: How many types of undefined variables can we find in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are two kinds of undefined variables: the first is the one that has 
never been declared and the second is the kind of undefined variable that has been declared 
but has never had a value assigned to it.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>41: What does (==) & (===) operators do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The first (==) is the equality operator and it checks if its two operands are
equal. The second (===) is called the identity operator and it checks if two operands are 
identical by using a strict definition.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>42: How many types of operators can we find in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are eight types of operators in JavaScript. These are as follows: 
operator, arithmetic, equality, relational, string, logical, bitwise and miscellaneous.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>43: How many types of comparison operators does JavaScript contain?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are four types of comparison operators in JavaScript. They are: less 
than (&lt;); greater than (&gt;l); less than or equal (&lt;=) and greater than or equal (&gt;=).</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>44: Can comparison be done on any type of operands?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4> Yes. Operands in JavaScript that are not number or strings are converted.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>45: What are logical operators and how are they used in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The logical operators perform Boolean algebra and are used mostly with 
comparison operators to show complex comparisons that involve more than one variable.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>46: Does JavaScript contain classes?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Yes. Although they do not define the structure of an object like in Java and 
C++, it does approximate the classes with its constructors and their prototype objects.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>47: What is the purpose of an object in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>An object is an instance of its class. This allows us to have multiple 
instances of any class.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>48: How are classes and objects in JavaScript named and why?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Classes are named with an initial capital letter and an object with lowercase 
letters. This ensures that classes and objects are distinct from each other.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>49: What are class properties in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Class property is associated with a class itself and not instance of a class. 
This ensures that no matter how many instances of a class are created only one copy of each 
class property exists.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>50: What are class methods in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Class methods are associated with a class rather than an instance of a class, 
meaning they are invoked by the class itself and not an instance of the class.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>51: Do class properties and class methods have a global and local range?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>No. They are both only global because they do not operate on a particular object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>52: How do JavaScript equality operators compare objects?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Equality operators compare objects by reference and not by value, checking 
to see if both references are to the same object. They do not check to see if two objects have 
the same property names and values.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>53: Are the null and undefined values for the variable same?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>No. Variables that are declared and not assigned any value will have undefined 
values whereas the variable that is assigned a null will have null values.</p>

<h4>Example:</h4>
<pre>
var qno;
”undefined value”
var Items=10;
Items=null;
”null value”
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>54: What is the difference between “===” and “==”? Give examples</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) “===” returns true - if both the operands are same and are of the same data type<br>
b) “==” checks only for operands - if both are same, returns true</p>
<p>For comparison of operands, JavaScript converts different data type to same type.</p>

<h4>Example:</h4>
<pre>
Let p=3
p==’3’ //true p===’3’ //false
3==’3’ //true 3===’3’ //false

P==3 //true P===3 //true
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>55: What is the function of delete operator in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>It deletes<br>
a) an object<br>
Syntax: delete obj_name1;<br>
b) particular element in an array<br>
Syntax: delete arr_ele1[index];<br>
c) property of an object<br>
Syntax: delete obj_name2.prop_name;</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>56: How will you clip the particular portion of an element?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using clip property of the style object, we can clip a particular portion of an element.</p>

<h4>Example:</h4>
<pre>
my_obj1.style.clip=”values”;
my_obj1
</pre>

<p>document object, getElementById property values<br>
auto(Unclip),rect(top1,right1,botttom1,left1)-pin the shape defined by value.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>MODULES, CHARACTERS AND ATTRIBUTES</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>57: How is a module in JavaScript written so that it can be used by any script or module?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The most important rule is to never define global variables as to have the
risk of having that value overwritten by a module or another programmer.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>58: How are regular expressions represented and created in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Regular expressions are represented by the RegExp objects and are created
by the RegExp() constructor or a special literal syntax.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>59: How do you combine literal characters in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Literal characters can be combined into character classes by placing them
within square brackets.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>60: What document properties does a document contain?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>In a document we can find the following properties: bgcolor, cookie,
domain, lastModified, location, referrer, title and URL.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>61: How many types of DOM document object collections can we find in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are five DOM properties that give access to special elements within a
document: anchors, applets, forms, images and links.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>62: Does use of DOM properties allow you to change the structure of a document?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>No. Using these properties you can inspect and alter a link and read values
from a link but the text in the document cannot be changed; the structure of the document 
cannot be altered.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>63: How are document objects named in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Documents are named with the name attribute of forms. You can change
elements, links and images when the name attribute is present. Its value is
used for exposure to the corresponding object by name.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
EVENT HANDLERS AND DOM
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>64: How are event handlers defined in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Event handlers are defined by assigning a function to an event handler
property, unlike HTML where event handlers are defined by giving a string
of JavaScript code to an event handler attribute.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>65: What do the HTMLInputElement and HTMLFormElementinterfaces define in HTML DOM?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The HTMLInputElement defines focus() and blur() methods and form
property. HTMLFormElementinterfaces defines submit() and reset()
methods and length property.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>66: How many levels of DOM standard are currently released?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are two levels of DOM: the first one was released in 1998 and it
defines the core DOM interfaces. The second level that was released in
2000 that updates the core interfaces and defines standard APIs for working
with document events style sheets CSS.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>67: Are there any more levels of DOM?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Yes there are. One of them is the level 3 DOM, but its features are not fully
supported by all the web browsers and the other is the level0 DOM whish in
fact is the legacy DOM.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>68: What does the Node interface define in DOM?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The node interface defines the childNotes, firstChild, lastChild, nextSibling
and previousSibling properties.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>69: How do you find document elements in a HTML document?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>You can find elements by using the getElementsByTagName and obtain any
type of HTML element.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>70: How are documents created and modified in DOM?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Documents are modified by setting attribute values on document elements
with the element.setAttribute() method. They are created with
document.createDocumentFragment().</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>71: How can you build a DOM tree of arbitrary document content?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>You can achieve this by creating new Element and text nodes with the
Document.CreateElement() and Document.CreateTextNote() methods; you
can then add them to a document with the Note.AppendChild(),
Note.InsertBefore() and Note.replaceChild() methods.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>72: How do you find document elements in IE4?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Because IE4 does not support the getElementById() and get 
ElementsBytagName()methods we are forced to use the array property
named all().</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>73: How to access Html attributes using DOM?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using three methods of DOM:<br>
a) getAttribute(): Retrives the value of an attribute<br>
b) setAttribute(): Modifies the value of an attribute<br>
c) removeAttribute(): Removes the entire attributes from an element</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>74: What is the difference between getAttribute() and getAttributeNode()?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
<p>a) getAttribute(): returns the value of an attribute<br>
b) getAttributeNode(): returns the attribute itself</p>

<h4>Example:</h4>
<pre>
<body>
  <p id="ki" attr="Ish">Hellllo</p>
  <script>
    txt1=document.getElementById('ki').getAttribute('attr');
    document.write(txt1 + "<br>");
    txt2=document.getElementById('ki').getAttributeNode('attr');
    document.write(txt2.name +"&nbsp : &nbsp ");
    document.write(txt2.value);
  </script>
</body>
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>75: What are the event handlers in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Event handlers are the JavaScript code that can be used inside the Html tags
and gets executed when any events such as form submission, page loading
occur. Some of the event handlers in JavaScript are:</p>
<p>a) onload<br>
b) onunload<br>
c) onclick<br>
d) onmouseout<br>
e) onmouseover</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>76: Can you use two or more functions in onclick event?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>By separating the functions with semicolon(;) we can use two or more
functions. First function gets executed after onclick event. The consecutive
functions get executed only when the immediate previous function returns
true.</p>

<h4>Example:</h4>
<pre>onclick=(“my_fun1();my_fun2();my_fun3()”);</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>KEYWORDS, CSS AND CSS2</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>77: What is the “this” keyword in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>When an event handler with an HTML or JavaScript property is defined a
function to a property of a document element is assigned. When the event
handler is invoked the “this” keyword refers to the target element.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>78: What does lexically scoped in JavaScript mean?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>It means that functions run in the scope that they are defined in and not in
the scope they are called in.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>79: Is the following expression correct: element.style.font-family="arial";?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>No. It is incorrect because in JavaScript many CSS style attributes contain
hyphens in their names and these are interpreted as minus signs.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>STATEMENTS AND FUNCTIONS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>80: How can you replace an if-else statement in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>You can simply replace if-else statement by using the ternary operator.
These kinds of operators require three operands. The ternary operator can
be defined as follows:</p>
<pre>(condition) ? val1 :val2.</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>81: What is a "memoization" method in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Memoization is an optimization technique used in JavaScript. Functions
may use objects to remember the results of previous operations, in this way
avoiding unnecessary work.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>82: What does 2+3+”1” evaluate to?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>As 2 and 3 are integers, 2+3 will evaluate to 5. Since “1” is a string, it will
concatenate with 5 and the final result will be the string “51”</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>ROLES OF JAVASCRIPT, SCRIPTS AND EVENTS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>83: Give some examples of the role that JavaScript has on the Web.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The role of JavaScript is to provide a better user browsing experience.
JavaScript can do many things like: creating visual effects such as image
rollovers, sorting the columns of a table, so the user can easily find what he
needs and hiding certain content.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>84: Give an example on how JavaScript can be used in URLs.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JavaScript can be used in URLs, using “JavaScript:” pseudoprotocol
specifier. This specifies that the body of the URL is an arbitrary string of
JavaScript code to be run by the JavaScript interpreter. It is treated as a
single line of code, and the statements must be separated by semicolons. A
JavaScript URL can look like this one:</p>
<pre>
JavaScript:varJavaScript:varJavaScript:varJavaScript:varJavaScript:varJava
Script:varJavaScript:varJavaScript:varJavaScript:varJavaScript:varJavaScri
pt:varJavaScript:varJavaScript:varJavaScript:varJavaScript:varJavaScript:v
ar today = new Date(); “<p>The date is:</p>” + today;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>85: How are scripts in JavaScript executed?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
Scripts are executed in the order in which they appear and the code in the
<script> tags is executed as part of document loading process.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>86: What do scripts placed in the <head> part of an HTML document do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Scripts placed in the <head> section usually define functions that are to be
called by other code and/or declare and initialize variables used by other
code.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>87: What do scripts placed in the <body> part of an HTML document do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Scripts placed in the <body> part of a document can do everything that
those placed in a <head> section of the document do. They can also
manipulate document elements that appear before the script.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>88: When does browser trigger the onload event?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The browser triggers the onload event and executes any registered
JavaScript code under the following scenarios:</p>
<p>a) Once the document has been parsed,<br>
b) All scripts were executed and<br>
c) All auxiliary content has finished loading.</p>

<p>For all the major browsers (except IE), the JavaScript onload event does not
trigger when the page loads as a result of a Back button operation. Rather
the event is triggered only when the page is loaded.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>89: When does the onunload event trigger and what does it do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The onunload event triggers after the user navigates away from the web page giving the 
code on that page a final chance to run; the onunload event enables the possibility to undo 
effects of your onload handler or scripts in the web page.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>90: How can we read or write a file in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Client-side JavaScript does not provide any way to read, write or delete
files or directories on the client computer. This is also a security aspect –
with no File object and no file access functions, a JavaScript program
cannot delete a user's data.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>91: Explain about “cross-site scripting”.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Cross Site Scripting (XSS) is called as the name of a security issue where
the hacker or attacker injects the scripts or HTML tags into a website.
Even though defending XSS attack is a job for server-side script developers,
the JavaScript programmers should also be aware of cross site scripting and
defend against this attack.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>92: What are JavaScript timers? Give examples and explain one of them.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>It is very important for any programming environment to have the ability to
schedule code to be executed at some point in the future. Client-side
JavaScript provides some global functions like: setTimeout(),
clearTimeout(), setInterval(), clearInterval(). For example setTimeout()
method schedules a function to run after a specific number of milliseconds
elapses.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>93: Explain the history property in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The history property of the Window object refers to the History object for
the window. The History object supports three methods: back(), forward()
and go(). The first 2 methods are similar with what happens when the user
clicks on the Back and Forward browser buttons. The go() method takes an
integer argument and can skip any number of pages</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>94: What is the “Screen” object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The screen property of the Window object refers to a Screen object that
provides information about the size of the user's display, the number of
colors available on it. The “width” and “height” properties can be used to
specify the size of the display in pixels.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>95: What is the “Navigator” object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The navigator property of a Window object refers to a Navigator object that
contains important information about the web browser, such as the version
and the list of data formats it can display. In the past Navigator object was
used by scripts to determine if they were running in Internet Explorer or in
Netscape web browser.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>96: What is “onreset” in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Onreset is an event handler of a form object in JavaScript. It gets executed
when the reset button in the form is clicked and resets the fields when it
receives true value otherwise prevent the form elements from being reset.</p>

<h4>Example:</h4>
<pre>onreset=”alert(‘AABBCC’)”</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>97: What is void 0 in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) JavaScript files can be executed directly in the web browsers by placing
“JavaScript:” before the code<br>
b) Web browsers attempt to load the page when any value returning
JavaScript’s code is executed<br>
c) void 0 is used to prevent the unwanted action</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>98: What is the best practice to place the JavaScript codes?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Place all JavaScript codes in one place. So it can be placed,<br>
a) At the end of html tag<br>
b) Below second header tag<br>
c) Before the closing of bod tag</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>99: How to prevent caching of web pages in temporary internet files folder?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Caching of web pages in temporary internet files folder can be prevented by
adding &lt;META HTTP-EQUIP=”PRAGMA” CONTENT=”NO-CACHE”&gt;
in the second header tag which is placed before the html’s end tag(&lt;/html&gt;).

<h4>Example:</h4>
<pre>
&lt;html&gt;
&lt;head&gt;
&lt;META HTTP-EQUIV="REFRESH" CONTENT="3"&gt;
&lt;/head&gt;
&lt;body&gt;
&lt;p&gt;Hello&lt;/p&gt;
&lt;/body&gt;
&lt;head&gt;

&lt;META Http-equiv="PRAGMA" Content="NO-CACHE"&gt;
&lt;/head&gt;
&lt;/html&gt;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>100: Why adding of meta tag in first header will not prevent caching of the Web page?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The browsing page gets cached only when the buffer is half filled. So when
the meta tag is added in first header, the internet explorer search for that
page in cache at that instant. Most of the time, buffer won't get half filled at
the beginning of parsing.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>101: What is the purpose of meta tag?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>When this tag is read while parsing the html code, internet explorer
searches for this page in cache at that instant. If it is found, it will be
removed from the cache.</p>

<h4>Syntax:</h4></p>
<pre>&lt;META Http-equiv="PRAGMA" Content="NO-CACHE"&gt;</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>102: How will you resolve looping problem in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using closures which combines the function with its referencing
environment, looping can be resolved. It keeps the local variable of the
function alive even after the function returned the value. When there is
function within the function, Closure is created.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>103: Give any example for resolving looping problem.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<pre>
var method1={};
  for(var k=0;k<5;k++){
    method1[i]=function(){
      document.write(“Iteration:” + k + “<&nbsp>”);
    };
  }
  for(var m=0;m<5;m++){
  method1[j]();
}
// Output:
// 4 4 4 4 4 instead of 0 1 2 3 4
</pre>

<p>By adding closure,this can be rectified.</p>

<pre>
method1[i]=function(n){
  return function(){
    document.write(“Iteration:” + n + “<&nbsp>”);
  }
})(k);
// Output:
// 0 1 2 3 4
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>104: When is the Execution context created and what are the primary components?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>During execution of JavaScript function, the execution context is created. It
keeps track of the execution of its related code. Global execution context is
created when executing the application.<br>
a) LexicalEnvironment: Resolves the identifier references<br>
b) VariableEnvironment: Records the variable-function declaration bindings<br>
c) ThisBinding: value of “this” keyword related with execution context</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>105: When is the Execution context stack created?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Global execution context: Created when executing the application<br>
b) New execution context: Created when the new functions are created<br>
c) Collection of this execution context form the execution context stack.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>106: How is the outer scope environment references maintained?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using LexicalEnvironment, the outer scope environment references are
maintained. It contains two components:</p>
<p>a) Environment Record: Identifier bindings are stored for the execution context<br>
b) Outer Refernces: Points to the declaration of execution context in lexical Environment</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>107: How will you read or write in a file using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>An I/O operation such as reading or writing is not possible. However, “Java
Applet” can be implemented to read files for script.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>108: How will you create rich, responsive display and editor user interface?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using knockout we can create rich, responsive display and editor user
interface. It is JavaScript library which implements the model view-
viewmodel pattern. It is used to create UI and allows dynamic updation and
can be used with any server or client.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>109: Which is the new JavaScript engine developed for internet explorer9 by Microsoft?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Chakra is the new JavaScript engine for IE9. A distinct feature is that its JIT
compiles scripts on separate “CPUcore”, parallel to web browsers. The
engine also accesses the computer’s graphic processing unit for 3D videos
and graphics. To execute scripts on traditional web pages and to improve
JavaScript runtime and libraries, a new interpreter was included.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>110: What is Node.js?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Node.js is a software designed for creating server side JavaScript
application which is not executed in client browser. It is event based and
runs asynchronously to provide scalability and reduce overhead.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>111: Which is alternative to XML for data exchange in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JSON (JavaScript Object Notation). Light weighted, text-based data
exchange format. Web data is imported into JavaScript applications using
JSON.</p>

<h4>Example:</h4>

<p>JSON Object creation</p>

<pre>
var obj_json1={“Company_name”:”ABC”,”Experiance”:”5”};
document.write(“Co Name:” + obj_json1.Company_name); //Co Name:ABC
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>112: What are the sub-components of dynamic component in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Dynamic typing: Based on values; not associated on variable<br>
b) Obj-based: Properties of an object can be modified at run-time; Built-in
functions are used for properties to maintain dynamicity<br>
c) Run-time evaluation: eval() is used for run time evaluation and will
take dynamic arguments at run time.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>OPENING AND MANIPULATING WINDOWS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>113: How can you open a new window using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>We can open a new web browser window using “open()” method of the
Window object.Window.open() has four optional arguments and returns a
window object that represents the new open window. The first argument is
the URL of the document to display in the new window (if it is null or
empty string, the window will be empty), the second argument is the name
of the window; the third parameter is a list of features that specify the
window size and GUI decoration. The fourth argument is useful only when
the second argument is mentioned.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>114: How can you close a window using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>We can close a created window object using “close()” method. The syntax
is: Window.close()</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>115: What does the “location” function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The location property of a window is a reference to a location object and
represents the URL of the document that is displayed in the window. The
Href property of the location object is a string that contains all the text of
the URL.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>116: What other properties besides Href can we find in the “location” function in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Other properties that we can use are: protocol, host, pathname and search.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>117: What happens when a string value is added to the location function in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The browser interprets the string as a URL and tries to load it and display
the document and that URL.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>118: What is the history object in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The history object refers to the History of the browser window. The
multitudes of elements that the history object incorporates are never
accessible to scripts.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>119: Which are the methods supported by the history object in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are three methods supported by the history object: the back(), the
forward() and the go().</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>120: How many and which are the coordinates of a browser within the HTML document?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are three types of coordinates and these are: screen, window and
document coordinates.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>OBJECTS AND THEIR PROPERTIES IN JAVASCRIPT</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>121: Name the properties of Navigator in JavaScript.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>There are five properties for the navigator object and these are: appName,
appVersion, userAgent, appCodeName and platform.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>122: What happens when confirm() or prompt() methods are used in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>When these boxes are initialized the code stops running and the currently
loading document stops loading until the user response with the requested
input.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>123: What happens when the mouse is moved over a hyperlink in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JavaScript code evaluates the onmouseover attribute and sets the status
property of the window, thus returning the “true” value telling the browser
not to take any actions.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>124: What does the “defaultStatus” property do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The “defaultStatus” property enables text to be displayed in the status line
when the browser does not find anything to display. Newer versions of the
current browser have this property deprecated.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>125: What is the “onerror” property in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The “onerror” property has a special status: the function the user assigns
becomes an error handler for the window; the function assigned to the
property is invoked when an error occurs in that window.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>126: What arguments does the error handler receive when an error occurs in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The error handler receives three arguments: the first is the message that
describes the error; the second is the string that contains the URL of the
document containing the JavaScript code that caused the error and the third
argument is line number within the document where the error occurred.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>127: In addition to the three arguments that the error handler receives, is its return value of any importance?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The return value of the error handler is significant: if the onerror handler
returns True then the browser does not display its own error message having
been told that the handler has taken care of the error.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>128: How can JavaScript code refer to a window or frame object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>In JavaScript we can refer in any window or frame to its own window or
frame using “window” or “self”. They are necessary to use when the
programmer needs to refer to this global object itself. In case the
programmer wants to refer to a method or property of the window/frame, it
is not necessary to prefix the property or method name with “window” or
“self”.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>129: What is a DOM (Document Object Model)?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>DOM (Document Object Model) is an API that defines the way to access
the objects that compose a document. W3C defines a standard DOM that is
reasonably well supported in all modern browsers.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>130: What does the method write() of the Document object do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The write() method allows users to write content into the document. The
write() method is part of DOM and it can be used in two ways. First of all,
it can be used within a script to output HTML into the document being
parsed. Second, write() can be used (in conjunction with open() and close()
methods of the Document object) to create entirely new documents in other
windows or frames.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>131: How will you determine an object type?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using “Instanceof and isprototypeof” by checking its instance and
prototype respectively.</p>

<h4>Example:</h4>

<pre>
document.writeln(book1 instanceof Book);
var Book = function() {...};
Book.prototype.constructor == Book; //return true
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>132: What is alert and confirm box in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Alert and confirm both are pop ups in JavaScript and take the focus of
the user from the current page to pop ups<br>
b) Alert provides the user with “ok” button whereas confirm provides with
“ok” and “cancel” button where user can select any one of the options<br>
c) When “ok” is selected, confirm returns true else false.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>133: What are the properties of array object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Index property<br>
b) Input property<br>
c) Length property<br>
d) Constructor property<br>
e) Prototype property</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>134: What are the sub objects of the windows object in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Document object: Work with DOM and provides interface to XML and
Html documents and allow CSS manipulations<br>
b) Frame object: Represents &lt;frame&gt; HTML frames. Frame object will be
created for each &lt;frame&gt; tag<br>
c) Location object: Contains the current URL information
“window.location”<br>
d) History object: Contains the URL history visited by the user</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>135: What is the use of userAgent of navigator object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Identifies the operating system of the client’s machine<br>
b) “appVersion” and “userAgent” can also be used<br>
c) “userAgent” property of navigator object returns the value of the user
agent header sent by the browser to server</p>
<h4>Syntax:</h4>
<pre>
document.write(navigator.userAgent);
document.write(navigator.appVersion);
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>136: What are the ways to delete the property of an object and how?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>It can be deleted in two ways.</p>
<h4>Example:</h4>
<pre>
oven=new Object();
oven.name=”LG”;
oven.color=”Black”;
</pre>
<p>a) using object name and property</p>

<h4><b>Example:</h4>
<pre>delete oven.color;</pre>
<p>b) using object name and property with “with”statement</p>
<h4>example:</h4>
<pre>
with(oven)
delete color;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>137: What is the use of eval() in JSON?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>JSON can be parsed using the built-in function eval() and JSON data is
executed to generate native JavaScript object.</p>
<h4>Example:</h4>
<pre>obj_json2=eval(‘(‘ + JSON_text+’)’);</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>138: What are the advantages of JSON over XML?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) JSON provides array and object type and also some scalar data types
whereas XML does not provide any data types<br>
b) Formatting is done by direct mapping in JSON whereas it is complex in Xml<br>
c) Document size is too large in XML. When the data grows, amount of xml
also grows whereas documents are compact in JSON</p>
<h4>XML:</h4>
<pre>
&lt;Record&gt;
&lt;First_Name&gt;abcd&lt;/First_Name&gt;
&lt;Age&gt;25&lt;/Age&gt;
&lt;/Record&gt;
</pre>
<h4>JSON:</h4>
<pre>
{
  “Record”:{“First_Name”:”abcd”,”Age”:”25”}
}
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>139: How can the properties of JavaScript objects be accessed?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The properties of JavaScript objects be accessed in the two ways shown
below:</p>
<h4>Syntax:</h4>
<p>
a) obj_name.prop1;<br>
b) obj_name[“prop1”];</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>140: What are the objects of navigator objects?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Window object: gets created for every frame and web browser<br>
b) Mime type object: using enabledplugin, gets information about the
plugin<br>
c) Plugin object: gives information about an installed plug-in</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>141: How to access the properties of main window from the secondary window?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>This can be done using Opener property. The properties of the main
window can be accessed from secondary window.</p>

<h4>Example:</h4>
<p>In the secondary window:<br>
window.opener.document.bgColor=”my_color_value”; //give color name or hex code</p>
<p>It changes the background color of the primary window to the given color.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>142: How will you load the previous and next url from the history list?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The previous and next url from the history list can be loaded using back and
forward function of history object.</p>

<h4>Example:</h4>
<pre>“history.back()”;
“history.forward()”;</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>143: How will you determine whether the browser has cookies enabled?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The browser status can be determined using cookieEnabled
function of navigator object. If cookies are enabled returns true, else false.</p>

<h4>Example:</h4>
<pre>If(navigator.cookieEnabled)
document.write(“Enabled”);
else
document.write(“Not Enabled”);</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>JAVASCRIPT AND HTML</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>144: How can you change the font size of an Element in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<pre>document.getElementById(elementId).style.fontSize = “12”;</pre>

<p>In this case, JavaScript and CSS are very similar, because the CSS style
rules are laid on top of the DOM.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>145: How can you submit a form using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>This can be done using document.form[0].submit(), where 0 represent the
index of the form in the page. If there are more than one form in the page,
then the first form has index 0, the second form has index 1 and so on.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>146: How can you set the background color of an HMTL document?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>This can be easily done using document.bgcolor = “color”, where color can
be the name of a color – e.g. red, black, or it can represent the code of the
color – e.g. #00FF34.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>147: Name the Boolean operators in JavaScript.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The Boolean operators in JavaScript are: ‘&&’ - AND operator, ‘||’ – OR operator ‘!’ - 
NOT operator.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>148: How can we determine the state of a checkbox in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
<pre>var isChecked = window.document.getElementById(elementId).checked – isChecked</pre>
<p>is the name of the variable where the true or false value will be
stored. ElementId represents the id of the checkbox element. If the
checkbox is checked this will return true, otherwise false.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>149: How can you create an HTML button and what is the event called when the button is pressed?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>An HTML button can be created like this: &lt;input type=”button”&gt; or
&lt;button type=”button”&gt; and the event is “onclick”</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>150: How will you make loading of JavaScript code after Html by the browser?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>By “defer” script we can load JavaScript code after Html. It informs the
browser to load all html codes before JavaScript. So the code inside the
defer script gets executed only when the page is entirely parsed. It can use
on both external and inline scripts.</p>

<h4>Example:</h4>
<pre>&lt;script type=’text/javascript’ src=’a1.js‘ defer=’defer’&gt;&lt;/script&gt;</pre>
<p>Here loading of a1.js takes place after all html code has been parsed.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>151: Which popup allows the user to enter the input?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Prompt box allows the user to enter the input. It provides the user with text
box for input and two buttons (“ok and cancel”). On selecting “Ok”, it
returns true otherwise false.
Example:
var a1= prompt(“content1”,”myDefault_val”);
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>152: What are the ways to display the message on screen?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
a) Using write method.
Eg: document.write(“hello”);
b) Using getElementById.
Eg: function disp(text) {
var m1 = document.getElementById("my_disp");
m1.innerHTML = text;
return true;
}
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>153: How will you reload the page from server using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using reload() we can reload a page. It is a function of location object that
contains the details of present url. It takes either true or false as argument.
Default argument is false. When set to false, reloads the page from cache.
Otherwise ask the browser to load the page from server.</p>
<h4>Syntax:</h4>
<p>Window.location.reload(value);</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>154: How will you display large tables effectively in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using fixed width table we can display large tables effectively. Fixed width
tables are provided by the browser based on the width of the columns in the
first row, ensuring faster display.
<h4>Advantage:</h4>
<p>No need for the browser to wait till all data is received to infer
the best width.</p>
<h4>Syntax:</h4>
<p>In css,set “table-layout:fixed”</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>155: How will you create pop window using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>It can be created as below:
a) window.open(): opens a new browser window

<h4>Syntax:</h4>
Window.open(page_Url, window_ name,properties,replace);
For pop window,replace is always set to false.
b) window.showDialogBox(): creates a modal dialog box
Syntax:
window.showDialogBox(page_url,window_name,properties);
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>156: How will you fix the errors that make the JavaScript engines difficult to perform optimization?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using “Strict Mode” which makes the code run faster than the code without
strict mode such errors could be fixed. To enable strict mode, insert ‘use
strict mode’ before the code. It takes care of following functions:
a) Duplications are not allowed
b) If Deprecated languages is used, throws error
c) It denounces ‘with’ statement
d) Assign to read-only variables are not allowed
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>157: How will you make secure JavaScript code?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Using Strict Mode. The value passed with the “this” (keyword) to a
function will not be changed in strict mode

b) When a function is in strict mode, fn_name.arguments and
fn_name.caller throws error when tried to get or set
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>158: How will you add the external JavaScript file?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>External JavaScript file should be saved with an extension ”.js” and needs
to be imported to the html file by adding that file’s path to the “src”
attribute of &lt;script&gt; tag.</p>

<h4>Example:</h4>
<pre>
&lt;html&gt;
&lt;head&gt;
&lt;script src=”aa.js”&gt;&lt;/script&gt;
&lt;/head&gt;
&lt;body&gt;...&lt;/body&gt;
&lt;/html&gt;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>159: Is it possible to break up a string in a JavaScript code?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Yes. Using backslash”\”, a text can break up in a code.</p>

<h4>Example:</h4>
<pre>
document.write(“Break up a code”);
document.write (“Cannot break like this”); // This is not possible.
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>160: What is the use of “wait” property in cursor style?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Wait sets the cursor in wait state when the request is on process. Type of
cursor can be set or returned by using “cursor property”. Some of the type
of cursor are:<br>
a) default: default cursor<br>
b) wait: loading symbol or hourglass<br>
c) auto: browser default cursor<br>
d) help: arrow with a question mark symbol</p>
<h4>Syntax:</h4>
<pre>
myobject.style.cursor=”my_value”;
eg: myobject-window,document, my_value-wait,auto,help...
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>161: What are the properties that can be set in the background properties?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) color: sets the bgcolor<br>
b) image: sets the bgimage<br>
c) repeat: repeats the bgimage<br>
d) attachment: makes the image fixed or scrolls with the page<br>
e) position: sets the starting position of an image</p>

<h4>Syntax:</h4>
<pre>
my_object.style.background=”my_value”;
// my_object=>window,document,..
// my_value=>color,image,reappear,attachment,position
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>162: What are the ways to set the background color?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The background color can be set in the following two ways:</p>
<ol>
  <li>a) Using bgColor
<pre>
my_obj.bgcolor=”my_color”
my_obj
document
my_color
colors,color value
</pre></li>
  <li>b) Using background
<pre>
my_obj.style.backgroundColor=”my_value”;
my_obj
document
my_value=color,image,reappear,attachment,position
</pre></li>
</ol>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>163: How will you add JavaScript files dynamically?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>By creating a new script element file and append it to the document, we can
add JavaScript files dynamically.
Example:
var head_elemt=document.getElementByTagName(“....”); //pass tag name
like”head”
var my_script=document.createElement(‘...’); //pass type as script
my_script.type=’text/javascript’;
my_script.src=’www.abc.co/ab.js’;
head_elemt.appendChild(my_script);
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>164: How will you get the current “x and y” co-ordinate value of the window when it is scrolled?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Using onscroll. It executes when the window is scrolled<br>
b) pageXOffset and pageYOffset are used to get the co-ordinate value</p>
<h4>Example:</h4>
<pre>
window.onscroll=function(){
var xvalue=window.pageXOffset ;
document.write(xvalue);}
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>165: What are the methods to create remote window?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Using custom property<br>
Secondary window:<p>
<pre>
windw2=window.open(“remote_win2”);
windw2.maker=self; //“self” gives the current window
</pre>
<p>Remote window:</p>
<pre>
function remote_wind2(link2){
maker.location=link2;
}
&lt;input type=”button” value=”Address” onclick=remote_wind2()&gt;
</pre>
<p>b) Using opener property</p>
<pre>
function remote_windw2(link1){
window.opener.location=link;
}
&lt;input type=”button” value=”Address” onclick=remote_windw2()&gt;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>166: How will you get the height of the browser window?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
a) Using availHeight property of the screen object.<br>
b) Gives the height of the browser window excluding the taskbar
height,etc..</p>
<h4>Example:</h4>
<pre>document.write(“Height:” + screen.availHeight);</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>167: How will you get the language code of the linked page?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using hreflang property of the anchor object we can get the language code
of the linked page. Anchor object creates a link to another page or
document.</p>
<h4>Example:</h4>
<pre>my_anchor_object1.hreflang;</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>168: How would you input a file?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using FileUpload Object we can input a file. The type should be specified
as “file” in the <input> tag. It creates the fileupload object that opens the
file dialog box on clicking the button.</p>
<h4>Example:</h4>
<pre>&lt;input type=”file”&gt;</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>JAVASCRIPT FORMS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>169: What is the importance of the “name” attribute of a <form> tag?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>When a Form object is created, the name attribute is stored as an element in
the form[] array of the Document object, and it is also stored in the
properties of the Document objects. So, after defining a <form
name=”formName”>, it will be easy to refer the Form object using
document.formName instead of document.form[0]. This attribute has
nothing to do with submitting the form.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>170: What are the event handlers of the form element?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
The following event handlers are supported by form elements: onclick,
onchange, onfocus, onblur.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>171: What does “onchange” event handler do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>This event handler is triggered when the user enters text or selects an
option, changing in this way the value represented by the element. Button
and other related elements do not support this event handler because they
don't have a value that can be edited. This event it is triggered when the
focus is lost and it is moved to another form element.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>172: What is a “cookie”?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>A cookie is a named data stored by the web browser and associated with a
particular web page or web site. They were originally designed for the
server-side programming and they are implemented as an extension to the
HTTP protocol. The cookie data is transmitted between the client and the
server and the server-side scripts can read and write cookie values that are
stored on the client. In JavaScript, cookies are manipulated using “cookie”
property of the Document object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>173: What does the “new” operator do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>The “new” operator creates a new object, that has no properties, and then it
invokes the function passing the new objected created as the value of “this”
keyword. The function that uses the “new” operator is called “constructor
function” or just simply “constructor”.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>174: What does <optgroup> tag do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>It is used with select statement to group the related options in the drop
down list. It will be useful to display long list.</p>
<h4>Example:</h4>
<pre>
&lt;select&gt;
&lt;optgroup label=”JAVA”&gt;
&lt;option value=”hibernate1”&gt;Hibernate&lt;/option&gt;
&lt;option value=”struts1”&gt; Struts &lt;/option&gt;
&lt;/optgroup&gt;
&lt;optgroup label=”WEBSERVICE”&gt;
&lt;option value=”soap1”&gt;SOAP&lt;/option&gt;
&lt;option value=”xml1”&gt; Xml &lt;/option&gt;
&lt;/optgroup&gt;
&lt;/select&gt;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>175: Compare between session state and view state.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>176: Which function is better for fast execution: window.onload or window.onDocumentReady?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>window.onDocumentReady is better for fast execution because it executes
the code once DOM is loaded by the browser and will not wait for the
object such as images to be loaded whereas onLoad executes only when the
browser loads DOM and all other resources such as images gets loaded.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>177: What is the purpose of “visibility” property in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) “Visibility”: Makes the element either visible or invisible<br>
b) ”collapse”: Used to hide the elements in a table<br>
c) ”inherit”: Takes the values from the parent element</p>
<h4>Example:</h4>
<pre>
my_elemt.style.visibility=”my_val”;
my_val
visible,hidden,collapse,inherit
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>178: What are the ways to make an element visible/hidden?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>a) Using display property</p>

<pre>
my_elemt.style.display=” ”; //visible
my_elemt.style.display=”none”; //hidden
</pre>

<p>b) Using visibility property</p>

<pre>
my_elemt.style.visibility=”visible”; //visible
my_elemt.style.visibility=”hidden”; //hidden
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>179: How will you disable the html form fields, for instance password field?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using disabled property of a password object.</p>

<h4>Example:</h4>
<pre>document.getElementById(“Field_Id”).disabled=true;</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>180: How will you select the contents in the text field, say password?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using select function of password object, we can select the contents in text field.</p>

<h4>Example:</h4>
<pre>document.getElementById(“Field_Id”).select();</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>181: How will you display the id of the form and the name attribute of the hidden element?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using “form” and name property of hidden object, we can display the id of
the form and the name attribute of the hidden element.</p>

<h4>Example:</h4>
<pre>
var form_id1= document.getElementById(“my_elemt_id”).form.id;
var name_id2= document.getElementById(“my_elemt_id”).name;
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>182: How will you get the last row from a table in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using tFoot property of a table object we can get the last row from a table.
The last rows of tables in Html can be combined using the tfoot element.</p>

<h4>Example:</h4>

<pre>
my_table_objects.tFoot;
my_table_objects
document object,getElementById property
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>183: How will you create and delete caption to a table?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>

<p>Using createCaption and deleteCaption function of the table object.</p>

<h4>Example:</h4>

<pre>
my_table_objects.createCaption(); //create
my_table_objects.deleteCaption(); //delete
my_table_objects
document object,getElementById
property
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>184: How will you create a text area and make it read-only?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
a) Using textarea object</p>

<h4>Example:</h4>
<pre>&lt;textarea id=”my_txt” cols=”22”&gt;
My_text
&lt;/textarea&gt;
</pre>
<p>b) Using readOnly property of textarea object</p>
<h4>Example:</h4>
<pre>
my_table_objects.readOnly=”my_value1”; //delete
my_table_objects
document object,getElementById property
my_value1
true
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>185: How will you change the caption display position of a table?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:

<p>Using captionSide property of the style object we can change the caption
display position of a table.</p>

<h4>Example:</h4>
<pre>
my_obj1.style.captionSide=”values”;
my_obj1
document object,getElementById property
values top/bottom
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>JAVASCRIPT CONSTRUCTORS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>186: What does a JavaScript constructor do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h4>Answer:</h4>
The constructor initializes the newly created object and sets any properties
that need to be set before that object is used. You can easily define a
constructor function, by writing a function that adds properties to “this”
operator.</p>
Example:
// define the constructor
function circle(r){
this.radius = r;
}
//invoke the constructor to create a circle object:
var circle1 = new circle(3); // we pass the radius value to the constructor so
that it will initialize the new object appropriately.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>187 What is the value that the constructor function returns?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Typically, the constructor does not return any values. They simply initialize
the object passed as the value of “this” operator and return nothing.
Anyway, the constructor can return an object value, but in this case the
returned object becomes the value of the “new” expression and the object
that was the value of this is simply not taken into account.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>188: How many types of common object methods can we find in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>We have three types of object methods: the toString|() method; the
valueOf() method and comparison method.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>189: How does class hierarchy manifest themselves in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Java and C++ have an explicit concept of the class hierarchy; so any class
can be extended or sub-classed so that subclass that results can be inherited.
JavaScript supports prototype inheritance instead of class-based inheritance
so the Object class is the most generic with all other classes as specialized
versions of it or subclasses.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>190: What does “overriding method” mean?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>If a subclass defines a method that has the same name as the method in the
superclass it is called overriding that method. This is a common thing to do
when creating subclasses of existing classes. For example when toString()
method is defined, the toString() method of Object is overridden.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>191: How can you create an XML document in Firefox using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>We can create an empty XML Document in Firefox and related browsers with 
document.implementation.createDocument() which is a DOM Level 2 method.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>192: How are images accessed from JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Images can be referred using document.images[0] // for the first images,
document.images[1] and so one for the next images. Once the image is
accessed, you can perform different tasks on them.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>193: Where is the arguments() array placed in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It is placed and defined only within a function body. Within the arguments
of a body arguments refers to Arguments object for the function.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>194: Which are the properties of the arguments object in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The properties of the arguments object are callee and length. All values that
are passed as arguments become array elements of the arguments object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>195: What happens when a function is invoked with the arguments object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Arguments object is created for it and the local variable arguments are
initialized to refer that arguments object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>MISCELLANEOUS ARGUMENTS, FUNCTIONS AND METHODS IN JAVASCRIPT</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>196: What does arguments.callee do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The arguments.callee refers to the currently running function and it
provides a way for an unnamed function to refer to itself.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>197: What does arguments.length do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The arguments.length specifies the number of arguments that are passed to
the current function; it only specifies the number of arguments actually
passed and not the expected number.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>198: What other JavaScript method you know that is similar with shift() method?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Other method similar with shift() is Array.pop(), the only exception is that it
operates on the beginning of an array rather that the end.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>199: How can you remove a page from the browser history?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>If the programmer wants to remove the current page from the browser history, it can simply 
use location.replace() method. Invoking this method causes the browser to request a page 
through a GET method just like a regular web page.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>200: How can you pass data between pages using cookies?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>In this case cookies.js library can be used with onunload event handler of
one page to store 1 to 20 name/value pairs on the user's machine. In the
second document, the onload event handler is used to retrieve the cookie
data and assign the value to a text input field with the same name located on
the second page.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>201: What is the difference between resizeTo() and resizeBy() methods?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Both the given methods are applicable to window object. In case you want
to resize the window to a specific pixel size, resizeTo() method is the most
appropriate. To increase or decrease the size of the window by a fixed pixel
amount, you can use resizeBy() method.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>202: What is the difference between moveTo() and moveBy() methods?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Both the methods are applicable to window object. The first method,
moveTo() is used to move the window to a screen coordinate point, by the
other hand, the moveby() method shifts the position of the window by a
known pixel amount.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>203: How can a window that is buried beneath other windows be brought back to the front?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>In this case, for any window to which you have a valid reference, the
focus() method must be invoked.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>204: What happens when a string argument is passed with the Date() constructor in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>If one string argument passes with the Date() constructor it results in the
string being a representation of a date in the format that is accepted by the
Date.parse() method.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>205 Which are the arguments of the Date() constructor in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The date() constructor arguments are: milliseconds1, datestring, year,
month, day, hours, minutes, seconds and milliseconds2 (optional argument).</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>206: What does URIError indicate in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The URIError indicates that one or more escape sequences in URI are
malformed and they cannot be correctly sequenced.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>207: What does the encodeURIComponent function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It is a global function that returns an encoded copy of the string argument.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>208: What does the string argument do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The string argument is a string that simply contains a portion of a URI or
other text that has to be encoded.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>209: What is and what does the escape() function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The escape() function is a global function that returns a new string that
contains an encoded version of s; the string s by itself is not modified.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>210: What does the apply() function do in JavaScript and which are its arguments?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The apply() function invokes the specified function and treats it like it were 
a method of thisobj argument passing it then the arguments contained by the 
args array.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>211: What does the getClass() function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The getClass() function takes a JavaObject object as an argument and return
the JavaClass object of the respective JavaObject.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>212: What is Infinity in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Infinity is a global property that contains special numeric value that
represents positive infinity; it cannot be deleted by the delete operator.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>213: What does the exec() method do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The exec() is the most powerful pattern-matching method of RegExp and
String. It searches string for text that matches the regexp and if it finds a
match returns an array of results; if not it returns null.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>214: What happens when the exec() method is invoked on a nonglobal pattern?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The exec() performs a search and then returns the same result as
String.match() would.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>215: Does exec() include full details of every match even if regexp is not global?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It is different in this regard to String.match() which return less information
when used with global patterns.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>216: What is an anchor in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>An anchor is a named location within an Html document that is created with 
an &lt;a&gt; tag that has an attribute specified.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>217: What does the focus() method do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The focus() method scrolls the document so that the anchor location is
visible; it is created by any standard HTML <a> tag that contains a name
attribute.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>218: Is JSObject a JavaScript object?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>No. JSObject is a Java class that cannot be used in any JavaScript
programs; it invokes the JavaScript methods into Java.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>219: What does the call() method of JSObject class do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It invokes a name method of the JavaScript object represented by the
JSObject; the arguments are passed to the method as an array of Java
objects, then the return value of the JavaScript method is returned as a Java
object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>220: What does the eval() method of the JSObject do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It evaluates the JavaScript code that is contained within a string s in the
context of the JavaScript object. Its behavior is similar to that of the eval()
method of JavaScript.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>221: What does the getSlot() method of the JSObject do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It reads and returns the value of an array element that is specified at the
index of a JavaScript object.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>222: What does the removeMember() method of the JSObject do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It deletes a named property that belongs to the JavaScript object represented
by the JSObject.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>223: What does the setMember() method of the JSObject do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>This method is the opposite of removeMember in that it sets a value of a
named property of a JavaScript object from Java.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>224: What does the toString() method of JSObject do?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It invokes the toString() of the JavaScript object and returns the result of
that method.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>225: What does the (n) argument represent in isFinite(n) and what does it return?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The (n) argument is the number that is to be tested and if n can be converted
or is a finite number return true and false or NaN if n is positive or negative
infinity.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>226: What does the isNaN() function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It tests its arguments to see if it is the value of Nan, which is an illegal number.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>227: What does the setYear() function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>It sets the year field of a specified date object with a special behavior for
years between 1900 and 1999.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>228: What does the join() method do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Put in all the elements of the array into a string separated by the specified
separator. Default separartor is comma “,”.</p>
<h4>Example:</h4>
<pre>
var fourwheelers = [“Car”,”Bus”,”Lorry”] ;
document.write(fourwheelers.join(“-”));
”Car-Bus-Lorry”
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>229: How will you pop the last element from an existing array?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Using pop() function we can pop the last element from an existing array. It
removes and returns the last element of an array. Length of the array will
decrease by 1.</p>
<h4>Example:</h4>
<pre>
var no=[1,2,3];
document.write(no);
”1,2,3”
document.write.(no.pop() +”<br>”);

”3”
document.write(no);
”1,2”
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>230: How to pop the first element from an existing array?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Using shift() function we can pop the first element from an existing array. It
removes and returns the first element of an array. Length of the array will
decrease by 1.</p>
<h4>Example:</h4>
<pre>
var no=[1,2,3];
document.write(no);
”1,2,3”
document.write.(no.shift() +”<br>”);
”1”
document.write(no);
”2,3”
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>231: How will you add one or more elements to the end of the existing array?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Using push() function we can add more elements. It adds the new items to
the end of the array and returns its length.</p>
<h4>Example:</h4>
<pre>
var no=[1,2,3];
document.write(no);
”1,2,3”
document.write(no.push(5));
”4”
document.write(no);
”1,2,3,5”
</pre>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>232: How will you add one or more elements to the beginning of the existing array?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using unshift() function we can add more elements. It adds the new items
to the beginning of the array and returns its length.
Example:
var no=[1,2,3];
document.write(no);
”1,2,3”
document.write(no. unshift (5));
”4”

document.write(no);
”5,1,2,3”
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>233: How will you reverse the elements in an array?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using reverse() function without creating new array.
Example:
var no=[1,2,3];
document.write(no);
”1,2,3”
document.write(no.reverse());
”3,2,1”
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>234: What does the Array.slice(start,end) method do in JavaScript and how to retrieve 
the elements within the selected position in an array?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Its returns the array object containing the elements starting from the
specified start value till the element before the end value. When a negative
value is used for the start or end values, that gets added to the length of the
array and returns the elements within that position.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>235: What does the Array.sort() method do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
a) Default sort(): used to sort the alphabets in ascending order
b) reverse() is used with the sort(): Used to sort the alphabets in
descending order
c) To sort the numbers, some functions are passed as arguments in sort()
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>236: What is encodeURI( ) and encodeURIComponent( )?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
a) Used to encode the given uri
b) encodeURI() encodes the special characters except “ : @ $ # = & / + ? “
c) encodeURIComponent encodes all the special characters including “ :
@ $ # = & / + ? “
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>237: What is decodeURI( ) and decodeURIComponent( )?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
a) Used to decode the given encoded uri. decodeURI() decodes the special
characters except “ : @ $ # = & / + ? “
b) decodeURIComponent denotes all the special characters including “ : @
$ # = & / + ? “
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>238: What does the splice( ) function do in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Adds or remove elements to/from an existing array and return the removed
elements.
array.splice(index,no of items to be removed,new items1,new items2...new
itemn);
Example:
var no=[1,2,3,4,5];
document.write(no);
”1,2,3,4,5”
document.write(no. splice (1,2,9,10));
”2,3”
document.write(no);
”1,9,10,4,5”
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>239: How will you print the current window using JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Using window.print() function to print the contents of the specified window.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>240: How will you get default value when an argument is not passed in calling function?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
By Shorthand assignment. It checks whether the passed argument contains a
value.

Example:
function add1(a1,a2){
var b1=a1 || 1;
b1=5
var b2=a2 || 2;
b2=2
return b1+b2;
7
}
add1(5);
Here, since the first argument is only passed, it is treated as true hence”5”
gets assigned to b1. Since the Second argument is not passed, it is treated as
undefined value (i.e.) false hence the default value gets assigned.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>241: How will you encode and decode a string?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
a) Using escape() and unescape()
b) escape(): Encodes the string and special characters except “ + * - _ . @ /
” . It converts the non Ascii codes to two or four digit hex format
c) unescape(): decodes the encoded string
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>242: How will you pass a function as argument to another function?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using callback. A function that is passed as a argument to another function
gets a reference called “Callback”. The callback functions gets executed
only after the execution of called function.
Example:
function oven(time,callback){
document.write(“Started at” +time+ “<br>”);
callback();
}
oven(5,function(){
document.write(“Stopped”);});
Output:
Started at 5
Stopped
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>243: What is the need for callback function?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
When a function is called, execution of the function takes place which will
return some value. If the execution time will be longer for the function to
return a value, for instance, when it may have to wait for some input from
another function or user, it needs to be implemented asynchronously using
callback function.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>244: How will you get a substring from a string in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
a) substring(): Retrieves the string starting from the start value till end
value. White space are included
Syntax: substring(start_value,end_value);
b) substr(): Retrieves the string starting from the start value till the length
specified
Syntax: substr(start_value,leng);
Example:
var a=”color my world”;
document.write(substring(3,7); // r my
document.write(substr(3,7); // o my wo
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>245: How will you get the function (fn1) which recently called the current function (fn2)?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using “fn2.caller” we can get the fn1 info. If the control of the program is
in the fn2(), it will return the function (fn1) by which fn2 is recently called
by using fn2.caller.
“fn2.arguments” gives the arguments passed to the fn2.
Example:
function fn_2(){
use strict mode;

fn_2.caller;
fn_2.arguments;
}
function fn_1(){
fn_2();
}
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>246: How will you execute the page that is about to be unloaded, before the execution of onload()?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using onbeforeunload we can execute the page that is about to be unloaded.
The “onunload” function occurs when the page is closed or navigating to
another page. Hence onbeforeunload alerts the user about navigation before
“onunload”.
Example:
window.onbeforeunload=alert_msg();
function alert_msg(){
return “Message to be displayed to the user.”;
}
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>247: How will you find whether the window is closed or not?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using closed property we can check the status of the window. It returns
“true” if the window is closed else returns “false”.
Example:
if(window.opener.closed)
document.write(“closed”);
else
document.write(“open”);
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>248: How will you call a function repeatedly for a particular interval of time?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Using setInterval function we can repeatedly call a function for a period of
time.. It also clears the timer by returning unique id which will be passed as
a parameter for clearTimer.
Example:
setInterval(my_funct_1(),444);
my_funct_1
function to be called
444
specified_ interval
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>249: What is the difference between test and exec function?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
a) Both functions are used to search the particular pattern.
b) test function returns a Boolean value and exec function returns the found
value.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>JAVASCRIPT DESIGN PATTERNS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>250: What is a Pattern and explain about design patterns in software programming?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
A Pattern is often a theme of recurring objects or events. It could be a
model or template that could be used to develop or generate a working
component. In software development, a pattern is a solution to a common
problem. A pattern is more of a best practice or a template which could be
used to solve various categories of problems.
Design pattern is a reusable architecture or program that could be reused
during the development of any software which usually speed up the
development activity. Reusing the Design Patterns always helps to prevent
subtle issues which could cause major concerns. Reusing design patterns
also improves code readability for architects and coders.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>251: Why is it important to identify patterns?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Identifying patterns is very important because:
a) Patterns always help us to write better code with proven best practices.
There is no need to reinvent the wheel.
b) Patterns always provide an abstraction level – When you build a more
complex problem, patterns helps not to think of the low-level details but by
default includes the low-level details with self-contained blocks.

c) Patterns often improves the communication between software developers
and their teams even when they don’t communicate face to face.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>252: What is Singleton Pattern and what is its importance in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
When the number of instances for a particular object is limited to just one,
then that single instance is called the Singleton.
Following are the importance of Singleton:
a) Singletons are particularly useful when system-wide actions are needed
to be coordinated from one single location. For example: consider database
connection pool. The database connection pool often manages creation,
destruction, and ensures that the database connections are never lost for the
entire application.
b) Singletons mainly reduces the need for the global variables. In
JavaScript, global variables are important because it limits the variable
name collisions and namespace pollution.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>253: How will you create singleton in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
We can create Singleton by creating a simple object using the object literal.
For Example:
var mySingletonObj = {
myProp: 'My Value'

};
In the above code snippet,
mySingletonObj is the simple object created and
myProp: ‘My Value’ is the object literal.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>254: How will you create 2 equal objects in JavaScript?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
We could create 2 equal objects with the help of new keyword. For
example:
var myObject1 = new Mars();
var myObject2 = new Mars();
myObject1 === myObject2 //This returns true
In the above code snippet, myObject1 is created only the first time when the
constructor Mars is called. The second time (and third, fourth, and so on)
the same myObject1 object is returned. This is why myObject1 ===
myObject2 — since they are mainly two references that are pointing to the
same exact object.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>255: What is the purpose of Factory pattern?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
The Factory Pattern similar to other patterns is also used to create objects.
But here are the two main purposes:
a) Perform repeating operations while setting up similar objects

b) Create objects without actually knowing the specific object type during
compile time
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>256: How will you create a Factory pattern?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
In JavaScript, Factory pattern could be created as follows:
var myCorolla = MakeCar.factory('Compact');
var myIkon = MakeCar.factory('SUV');
In the above code snippet, we have a method that accepts a string at runtime
and then creates and returns objects of the requested type. There are no
constructors used with new or any object literals, but just a function that
creates objects based on a type identified by a string.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>257: Explain about Iterator pattern.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
In Iterator pattern, the object holds aggregate data. The data could be stored
in a complex structure, and we have to provide access to each element. The
object consumer does not need to know the data structure.
For Example:
var myElement;
while (myElement = myData.next()) {
console.log(myElement);
}

In the above code, myData has collection of data and each element of them
could be accessed by simply calling the next() method in a loop.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>258: Explain about Decorator Pattern.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
In Decorator pattern, a new or additional functionality could be added to an
object dynamically during runtime. Objects are mutable in JavaScript, so
adding a functionality to an object could be done quite easily.
The main feature of the decorator pattern is configuration and
customization of the existing object.
var mySale = new Sale(1000); // the price is 1000 Rupees
mySale = mySale.decorate('tax'); // add tax
mySale.getModifiedPrice(); // "Rs1012.88"
In the above code, we decorate the code (add additional
functionality) with a tax for the mySale object and then get the
modified price.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>259: What is the importance of Strategy Pattern?</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
The strategy pattern enables you to select algorithms at runtime. The clients
of your code can work with the same interface but pick from a number of
available algorithms to handle their specific task.

For example, consider the problem of solving form validation using strategy
pattern. You can create one validator object with a validate() method. This
is the method that will be called regardless of the concrete type of form and
will always return the same result. The result will be list of data that didn’t
validate and return any error messages.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>260: Explain data validation using strategy pattern.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Let’s say you have the following piece of data, probably coming from a
form on a page, and you want to verify whether it’s valid:
var myData = {
firstName: "Spider",
lastName: "Man",
myAge: "UnKnown",
userName: "spider_man"
};
We need to configure the validator first and set the rules of what you
consider to be valid and acceptable. Let’s say we accept anything for first
name, the age should be a number and the username to have letters and
numbers and no special characters. The configuration will be something
like:
validator.config = {
firstName: 'isNonEmpty',
myAge: 'isNumber',

userName: 'isAlphaNum'
};
Now that the validator object is configured to handle data, we call the
validate() method and print any validation errors to the console:

validator.validate(myData);
if (validator.hasErrors()) {
console.log(validator.messages.join("\n"));
}

This could print the following error messages:
Invalid value for *age*, the value can only be a valid number, e.g. 1, 3 10, etc.,
Invalid value for *username*, the value can only contain characters and
numbers, and no special symbols
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>261: Explain Facade pattern with example.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
The facade is a simple pattern; it provides an alternative interface to an
object. It’s a good design practice to keep the methods short and not have
them handle too much work.
For example, when handling browser events, we have the following methods:

stopPropagation(); //Traps the event and doesn’t let it bubble up to the parent nodes
preventDefault(); //Doesn’t let the browser do the default action (for example, following a link or submitting a form)

The above are two different methods with unique purpose, but the above
two methods are often called together at the same time. So rather than
duplicating the above two method calls all over the application, we could
create a façade method and that invokes both the methods.

var myEvent = {
stop: function (e) {
e.preventDefault();
e.stopPropagation();
}
};

In the above code, myEvent is a Façade that invokes 2 methods when it’s triggered.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>262: Explain about Proxy Pattern.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>In Proxy design pattern, one object acts as an interface to another object.
The proxy sits between the client object and the object itself and protects
access to that object.
Proxy pattern may look like an overhead but it’s useful to improve the
performance. The proxy serves as a guardian of the object and tries to have
the real subject do as little work as possible.</p>
<p>Network request is one of the expensive operation you could perform in
web application. Proxy pattern is useful to make this expensive operation
and it’s necessary to combine HTTP requests as often as possible.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>263: Explain about Mediator pattern.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Irrespective of the applications are small or large, applications are made of
unique objects. All these unique objects need a way to communicate among
themselves in a manner that doesn’t affect maintenance and the ability to
safely change a part of the application without breaking the rest of it. This is
where Mediator pattern plays an important role.</p>

<p>When the application grows, we add objects one by one and it grows
rapidly. Then, during refactoring, objects are removed and rearranged.
When objects know too much about each other and communicate directly
by calling each other’s methods and change the properties, it leads to
undesirable tight coupling.</p>

<p>When objects are closely coupled, it’s not easy to change one object without
affecting many others. Then even the simplest change in an application is
no longer trivial, and it’s virtually impossible to estimate the time a change
might take. The mediator pattern alleviates this situation by promoting
loose coupling and helping to improve maintainability.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>264: Explain about Observer Pattern.</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>The Observer pattern is mainly used in client-side JavaScript programming.
All the browser events like key-press, mouse-over, and so on are examples
of Observer pattern.</p>
<p>Another name for this pattern is custom events since they were created
programmatically as opposed to the ones that the browser triggers.
This pattern is also called as subscriber / publisher pattern. The main
motivation for this pattern is to promote loose coupling. Instead of one
object calling another object’s method, an object subscribes to another
object’s specific activity and gets notified.</p>
<p>The subscriber is also called as observer. The object being observed is
called as subject or publisher. The publisher calls or notifies all the
subscribers when an event occurs and this pass a message in the form of an
event object.</p>


<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>HR INTERVIEW QUESTIONS</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<p>Review these typical interview questions and think about how you would
answer them. Read the answers listed; you will find best possible answers
along with strategies and suggestions.</p>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
1: Tell me about a time when you worked additional hours to finish a project.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
It's important for your employer to see that you are dedicated to your work,
and willing to put in extra hours when required or when a job calls for it.
However, be careful when explaining why you were called to work
additional hours – for instance, did you have to stay late because you set
goals poorly earlier in the process? Or on a more positive note, were you
working additional hours because a client requested for a deadline to be
moved up on short notice? Stress your competence and willingness to give
110% every time.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
2: Tell me about a time when your performance exceeded the duties and requirements of your job.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
If you're a great candidate for the position, this should be an easy question
to answer – choose a time when you truly went above and beyond the call
of duty, and put in additional work or voluntarily took on new responsib-
ilities. Remain humble, and express gratitude for the learning opportunity,
as well as confidence in your ability to give a repeat performance.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
3: What is your driving attitude about work?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
There are many possible good answers to this question, and the interviewer
primarily wants to see that you have a great passion for the job and that you

will remain motivated in your career if hired. Some specific driving forces
behind your success may include hard work, opportunity, growth potential,
or success.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
4: Do you take work home with you?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
It is important to first clarify that you are always willing to take work home
when necessary, but you want to emphasize as well that it has not been an
issue for you in the past. Highlight skills such as time management, goal-
setting, and multi-tasking, which can all ensure that work is completed at
work.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
5: Describe a typical work day to me.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
There are several important components in your typical work day, and an
interviewer may derive meaning from any or all of them, as well as from
your ability to systematically lead him or her through the day. Start at the
beginning of your day and proceed chronologically, making sure to
emphasize steady productivity, time for review, goal-setting, and
prioritizing, as well as some additional time to account for unexpected
things that may arise.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
6: Tell me about a time when you went out of your way at your previous job.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Here it is best to use a specific example of the situation that required you to
go out of your way, what your specific position would have required that
you did, and how you went above that. Use concrete details, and be sure to
include the results, as well as reflection on what you learned in the process.
7: Are you open to receiving feedback and criticisms on your job performance, and adjusting as necessary?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
This question has a pretty clear answer – yes – but you'll need to display a
knowledge as to why this is important. Receiving feedback and criticism is
one thing, but the most important part of that process is to then implement it
into your daily work. Keep a good attitude, and express that you always
appreciate constructive feedback.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
8: What inspires you?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
You may find inspiration in nature, reading success stories, or mastering a
difficult task, but it's important that your inspiration is positively-based and
that you're able to listen and tune into it when it appears. Keep this answer
generally based in the professional world, but where applicable, it may
stretch a bit into creative exercises in your personal life that, in turn, help
you in achieving career objectives.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
9: How do you inspire others?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
This may be a difficult question, as it is often hard to discern the effects of
inspiration in others. Instead of offering a specific example of a time when
you inspired someone, focus on general principles such as leading by
example that you employ in your professional life. If possible, relate this to
a quality that someone who inspired you possessed, and discuss the way
you have modified or modeled it in your own work.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
10: What has been your biggest success?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Your biggest success should be something that was especially meaningful to
you, and that you can talk about passionately – your interviewer will be
able to see this. Always have an answer prepared for this question, and be
sure to explain how you achieved success, as well as what you learned from
the experience.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
11: What motivates you?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
It's best to focus on a key aspect of your work that you can target as a
“driving force” behind your everyday work. Whether it's customer service,
making a difference, or the chance to further your skills and gain
experience, it's important that the interviewer can see the passion you hold
for your career and the dedication you have to the position.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
12: What do you do when you lose motivation?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
The best candidates will answer that they rarely lose motivation, because
they already employ strategies to keep themselves inspired, and because
they remain dedicated to their objectives. Additionally, you may impress
the interviewer by explaining that you are motivated by achieving goals and
advancing, so small successes are always a great way to regain momentum.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
13: What do you like to do in your free time?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
What you do answer here is not nearly as important as what you don't
answer – your interviewer does not want to hear that you like to drink,
party, or revel in the nightlife. Instead, choose a few activities to focus on
that are greater signs of stability and maturity, and that will not detract from
your ability to show up to work and be productive, such as reading,
cooking, or photography. This is also a great opportunity to show your
interviewer that you are a well-rounded, interesting, and dynamic
personality that they would be happy to hire.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
14: What sets you apart from other workers?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
This question is a great opportunity to highlight the specific skill sets and
passion you bring to the company that no one else can. If you can't outline
exactly what sets you apart from other workers, how will the interviewer
see it? Be prepared with a thorough outline of what you will bring to the
table, in order to help the company achieve their goals.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
15: Why are you the best candidate for that position?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Have a brief response prepared in advance for this question, as this is
another very common theme in interviews (variations of the question
include: “Why should I hire you, above Candidate B?” and “What can you
bring to our company that Candidate B cannot?”). Make sure that your
statement does not sound rehearsed, and highlight your most unique
qualities that show the interviewer why he or she must hire you above all
the other candidates. Include specific details about your experience and
special projects or recognition you've received that set you apart, and show
your greatest passion, commitment, and enthusiasm for the position.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
16: What does it take to be successful?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Hard work, passion, motivation, and a dedication to learning – these are all
potential answers to the ambiguous concept of success. It doesn't matter so
much which of these values you choose as the primary means to success, or
if you choose a combination of them. It is, however, absolutely key that
whichever value you choose, you must clearly display in your attitude,
experience, and goals.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
17: What would be the biggest challenge in this position for you?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Keep this answer positive, and remain focused on the opportunities for
growth and learning that the position can provide. Be sure that no matter

what the challenge is, it's obvious that you're ready and enthusiastic to
tackle it, and that you have a full awareness of what it will take to get the
job done.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
18: Would you describe yourself as an introvert or an extrovert?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
There are beneficial qualities to each of these, and your answer may depend
on what type of work you're involved in. However, a successful leader may
be an introvert or extrovert, and similarly, solid team members may also be
either. The important aspect of this question is to have the level of self-
awareness required to accurately describe yourself.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
19: What are some positive character traits that you don't possess?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
If an interviewer asks you a tough question about your weaknesses, or lack
of positive traits, it's best to keep your answer light-hearted and simple – for
instance, express your great confidence in your own abilities, followed by a
(rather humble) admittance that you could occasionally do to be more
humble.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
20: What is the greatest lesson you've ever learned?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
While this is a very broad question, the interviewer will be more interested
in hearing what kind of emphasis you place on this value. Your greatest
lesson may tie in with something a mentor, parent, or professor once told
you, or you may have gleaned it from a book written by a leading expert in
your field. Regardless of what the lesson is, it is most important that you
can offer an example of how you've incorporated it into your life.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
21: Have you ever been in a situation where one of your strengths became a weakness in an alternate setting?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
It's important to show an awareness of yourself by having an answer for this
question, but you want to make sure that the weakness is relatively minor,
and that it would still remain a strength in most settings. For instance, you
may be an avid reader who reads anything and everything you can find, but
reading billboards while driving to work may be a dangerous idea.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
22: Who has been the most influential person in your life?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Give a specific example (and name) to the person who has influenced your
life greatly, and offer a relevant anecdote about a meaningful exchange the
two of you shared. It's great if their influence relates to your professional
life, but this particular question opens up the possibility to discuss
inspiration in your personal life as well. The interviewer wants to see that
you're able to make strong connections with other individuals, and to work
under the guiding influence of another person.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
23: Do you consider yourself to be a “detailed” or “big picture” type of person?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Both of these are great qualities, and it's best if you can incorporate each
into your answer. Choose one as your primary type, and relate it to
experience or specific items from your resume. Then, explain how the
other type fits into your work as well.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
24: What is your greatest fear?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Disclosing your greatest fear openly and without embarrassment is a great
way to show your confidence to an employer. Choose a fear that you are
clearly doing work to combat, such as a fear of failure that will seem
impossible to the interviewer for someone such as yourself, with such clear
goals and actions plans outlined. As tempting as it may be to stick with an
easy answer such as spiders, stay away from these, as they don't really tell
the interviewer anything about yourself that's relevant.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
25: What sort of challenges do you enjoy?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
The challenges you enjoy should demonstrate some sort of initiative or
growth potential on your part, and should also be in line with your career
objectives. Employers will evaluate consistency here, as they analyze
critically how the challenges you look forward to are related to your
ultimate goals.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
26: Tell me about a time you were embarrassed. How did you handle it?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
No one wants to bring up times they were embarrassed in a job interview,
and it's probably best to avoid an anecdote here. However, don't shy away
from offering a brief synopsis, followed by a display of your ability to laugh
it off. Show the interviewer that it was not an event that impacted you
significantly.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
27: What is your greatest weakness?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This is another one of the most popular questions asked in job interviews,
so you should be prepared with an answer already. Try to come up with a
weakness that you have that can actually be a strength in an alternate setting
– such as, “I'm very detail-oriented and like to ensure that things are done
correctly, so I sometimes have difficulty in delegating tasks to others.”
However, don't try to mask obvious weaknesses – if you have little practical
experience in the field, mention that you're looking forward to great
opportunities to further your knowledge.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
28: What are the three best adjectives to describe you in a work setting?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
While these three adjectives probably already appear somewhere on your
resume, don't be afraid to use them again in order to highlight your best
qualities. This is a chance for you to sell yourself to the interviewer, and to
point out traits you possess that other candidates do not. Use the most
specific and accurate words you can think of, and elaborate shortly on how
you embody each.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
29: What are the three best adjectives to describe you in your personal life?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Ideally, the three adjectives that describe you in your personal life should be
similar to the adjectives that describe you in your professional life.
Employers appreciate consistency, and while they may be understanding of
you having an alternate personality outside of the office, it's best if you
employ similar principles in your actions both on and off the clock.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
30: What type of worker are you?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This is an opportunity for you to highlight some of your greatest assets.
Characterize some of your talents such as dedicated, self-motivated, detail-
oriented, passionate, hard-working, analytical, or customer service focused.
Stay away from your weaker qualities here, and remain on the target of all
the wonderful things that you can bring to the company.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
31: Tell me about your happiest day at work.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Your happiest day at work should include one of your greatest professional
successes, and how it made you feel. Stay focused on what you
accomplished, and be sure to elaborate on how rewarding or satisfying the
achievement was for you.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
32: Tell me about your worst day at work.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
It may have been the worst day ever because of all the mistakes you made,
or because you'd just had a huge argument with your best friend, but make
sure to keep this answer professionally focused. Try to use an example in
which something uncontrollable happened in the workplace (such as an
important member of a team quit unexpectedly, which ruined your team's
meeting with a client), and focus on the frustration of not being in control of
the situation. Keep this answer brief, and be sure to end with a reflection on
what you learned from the day.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
33: What are you passionate about?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Keep this answer professionally-focused where possible, but it may also be
appropriate to discuss personal issues you are passionate about as well
(such as the environment or volunteering at a soup kitchen). Stick to issues
that are non-controversial, and allow your passion to shine through as you
explain what inspires you about the topic and how you stay actively
engaged in it. Additionally, if you choose a personal passion, make sure it
is one that does not detract from your availability to work or to be
productive.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
34: What is the piece of criticism you receive most often?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
An honest, candid answer to this question can greatly impress an
interviewer (when, of course, it is coupled with an explanation of what
you're doing to improve), but make sure the criticism is something minimal
or unrelated to your career.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
35: What type of work environment do you succeed the most in?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Be sure to research the company and the specific position before heading
into the interview. Tailor your response to fit the job you'd be working in,
and explain why you enjoy that type of environment over others. However,
it's also extremely important to be adaptable, so remain flexible to other
environments as well.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
36: Are you an emotional person?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
It's best to focus on your positive emotions – passion, happiness,
motivations – and to stay away from other extreme emotions that may cause
you to appear unbalanced. While you want to display your excitement for
the job, be sure to remain level-headed and cool at all times, so that the
interviewer knows you're not the type of person who lets emotions take you
over and get in the way of your work.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
37: How do you make decisions?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This is a great opportunity for you to wow your interviewer with your
decisiveness, confidence, and organizational skills. Make sure that you
outline a process for decision-making, and that you stress the importance of
weighing your options, as well as in trusting intuition. If you answer this
question skillfully and with ease, your interviewer will trust in your
capability as a worker.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
38: What are the most difficult decisions for you to make?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Explain your relationship to decision-making, and a general synopsis of the
process you take in making choices. If there is a particular type of decision
that you often struggle with, such as those that involve other people, make
sure to explain why that type of decision is tough for you, and how you are
currently engaged in improving your skills.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
39: When making a tough decision, how do you gather information?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
If you're making a tough choice, it's best to gather information from as
many sources as possible. Lead the interviewer through your process of
taking information from people in different areas, starting first with advice
from experts in your field, feedback from coworkers or other clients, and by
looking analytically at your own past experiences.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
40: Tell me about a decision you made that did not turn out well.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Honesty and transparency are great values that your interviewer will
appreciate – outline the choice you made, why you made it, the results of
your poor decision – and finally (and most importantly!) what you learned
from the decision. Give the interviewer reason to trust that you wouldn't
make a decision like that again in the future.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
41: Are you able to make decisions quickly?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
You may be able to make decisions quickly, but be sure to communicate
your skill in making sound, thorough decisions as well. Discuss the
importance of making a decision quickly, and how you do so, as well as the
necessity for each decision to first be well-informed.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
42: Tell me about your favorite book or newspaper.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
The interviewer will look at your answer to this question in order to
determine your ability to analyze and review critically. Additionally, try to
choose something that is on a topic related to your field or that embodies a

theme important to your work, and be able to explain how it relates. Stay
away from controversial subject matter, such as politics or religion.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
43: If you could be rich or famous, which would you choose?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This question speaks to your ability to think creatively, but your answer
may also give great insight to your character. If you answer rich, your
interviewer may interpret that you are self-confident and don't seek
approval from others, and that you like to be rewarded for your work. If
you choose famous, your interviewer may gather that you like to be well-
known and to deal with people, and to have the platform to deliver your
message to others. Either way, it's important to back up your answer with
sound reasoning.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
44: If you could trade places with anyone for a week, who would it be and why?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This question is largely designed to test your ability to think on your feet,
and to come up with a reasonable answer to an outside the box question.
Whoever you choose, explain your answer in a logical manner, and offer
specific professional reasons that led you to choose the individual.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
45: What would you say if I told you that just from glancing over your resume, I can already see three spelling mistakes?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Clearly, your resume should be absolutely spotless – and you should be
confident that it is. If your interviewer tries to make you second-guess
yourself here, remain calm and poised and assert with a polite smile that
you would be quite surprised as you are positive that your resume is error-
free.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
46: Tell me about your worldview.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This question is designed to offer insight into your personality, so be aware
of how the interviewer will interpret your answer. Speak openly and
directly, and try to incorporate your own job skills into your outlook on life.
For example, discuss your beliefs on the ways that hard work and
dedication can always bring success, or in how learning new things is one
of life's greatest gifts. It's okay to expand into general life principles here,
but try to keep your thoughts related to the professional field as well.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
47: What is the biggest mistake someone could make in an interview?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
The biggest mistake that could be made in an interview is to be caught off
guard! Make sure that you don't commit whatever you answer here, and
additionally be prepared for all questions. Other common mistakes include
asking too early in the hiring process about job benefits, not having
questions prepared when the interviewer asks if you have questions,
arriving late, dressing casually or sloppily, or showing ignorance of the
position.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
48: If you won the $50m lottery, what would you do with the money?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
While a question such as this may seem out of place in a job interview, it's
important to display your creative thinking and your ability to think on the
spot. It's also helpful if you choose something admirable, yet believable, to
do with the money such as donate the first seventy percent to a charitable
cause, and divide the remainder among gifts for friends, family, and of
course, yourself.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
49: Is there ever a time when honesty isn't appropriate in the workplace?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This may be a difficult question, but the only time that honesty isn't
appropriate in the workplace is perhaps when you're feeling anger or
another emotion that is best kept to yourself. If this is the case, explain
simply that it is best to put some thoughts aside, and clarify that the process
of keeping some thoughts quiet is often enough to smooth over any
unsettled emotions, thus eliminating the problem.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
50: If you could travel anywhere in the world, where would it be?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This question is meant to allow you to be creative – so go ahead and stretch
your thoughts to come up with a unique answer. However, be sure to keep
your answer professionally-minded. For example, choose somewhere rich

with culture or that would expose you to a new experience, rather than
going on an expensive cruise through the Bahamas.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
51: What would I find in your refrigerator right now?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
An interviewer may ask a creative question such as this in order to discern
your ability to answer unexpected questions calmly, or, to try to gain some
insight into your personality. For example, candidates with a refrigerator
full of junk food or take-out may be more likely to be under stress or have
health issues, while a candidate with a balanced refrigerator full of
nutritious staples may be more likely to lead a balanced mental life, as well.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
52: If you could play any sport professionally, what would it be and what aspect draws you to it?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Even if you don't know much about professional sports, this question might
be a great opportunity to highlight some of your greatest professional
working skills. For example, you may choose to play professional
basketball, because you admire the teamwork and coordination that goes
into creating a solid play. Or, you may choose to play professional tennis,
because you consider yourself to be a go-getter with a solid work ethic and
great dedication to perfecting your craft. Explain your choice simply to the
interviewer without elaborating on drawn-out sports metaphors, and be sure
to point out specific areas or skills in which you excel.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
53: Who were the presidential and vice-presidential candidates in the recent elections?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This question, plain and simple, is intended as a gauge of your intelligence
and awareness. If you miss this question, you may well fail the interview.
Offer your response with a polite smile, because you understand that there
are some individuals who probably miss this question.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
54: Explain X task in a few short sentences as you would to a second-grader.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
An interviewer may ask you to break down a normal job task that you
would complete in a manner that a child could understand, in part to test
your knowledge of the task's inner workings – but in larger part, to test your
ability to explain a process in simple, basic terms. While you and your
coworkers may be able to converse using highly technical language, being
able to simplify a process is an important skill for any employee to have.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
55: If you could compare yourself to any animal, what would it be?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Many interviewers ask this question, and it's not to determine which
character traits you think you embody – instead, the interviewer wants to
see that you can think outside the box, and that you're able to reason your
way through any situation. Regardless of what animal you answer, be sure
that you provide a thorough reason for your choice.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
56: Who is your hero?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Your hero may be your mother or father, an old professor, someone
successful in your field, or perhaps even Wonder Woman – but keep your
reasoning for your choice professional, and be prepared to offer a logical
train of thought. Choose someone who embodies values that are important
in your chosen career field, and answer the question with a smile and sense
of passion.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
57: Who would play you in the movie about your life?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
As with many creative questions that challenge an interviewee to think
outside the box, the answer to this question is not as important as how you
answer it. Choose a professional, and relatively non-controversial actor or
actress, and then be prepared to offer specific reasoning for your choice,
employing important skills or traits you possess.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
58: Name five people, alive or dead, that would be at your ideal dinner
party.
Answer:
Smile and sound excited at the opportunity to think outside the box when
asked this question, even if it seems to come from left field. Choose
dynamic, inspiring individuals who you could truly learn from, and explain
what each of them would have to offer to the conversation. Don't forget to

include yourself, and to talk about what you would bring to the
conversation as well!
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
59: What is customer service?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Customer service can be many things – and the most important
consideration in this question is that you have a creative answer.
Demonstrate your ability to think outside the box by offering a confident
answer that goes past a basic definition, and that shows you have truly
considered your own individual view of what it means to take care of your
customers. The thoughtful consideration you hold for customers will speak
for itself.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
60: Tell me about a time when you went out of your way for a customer.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
It's important that you offer an example of a time you truly went out of your
way – be careful not to confuse something that felt like a big effort on your
part, with something your employer would expect you to do anyway. Offer
an example of the customer's problems, what you did to solve it, and the
way the customer responded after you took care of the situation.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
61: How do you gain confidence from customers?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
This is a very open-ended question that allows you to show your customer
service skills to the interviewer. There are many possible answers, and it is
best to choose something that you've had great experience with, such as “by
handling situations with transparency,” “offering rewards,” or “focusing on
great communication.” Offer specific examples of successes you've had.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
62: Tell me about a time when a customer was upset or agitated – how did you handle the situation?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Similarly to handling a dispute with another employee, the most important
part to answering this question is to first set up the scenario, offer a step-by-
step guide to your particular conflict resolution style, and end by describing
the way the conflict was resolved. Be sure that in answering questions
about your own conflict resolution style, that you emphasize the importance
of open communication and understanding from both parties, as well as a
willingness to reach a compromise or other solution.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
63: When can you make an exception for a customer?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Exceptions for customers can generally be made when in accordance with
company policy or when directed by a supervisor. Display an
understanding of the types of situations in which an exception should be
considered, such as when a customer has endured a particular hardship, had
a complication with an order, or at a request.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
64: What would you do in a situation where you were needed by both a customer and your boss?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
While both your customer and your boss have different needs of you and
are very important to your success as a worker, it is always best to try to
attend to your customer first – however, the key is explaining to your boss
why you are needed urgently by the customer, and then to assure your boss
that you will attend to his or her needs as soon as possible (unless it's
absolutely an urgent matter).
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
65: What is the most important aspect of customer service?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
While many people would simply state that customer satisfaction is the
most important aspect of customer service, it's important to be able to
elaborate on other important techniques in customer service situations.
Explain why customer service is such a key part of business, and be sure to
expand on the aspect that you deem to be the most important in a way that
is reasoned and well-thought out.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
66: Is it best to create low or high expectations for a customer?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
You may answer this question either way (after, of course, determining that
the company does not have a clear opinion on the matter). However, no
matter which way you answer the question, you must display a thorough
thought process, and very clear reasoning for the option you chose. Offer

pros and cons of each, and include the ultimate point that tips the scale in
favor of your chosen answer.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
67: Why would your skills be a good match with X objective of our company?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
If you've researched the company before the interview, answering this
question should be no problem. Determine several of the company's main
objectives, and explain how specific skills that you have are conducive to
them. Also, think about ways that your experience and skills can translate
to helping the company expand upon these objectives, and to reach further
goals. If your old company had a similar objective, give a specific example
of how you helped the company to meet it.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
68: What do you think this job entails?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Make sure you've researched the position well before heading into the
interview. Read any and all job descriptions you can find (at best, directly
from the employer's website or job posting), and make note of key duties,
responsibilities, and experience required. Few things are less impressive to
an interviewer than a candidate who has no idea what sort of job they're
actually being interviewed for.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
69: Is there anything else about the job or company you'd like to know?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:

If you have learned about the company beforehand, this is a great
opportunity to show that you put in the effort to study before the interview.
Ask questions about the company's mission in relation to current industry
trends, and engage the interviewer in interesting, relevant conversation.
Additionally, clear up anything else you need to know about the specific
position before leaving – so that if the interviewer calls with an offer, you'll
be prepared to answer.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
70: Are you the best candidate for this position?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Yes! Offer specific details about what makes you qualified for this position,
and be sure to discuss (and show) your unbridled passion and enthusiasm
for the new opportunity, the job, and the company.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
71: How did you prepare for this interview?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
The key part of this question is to make sure that you have prepared! Be
sure that you've researched the company, their objectives, and their services
prior to the interview, and know as much about the specific position as you
possibly can. It's also helpful to learn about the company's history and key
players in the current organization.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
72: If you were hired here, what would you do on your first day?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:

While many people will answer this question in a boring fashion, going
through the standard first day procedures, this question is actually a great
chance for you to show the interviewer why you will make a great hire. In
addition to things like going through training or orientation, emphasize how
much you would enjoy meeting your supervisors and coworkers, or how
you would spend a lot of the day asking questions and taking in all of your
new surroundings.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
73: Have you viewed our company's website?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Clearly, you should have viewed the company's website and done some
preliminary research on them before coming to the interview. If for some
reason you did not, do not say that you did, as the interviewer may reveal
you by asking a specific question about it. If you did look at the company's
website, this is an appropriate time to bring up something you saw there
that was of particular interest to you, or a value that you especially
supported.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
74: How does X experience on your resume relate to this position?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Many applicants will have some bit of experience on their resume that does
not clearly translate to the specific job in question. However, be prepared to
be asked about this type of seemingly-irrelevant experience, and have a
response prepared that takes into account similar skill sets or training that
the two may share.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
75: Why do you want this position?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Keep this answer focused positively on aspects of this specific job that will
allow you to further your skills, offer new experience, or that will be an
opportunity for you to do something that you particularly enjoy. Don't tell
the interviewer that you've been looking for a job for a long time, or that the
pay is very appealing, or you will appear unmotivated and opportunistic.
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
76: How is your background relevant to this position?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
Ideally, this should be obvious from your resume. However, in instances
where your experience is more loosely-related to the position, make sure
that you've researched the job and company well before the interview. That
way, you can intelligently relate the experience and skills that you do have,
to similar skills that would be needed in the new position. Explain
specifically how your skills will translate, and use words to describe your
background such as “preparation” and “learning.” Your prospective
position should be described as an “opportunity” and a chance for “growth
and development.”

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
77: How do you feel about X mission of our company?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
Answer:
It's important to have researched the company prior to the interview – and if
you've done so, this question won't catch you off guard. The best answer is
one that is simple, to the point, and shows knowledge of the mission at
hand. Offer a few short statements as to why you believe in the mission's
importance, and note that you would be interested in the chance to work
with a company that supports it.
*****

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h1>INDEX</h1>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>JavaScript Interview Questions</h2>
<h3>Introduction to JavaScript</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
1: What is JavaScript?
2: What kind of language does JavaScript provide?
3: Is there any connection between Java and JavaScript?
4: What is the official name of JavaScript and is it supported by all browsers?
5: What does JavaScript do?
6: Does prior knowledge of JAVA ease the use of JavaScript?
7: Is JavaScript case sensitive?
8: How do you place JavaScript?
9: Where do you place JavaScript?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Statements, Comments and Variables</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
10: Where do you place JavaScript?
11: Why are comments used in JavaScript and how are they inserted?
12: What are variables and how are they inserted?
13: What does a variable of var y=10; and var catname= "Tomcat"; do?
14: How many statements types can we find in JavaScript? Give some examples?
15: What are conditional statements and how are they implemented in JavaScript?
16: How will you determine a variable type in JavaScript?
17: What is the difference in evaluating [“8”+5+2] and [8+5+”2”]?
18: Is it possible to assign a string to a floating point variable?
19: Will variable redeclaration affect the value of that variable?
20: How will you search a matching pattern globally in a string?
21: How will you search a particular pattern in a string?
22: Which property is used to match the pattern at the start of the string?
23: Which property is used to match the pattern at the end of the string?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Operators and Functions</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
24: What are operators? Which are the most important operators in JavaScript?
25: Why comparison and logical operators are used?
26: How many types of pop-up boxes does JavaScript have? What are those?
27: Does creating an alert box prompt the user to respond with OK or Cancel?
28: What are functions in JavaScript and where are they placed?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Values, Arrays and Operators</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
29: What does the keyword null mean in JavaScript?
30: What does the value undefined mean in JavaScript?
31: Do the null and undefined values have the same conversion in Boolean, numeric and string context?
32: What are Boolean values?
33: Can a Boolean value be converted into numeric context?
34: What happens when a number is dropped where a Boolean value is expected to be?
35: What are objects in JavaScript?
36: What is an array in JavaScript?
37: From which version forward has JavaScript stopped using ASCII character set?
38: What is the scope of a variable in JavaScript?
39: In the body of the code which variable with the same name has more importance over the other: 
    the local or the global variable?
40: How many types of undefined variables can we find in JavaScript?
41: What does (==) & (===) operators do in JavaScript?
42: How many types of operators can we find in JavaScript?
43: How many types of comparison operators does JavaScript contain?
44: Can comparison be done on any type of operands?
45: What are logical operators and how are they used in JavaScript?
46: Does JavaScript contain classes?
47: What is the purpose of an object in JavaScript?
48: How are classes and objects in JavaScript named and why?
49: What are class properties in JavaScript?
50: What are class methods in JavaScript?
51: Do class properties and class methods have a global and local range?
52: How do JavaScript equality operators compare objects?
53: Are the null and undefined values for the variable same?
54: What is the difference between “===” and “==”? Give examples
55: What is the function of delete operator in JavaScript?
56: How will you clip the particular portion of an element?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Modules, Characters and Attributes</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
57: How is a module in JavaScript written so that it can be used by any script or module?
58: How are regular expressions represented and created in JavaScript?
59: How do you combine literal characters in JavaScript?
60: What document properties does a document contain?
61: How many types of DOM document object collections can we find in JavaScript?
62: Does use of DOM properties allow you to change the structure of a document?
63: How are document objects named in JavaScript?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Event Handlers and DOM</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
64: How are event handlers defined in JavaScript?
65: What do the HTMLInputElement and HTMLFormElementinterfaces define in HTML DOM?
66: How many levels of DOM standard are currently released?
67: Are there any more levels of DOM?
68: What does the Node interface define in DOM?
69: How do you find document elements in a HTML document?
70: How are documents created and modified in DOM?
71: How can you build a DOM tree of arbitrary document content?
72: How do you find document elements in IE4?
73: How to access Html attributes using DOM?
74: What is the difference between getAttribute() and getAttributeNode()?
75: What are the event handlers in JavaScript?
76: Can you use two or more functions in onclick event?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Keywords, CSS and CSS2</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
77: What is the “this” keyword in JavaScript?
78: What does lexically scoped in JavaScript mean?
79: Is the following expression correct: element.style.font-family= "arial";?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Statements and Functions</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
80: How can you replace an if-else statement in JavaScript?
81: What is a "memoization" method in JavaScript?
82: What does 2+3+”1” evaluate to?

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Roles of JavaScript, Scripts and Events</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
83: Give some examples of the role that JavaScript has on the Web.
84: Give an example on how JavaScript can be used in URLs.
85: How are scripts in JavaScript executed?
86: What do scripts placed in the <head> part of an HTML document do?
87: What do scripts placed in the <body> part of an HTML document do?
88: When does browser trigger the onload event?
89: When does the onunload event trigger and what does it do?
90: How can we read or write a file in JavaScript?
91: Explain about “cross-site scripting”.
92: What are JavaScript timers? Give examples and explain one of them.
93: Explain the history property in JavaScript?
94: What is the “Screen” object?
95: What is the “Navigator” object?
96: What is “onreset” in JavaScript?
97: What is void 0 in JavaScript?
98: What is the best practice to place the JavaScript codes?
99: How to prevent caching of web pages in temporary internet files folder?
100: Why adding of meta tag in first header will not prevent caching of the Web page?
101: What is the purpose of meta tag?
102: How will you resolve looping problem in JavaScript?
103: Give any example for resolving looping problem.
104: When is the Execution context created and what are the primary components?
105: When is the Execution context stack created?
106: How is the outer scope environment references maintained?
107: How will you read or write in a file using JavaScript?
108: How will you create rich, responsive display and editor user interface?
109: Which is the new JavaScript engine developed for internet explorer9 by Microsoft?
110: What is Node.js?
111: Which is alternative to XML for data exchange in JavaScript?
112: What are the sub-components of dynamic component in JavaScript?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Opening and Manipulating Windows</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
113: How can you open a new window using JavaScript?
114: How can you close a window using JavaScript?
115: What does the “location” function do in JavaScript?
116: What other properties besides Href can we find in the “location” function in JavaScript?
117: What happens when a string value is added to the location function in JavaScript?
118: What is the history object in JavaScript?
119: Which are the methods supported by the history object in JavaScript?
120: How many and which are the coordinates of a browser within the HTML document?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Objects and their Properties in JavaScript</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
121: Name the properties of Navigator in JavaScript.
122: What happens when confirm() or prompt() methods are used in JavaScript?
123: What happens when the mouse is moved over a hyperlink in JavaScript?
124: What does the “defaultStatus” property do in JavaScript?
125: What is the “onerror” property in JavaScript?
126: What arguments does the error handler receive when an error occurs in JavaScript?
127: In addition to the three arguments that the error handler receives, is its return value of 
     any importance?
128: How can JavaScript code refer to a window or frame object?
129: What is a DOM (Document Object Model)?
130: What does the method write() of the Document object do?
131: How will you determine an object type?
132: What is alert and confirm box in JavaScript?
133: What are the properties of array object?
134: What are the sub objects of the windows object in JavaScript?
135: What is the use of userAgent of navigator object?
136: What are the ways to delete the property of an object and how?
137: What is the use of eval() in JSON?
138: What are the advantages of JSON over XML?
139: How can the properties of JavaScript objects be accessed?
140: What are the objects of navigator objects?
141: How to access the properties of main window from the secondary window?
142: How will you load the previous and next url from the history list?
143: How will you determine whether the browser has cookies enabled?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>JavaScript and HTML</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
144: How can you change the font size of an Element in JavaScript? Give an example.
145: How can you submit a form using JavaScript?
146: How can you set the background color of an HMTL document?
147: Name the Boolean operators in JavaScript.
148: How can we determine the state of a checkbox in JavaScript?
149: How can you create an HTML button and what is the event called when the button is pressed?
150: How will you make loading of JavaScript code after Html by the browser?
151: Which popup allows the user to enter the input?
152: What are the ways to display the message on screen?
153: How will you reload the page from server using JavaScript?
154: How will you display large tables effectively in JavaScript?
155: How will you create pop window using JavaScript?
156: How will you fix the errors that make the JavaScript engines difficult to perform 
     optimization?
157: How will you make secure JavaScript code?
158: How will you add the external JavaScript file?
159: Is it possible to break up a string in a JavaScript code?
160: What is the use of “wait” property in cursor style?
161: What are the properties that can be set in the background properties?
162: What are the ways to set the background color?
163: How will you add JavaScript files dynamically?
164: How will you get the current “x and y” co-ordinate value of the window when it is scrolled?
165: What are the methods to create remote window?
166: How will you get the height of the browser window?
167: How will you get the language code of the linked page?
168: How would you input a file?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>JavaScript Forms</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
169: What is the importance of the “name” attribute of a <form> tag?
170: What are the event handlers of the form element?
171: What does “onchange” event handler do?
172: What is a “cookie”?
173: What does the “new” operator do?
174: What does <optgroup> tag do in JavaScript?
175: Comparison between session state and view state.
176: Which function is best for fast execution: window.onload or onDocumentReady?
177: What is the purpose of “visibility” property in JavaScript?
178: What are the ways to make an element visible/hidden?
179: How will you disable the html form fields, for instance password field?
180: How will you select the contents in the text field, say password?
181: How will you display the id of the form and the name attribute of the hidden element?
182: How will you get the last row from a table in JavaScript?
183: How will you create and delete caption to a table?
184: How will you create a text area and make it read-only?
185: How will you change the caption display position of a table?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>JavaScript Constructors</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
186: What does a JavaScript constructor do?
187: What is the value that the constructor function returns?
188: How many types of common object methods can we find in JavaScript?
189: How does class hierarchy manifest themselves in JavaScript?
190: What does “overriding method” mean?
191: How can you create an XML document in Firefox using JavaScript?
192: How are images accessed from JavaScript?
193: Where is the arguments() array placed in JavaScript?
194: Which are the properties of the arguments object in JavaScript?
195: What happens when a function is invoked with the arguments object?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>Miscellaneous Arguments, Functions and Methods in JavaScript</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
196: What does arguments.callee do in JavaScript?
197: What does arguments.length do in JavaScript?
198: What other JavaScript method you know that is similar with shift() method?
199: How can you remove a page from the browser history?
200: How can you pass data between pages using cookies?
201: What is the difference between resizeTo() and resizeBy() methods?
202: What’s the difference between moveTo() and moveBy() methods?
203: How can a window that is buried beneath other windows be brought back to the front?
204: What happens when a string argument is passed with the Date() constructor in JavaScript?
205: Which are the arguments of the Date() constructor in JavaScript?
206: What does URIError indicate in JavaScript?
207: What does the encodeURIComponent function do in JavaScript?
208: What does the string argument do in JavaScript?
209: What is and what does the escape() function do in JavaScript?
210: What does the apply() function do in JavaScript and which are its arguments?
211: What does the getClass() function do in JavaScript?
212: What is Infinity in JavaScript?
213: What does the exec() method do in JavaScript?
214: What happens when the exec() method is invoked on a nonglobal pattern?
215: Does exec() include full details of every match even if regexp is not global?
216: What is an anchor in JavaScript?
217: What does the focus() method do in JavaScript?
218: Is JSObject a JavaScript object?
219: What does the call() method of JSObject class do?
220: What does the eval() method of the JSObject do?
221: What does the getSlot() method of the JSObject do?
222: What does the removeMember() method of the JSObject do?
223: What does the setMember() method of the JSObject do?
224: What does the toString() method of JSObject do?
225: What does the (n) argument represent in isFinite(n) and what does it return?
226: What does the isNaN() function do in JavaScript?
227: What does the setYear() function do in JavaScript?
228: What does the join() method do in JavaScript?
229: How will you pop the last element from an existing array?
230: How to pop the first element from an existing array?
231: How will you add one or more elements to the end of the existing array?
232: How will you add one or more elements to the beginning of the existing array?
233: How will you reverse the elements in an array?
234: What does the Array.slice(start,end) method do in JavaScript and how to retrieve the elements 
     within the selected position in an array?
235: What does the Array.sort() method do in JavaScript?
236: What is encodeURI( ) and encodeURIComponent( )?
237: What is decodeURI( ) and decodeURIComponent( )?
238: What does the splice( ) function do in JavaScript?
239: How will you print the current window using JavaScript?
240: How will you get default value when an argument is not passed in calling function?
241: How will you encode and decode a string?
242: How will you pass a function as argument to another function?
243: What is the need for callback function?
244: How will you get a substring from a string in JavaScript?
245: How will you get the function (fn1) which recently called the current function (fn2)?
246: How will you execute the page that is about to be unloaded, before the execution of onload()?
247: How will you find whether the window is closed or not?
248: How will you call a function repeatedly for a particular interval of time?
249: What is the difference between test and exec function?
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h3>JavaScript Design Patterns</h3>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
250: What is a Pattern and explain about design patterns in software programming?
251: Why is it important to identify patterns?
252: What is Singleton Pattern and what is its importance in JavaScript?
253: How will you create singleton in JavaScript?
254: How will you create 2 equal objects in JavaScript?
255: What is the purpose of Factory pattern?
256: How will you create a Factory pattern?
257: Explain about Iterator pattern.
258: Explain about Decorator Pattern.
259: What is the importance of Strategy Pattern?
260: Explain data validation using strategy pattern.
261: Explain Façade pattern with example.
262: Explain about Proxy Pattern.
263: Explain about Mediator pattern.
264: Explain about Observer Pattern.
*****

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>HR Questions</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
1: Tell me about a time when you worked additional hours to finish a project.
2: Tell me about a time when your performance exceeded the duties and requirements of your job.
3: What is your driving attitude about work?
4: Do you take work home with you?
5: Describe a typical work day to me.
6: Tell me about a time when you went out of your way at your previous job.
7: Are you open to receiving feedback and criticisms on your job performance, and adjusting as 
   necessary?
8: What inspires you?
9: How do you inspire others?
10: What has been your biggest success?
11: What motivates you?
12: What do you do when you lose motivation?
13: What do you like to do in your free time?
14: What sets you apart from other workers?
15: Why are you the best candidate for that position?
16: What does it take to be successful?
17: What would be the biggest challenge in this position for you?
18: Would you describe yourself as an introvert or an extrovert?
19: What are some positive character traits that you don't possess?
20: What is the greatest lesson you've ever learned?
21: Have you ever been in a situation where one of your strengths became a weakness in an 
    alternate setting?
22: Who has been the most influential person in your life?
23: Do you consider yourself to be a “detailed” or “big picture” type of person?
24: What is your greatest fear?
25: What sort of challenges do you enjoy?
26: Tell me about a time you were embarrassed. How did you handle it?
27: What is your greatest weakness?
28: What are the three best adjectives to describe you in a work setting?
29: What are the three best adjectives to describe you in your personal life?
30: What type of worker are you?
31: Tell me about your happiest day at work.
32: Tell me about your worst day at work.
33: What are you passionate about?
34: What is the piece of criticism you receive most often?
35: What type of work environment do you succeed the most in?
36: Are you an emotional person?
37: How do you make decisions?
38: What are the most difficult decisions for you to make?
39: When making a tough decision, how do you gather information?
40: Tell me about a decision you made that did not turn out well.
41: Are you able to make decisions quickly?
42: Tell me about your favorite book or newspaper.
43: If you could be rich or famous, which would you choose?
44: If you could trade places with anyone for a week, who would it be and why?
45: What would you say if I told you that just from glancing over your resume, I can already see 
    three spelling mistakes?
46: Tell me about your worldview.
47: What is the biggest mistake someone could make in an interview?
48: If you won the $50m lottery, what would you do with the money?
49: Is there ever a time when honesty isn't appropriate in the workplace?
50: If you could travel anywhere in the world, where would it be?
51: What would I find in your refrigerator right now?
52: If you could play any sport professionally, what would it be and what aspect draws you to it?
53: Who were the presidential and vice-presidential candidates in the recent elections?
54: Explain X task in a few short sentences as you would to a second-grader.
55: If you could compare yourself to any animal, what would it be?
56: Who is your hero?
57: Who would play you in the movie about your life?
58: Name five people, alive or dead, that would be at your ideal dinner party.
59: What is customer service?
60: Tell me about a time when you went out of your way for a customer.
61: How do you gain confidence from customers?
62: Tell me about a time when a customer was upset or agitated – how did you handle the situation?
63: When can you make an exception for a customer?
64: What would you do in a situation where you were needed by both a customer and your boss?
65: What is the most important aspect of customer service?
66: Is it best to create low or high expectations for a customer?
67: Why would your skills be a good match with X objective of our company?
68: What do you think this job entails?
69: Is there anything else about the job or company you'd like to know?
70: Are you the best candidate for this position?
71: How did you prepare for this interview?
72: If you were hired here, what would you do on your first day?
73: Have you viewed our company's website?
74: How does X experience on your resume relate to this position?
75: Why do you want this position?
76: How is your background relevant to this position?
77: How do you feel about X mission of our company?
*****

<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
<h2>Some of the following titles might also be handy:</h2>
<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
1. .NET Interview Questions You'll Most Likely Be Asked
2. 200 Interview Questions You'll Most Likely Be Asked
3. Access VBA Programming Interview Questions You'll Most Likely Be Asked
4. Adobe ColdFusion Interview Questions You'll Most Likely Be Asked
5. Advanced C++ Interview Questions You'll Most Likely Be Asked
6. Advanced Excel Interview Questions You'll Most Likely Be Asked
7. Advanced JAVA Interview Questions You'll Most Likely Be Asked
8. Advanced SAS Interview Questions You'll Most Likely Be Asked
9. AJAX Interview Questions You'll Most Likely Be Asked
10. Algorithms Interview Questions You'll Most Likely Be Asked
11. Android Development Interview Questions You'll Most Likely Be Asked
12. Ant & Maven Interview Questions You'll Most Likely Be Asked
13. Apache Web Server Interview Questions You'll Most Likely Be Asked
14. Artificial Intelligence Interview Questions You'll Most Likely Be Asked
15. ASP.NET Interview Questions You'll Most Likely Be Asked
16. Automated Software Testing Interview Questions You'll Most Likely Be Asked
17. Base SAS Interview Questions You'll Most Likely Be Asked
18. BEA WebLogic Server Interview Questions You'll Most Likely Be Asked
19. C & C++ Interview Questions You'll Most Likely Be Asked
20. C# Interview Questions You'll Most Likely Be Asked
21. CCNA Interview Questions You'll Most Likely Be Asked
22. Cloud Computing Interview Questions You'll Most Likely Be Asked
23. Computer Architecture Interview Questions You'll Most Likely Be Asked
24. Computer Networks Interview Questions You'll Most Likely Be Asked
25. Core JAVA Interview Questions You'll Most Likely Be Asked
26. Data Structures & Algorithms Interview Questions You'll Most Likely Be Asked
27. EJB 3.0 Interview Questions You'll Most Likely Be Asked
28. Entity Framework Interview Questions You'll Most Likely Be Asked
29. Fedora & RHEL Interview Questions You'll Most Likely Be Asked
30. Hibernate, Spring & Struts Interview Questions You'll Most Likely Be Asked
31. HTML, XHTML and CSS Interview Questions You'll Most Likely Be Asked
32. HTML5 Interview Questions You'll Most Likely Be Asked
33. IBM WebSphere Application Server Interview Questions You'll Most Likely Be Asked
34. iOS SDK Interview Questions You'll Most Likely Be Asked
35. Java / J2EE Design Patterns Interview Questions You'll Most Likely Be Asked
36. Java / J2EE Interview Questions You'll Most Likely Be Asked
37. JavaScript Interview Questions You'll Most Likely Be Asked
38. JavaServer Faces Interview Questions You'll Most Likely Be Asked
39. JDBC Interview Questions You'll Most Likely Be Asked
40. jQuery Interview Questions You'll Most Likely Be Asked
41. JSP-Servlet Interview Questions You'll Most Likely Be Asked
42. JUnit Interview Questions You'll Most Likely Be Asked
43. Linux Interview Questions You'll Most Likely Be Asked
44. Linux System Administrator Interview Questions You'll Most Likely Be Asked
45. Mac OS X Lion Interview Questions You'll Most Likely Be Asked
46. Mac OS X Snow Leopard Interview Questions You'll Most Likely Be Asked
47. Microsoft Access Interview Questions You'll Most Likely Be Asked
48. Microsoft Powerpoint Interview Questions You'll Most Likely Be Asked
49. Microsoft Word Interview Questions You'll Most Likely Be Asked
50. MySQL Interview Questions You'll Most Likely Be Asked
51. Networking Interview Questions You'll Most Likely Be Asked
52. OOPS Interview Questions You'll Most Likely Be Asked
53. Operating Systems Interview Questions You'll Most Likely Be Asked
54. Oracle Database Administration Interview Questions You'll Most Likely Be Asked
55. Oracle E-Business Suite Interview Questions You'll Most Likely Be Asked
56. ORACLE PL/SQL Interview Questions You'll Most Likely Be Asked
57. Perl Programming Interview Questions You'll Most Likely Be Asked
58. PHP Interview Questions You'll Most Likely Be Asked
59. Python Interview Questions You'll Most Likely Be Asked
60. RESTful JAVA Web Services Interview Questions You'll Most Likely Be Asked
61. SAP HANA Interview Questions You'll Most Likely Be Asked
62. SAS Programming Guidelines Interview Questions You'll Most Likely Be Asked
63. Selenium Testing Tools Interview Questions You'll Most Likely Be Asked
64. Silverlight Interview Questions You'll Most Likely Be Asked
65. Software Repositories Interview Questions You'll Most Likely Be Asked
66. Software Testing Interview Questions You'll Most Likely Be Asked
67. SQL Server Interview Questions You'll Most Likely Be Asked
68. Tomcat Interview Questions You'll Most Likely Be Asked
69. UML Interview Questions You'll Most Likely Be Asked
70. Unix Interview Questions You'll Most Likely Be Asked
71. UNIX Shell Programming Interview Questions You'll Most Likely Be Asked
72. Windows Server 2008 R2 Interview Questions You'll Most Likely Be Asked
73. XLXP, XSLT, XPATH, XFORMS & XQuery Interview Questions You'll Most Likely Be Asked
74. XML Interview Questions You'll Most Likely Be Asked

