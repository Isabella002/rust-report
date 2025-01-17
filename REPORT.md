# Rust, a Deep Dive

## **INTRODUCTION**

## **TOPICS FOR DISCUSSION**

### **1. Data Types - B.Mester**

Rust is a statically typed language, so it's important to know all types of variables at the compile time. Any and every value in Rust is a specific data type. Rust consists of four primary scalar data types: 
* Boolean 
  * Boolean data types follow the universal true or false definition with the keyword being **bool** to classify the boolean type. Because boolean types have only two possible values (true/false) they are most incorporated into conditional statements.
* Character
  * Rust character types are used to store characters. The **char** type declares character values. Char literals are specified with single quotes instead of double quotes like string literals do.
* Floating-Point 
  * Floating-Point types are **f32** and **f64** which are respective bit sizes. Floating-point numbers are numbers with decimal points, like float numbers in other programming languages. The f32 type is a single precision float, and f64 has double precision.
* Integer  
  * Integer types are whole numbers, unsigned integers start with a *u* and signed integer types start with the letter *i*.
Rust's **char** type represents a *Unicode Scalar Value*, and represents a lot more than just ASCII.

### **2. Expressions - B.Mester**

Rust is an expression oriented language, so most constructs are expressions. Expressions in Rust primarily have two roles which are, to always produce a value that might have side effects depending on the purpose. Expressions can range from a literal value, to a function call and a lot of expressions have operands or sub-expressions.  Expressions in Rust determine the flow of execution. Blocks, being a type of expression, can be nested within one another, allowing for recursive nesting of blocks, statements, and expressions to any level of complexity. Rust expressions can be put into two main types:
* **Place expressions**
  * A place expression refers to memory location and is identified by paths, such as local variables, static variables, dereferences (* expr), array indexing expressions (expr[expr]), field references (expr.f), and parenthesized place expressions. In a place expression context, we find the left operand of an assignment or compound assignment expression, the single operand of a unary borrow operation, and the operand of any implicit borrow. Additionally, the discriminant or subject of a match expression and the right side of a let statement also fall into the place expression context. In contrast, all other expression contexts are considered value expression contexts.
* **Value expressions**
  * A value expression is an expression that represents an actual value. Any expression that is not a place expression is considered a value expression.

Each expression, including its sub-expressions, can occur in either a place context or a value context. The evaluation of an expression depends on both its own category and the context in which it appears.

### **3. Assignment Statements - J.Damo**

ASSIGNMENT STATEMENTS IN RUST

The syntax for Rust statements is as follows:
<ul>
  <li>Statement:</li>
  <li> ; </li>
  <li>| Item </li>
  <li>| LetStatement </li>
  <li>| ExpressionStatement </li>
  <li>| MacroinvocationSemi </li>
  </ul>

The statement block can be an outer expression or function in which Rust has declaration and expression statements.
Rust with declaration statement introduces names into the enclosed statement block in which declared names are denoting
new variables or else new items. The item declarations within a statement block restricts its scope to the statement
block. In Rust there is no implicit capture of the containing functions, generic parameters, parameters or else local
variable; whereas inner cannot access outer_var. (see example below)

<ul>
  <li>fn outer() { </li>
  <li>let outer_var = true; </li>
  <li>fn inner() { /* outer_var is not in scope here*/} </li>
  <li>inner(); </li>
  <li> } </li>
  </ul>

Another statements are let statements in Rust see syntax below:
  
  <ul>
    <li>LetStatement: </li>
    <li>OuterAttribute let PatternNoTopAlt (:Type) </li>
    <li>(=Expression (else BlockExpression));</li>
  </ul>
  
  In the Rust let statement thus introduces a new set of variables in a pattern in which a type annotation and then either
  ends or else followed by an initializer expression plus an optional else block. Likewise, any variables introduced by a
  variable declaration visible at point of declaration until ending enclosed block scope with exception shadowing another
  variable declaration . Example of let statement as follows:
  
  <ul>
  <li>let (mut v, w) = (vec! [1,2,3], 42); </li>
  <li>let Some(t) = v.pop else { </li>
  <li>panic!(); </li>
  <li>}; </li>
  <li>let [u,v] = [v [0], v[i]] else { </li>
  <li>panic!();</li>
  <li>}; </li>
  </ul>
  
  Other attributes on Rust statements in that statements accept outer attributes that have meaning on a statement are 
  cfg and the lint check attributes. In this report discussion about expression statements will be introduced by the 
  other team member B.Mester.
    
### **4. Statement-Level Control Structures - J.Damo**

STATEMENT LEVEL CONTROL STRUCTURES

The question is what are control structures in Rust? The answer is that control structure will let you specify instructions
to run only if certain conditions are met. Therefore, Rust's control structure are crucial for managing program flow,
thus enabling efficient exception of the code; therefore, simplifying the complex tasks into smaller reusable components.
Likewise, the conditional statements will allow you to running code based on conditions.

In Rust the if statement can test whether a certain condition evaluating to be true. Therefore, if condition does the
program will run the block of code. On the other hand, if the condition evaluates to be false the program will skip
the block of code; likewise moving on to the next statement or run the else statement block. Rust provide a match statement
a control flow construct allowing a program to matching values against a series of patterns executing code based on the 
matching pattern scheme. Here is an example of Rust syntax on if statements.

<ul>
  <li>if condition { //code to execute if condition is true </li>
  <li>} </li>
  <li>fn main() { </li>
  <li>let x = 15; </li>
  <li>if x > 10 { </li>
  <li>println!("x is greater than 10"); </li>
  <li>} </li>
  <li>} </li>
  </ul>
  
  Example on if statement evaluates false and an else statements runs.
  
  <ul>
  <li>fn main() { </li>
  <li>let x = 5; </li>
  <li>if x > 10 { </li>
  <li>println!("x is greater than 10"); </li>
  <li>} else{ </li>
  <li>println!("x is not greater than 10"); </li>
  <li>} </li>
  <li> } </li>
  </ul>
  
  Example of structure of Rust match statement.
  
  <ul>
  <li>match value{ </li>
  <li>pattern1 => { </li>
  <li>//code to execute if the value matches pattern </li>
  <li>}, </li>
  <li>pattern2 => { </li>
  <li>//code to execute if value matches pattern2
  <li>}, </li>
  <li>} </li>
  </ul>


### **5. Subprograms - A.Bower**

### **6. Abstract Data Types and Encapsulation Concepts - A.Bower**

### **7. Object-Oriented Programming - N.Trimmer**

### **8. Exception Handling and Event Handling - N.Trimmer**
