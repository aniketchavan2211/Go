
![Go-Language](https://github.com/aniketchavan2211/aniketchavan2211/blob/master/Images/go%20language.webp)

## Go-Language

### Introduction 

Go (Golang) is a programming language used for a variety of purposes, including servers, web development, cloud infrastructure, and command-line interfaces. It’s also beginner-friendly and easy to remember.

Go was designed by Google in 2007. Google was rapidly growing then, and the code its engineers were using, C++, was difficult to manage and overly complex. This slowed down the development process.

So Google engineers Robert Griesemer, Rob Pike, and Ken Thompson, developed something easier to manage and learn. This new language was Go.

Go became open source in 2009 and was released publicly in 2012. It quickly gained popularity among developers and engineers for its ease of use. Here’s an example of a simple “Hello, World!” program written in Go:

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello, GO !!!")
}
```

Today, Go is one of the most popular programming languages. Unlike dynamically typed languages, like JavaScript and Python, Go is statically typed. Statically typed programs won’t start up until errors have been fixed, while dynamically typed languages like JavaScript will start up even if they have errors.

### Comments

Like other's Programming GO language also has commnents, 
Comments are those code which does't been complied or executed by GO complier. 

#### Single-line Comments 

Go complier ignore this single line or one-liner code to been complied or executed.

```go
// Single - Line Comment
```

#### Multi-line Comments 

What if developer need to comment out whole function or more than one line code,
we used multi-line comments, start `/*` and end `*/` between those all code is been ignored. 


```go
/* 
Multi
Line
Comments 
*/
```

### Hello World

```go
package main

import "fmt"


func main() {
    fmt.Println("Hello, World !!!")
}
```

**Code Breakdown**

`package main`: we used main package which ahs some basics functions of code.

`import "fmt"`: we import or used fmt named function (classes in python).

`func`: `func` keyword is used define function.

`main()`:  `main` is named of function followed by `()` opening/closing rounded brackets.

`{ rest of code }`: In opening/closing parenthesis contains rest of code or logic of code. which further will executed.

### Execution on Terminal

1. Building Package

```bash
go build filename.go
```

The command will create a binary file which is disturbuted, 
compiled code which then executed without Go Complier installed. 

Run using

```bash
# for Linux
./filename
```

```
for Windows
.\filename.exe
```

2. Executed directly by Go Complier

This will run or executed program with Go complier installed.

```bash
go run filename.go
```

### Variables and Datatypes

#### Variables

Variables are like storage containers which store values, 
we use `var` keyword to define variable then name of variable_name then assigned values by using assignment operator `=`, then value.

```go
var variable_name string = "Aniket"
var name string = "Aniket"
```

here we define variable, named `variable_name` and `name` which both contains value `"Aniket"`.

when we need `Aniket` we just used variable name to access value.

`string` is datatype which is surrouned by two double quotes `"`,
any alphanumeric value contains between two double quotes is string. exapmles: `a`, `1`, `aaaabbbb`, `1234`.

##### Updating Variables

In Go langauge, we can also update values but can't change datatypes.

```go
var name string = "Aniket"
name = "H4ck3r"

// Throws an error
var name string = "Aniket"
name = 2.4
```

We are changing datatype from `string` to `float` datatypes.

**Note: If variable is not used it throws an error.**

**Dynamic Datatypes Detection**

using `:=` this automatically detected datatypes of variables.

```go
name := "Aniket"
```

#### Constants

Constants like variables but we can't update or change it's value, which means fixed.

Constants are declared like variables but in using a `const` keyword as a prefix to declare a constant with a specific type. It cannot be declared using `:=` syntax. 

```go
const var = "string"
```

#### Datatypes

##### Numbers

Numbers are integers like 0, 1, -2 and so on...

Numbers are have sub-category

`int8`:    8-bit signed integer
`int16`:   16-bit signed integer
`int32`:   32-bit signed integer
`int64`:   64-bit signed integer
`uint8`:   8-bit unsigned integer
`uint16`:  16-bit unsigned integer
`uint32`:  32-bit unsigned integer
`uint64`:  64-bit unsigned integer
`int`:     Both int and uint contain same size, either 32 or 64 bit.
`uint`:    Both int and uint contain same size, either 32 or 64 bit.
`rune`:    It is a synonym of int32 and also represent Unicode code points.
`byte`:    It is a synonym of uint8.
`uintptr`:     It is an unsigned integer type. Its width is not defined, but its can hold all the bits of a pointer value.


##### Floating - Point Numbers

Floating-point numbers are numbers with decimal point. 
example: 0.2, 4.63,...etc.

Floating-point numbers divide into two group.

`float32`:     32-bit IEEE 754 floating-point number
`float64`:     64-bit IEEE 754 floating-point number

##### Booleans

The boolean data type represents only one bit of information either true or false. The values of type boolean are not converted implicitly or explicitly to any other type.

`true` and `false` two values of booleans datatypes.

##### Strings

strings are basically any alphanumeric or met characters inside two double quotes `"strings"` is said to be strings.
example: `"string1", "23", "a028"`.

**Concatenation of Strings**

Strings can be concatenated using plus(+) operator.

```go
func main() {
     
    // str variable which stores strings
   str := "Aniket"
    
   // Display the length of the string
   fmt.Printf("Length of the string is:%d",
                                  len(str))
    
   // Display the string
   fmt.Printf("\nString is: %s", str)
    
   // Display the type of str variable
   fmt.Printf("\nType of str is: %T", str)
}
```

**Output**:
```go
Length of the string is:6
String is: Aniket
Type of str is: string
```

### Input / Output

#### Input

When user needs to input data we use `Scan()` function which define in `fmt` package, and address with variable name
here `&name`: `name` is is variable name and use `&` to address it.

```go
// define variable as name and allocated spaces
var name string 

// using Scan() function in fmt package, passing variable name with prefix 
// & which will store input value in name variable
fmt.Scan(&name)
```

#### Output 

Using `Printf()` formating function defined in fmt package, 
to display output on screen.

```go
fmt.Printf("Hello %v", name)
// Output: Hello, Aniket
```

Here, we use `PrintF()` function display `Hello, Aniket` accessing name variable.

`%d`: for digit
`%f`: for floating-point number


#### Operators

##### Arithmetic Operators


1. Addition: The `+` operator adds two operands. For example, `x+y`.
2. Subtraction: The `-` operator subtracts two operands. For example, `x-y`.
3. Multiplication: The `*` operator multiplies two operands. For example, `x*y`.
4. Division: The `/` operator divides the first operand by the second. For example, `x/y`.
5. Modulus: The `%` operator returns the remainder when the first operand is divided by the second. For example, `x%y`.

```go
   // Addition 
   result1:= p + q 
   fmt.Printf("Result of p + q = %d", result1) 
      
   // Subtraction 
   result2:= p - q 
   fmt.Printf("\nResult of p - q = %d", result2) 
      
   // Multiplication 
   result3:= p * q 
   fmt.Printf("\nResult of p * q = %d", result3) 
      
   // Division 
   result4:= p / q 
   fmt.Printf("\nResult of p / q = %d", result4) 
      
   // Modulus 
   result5:= p % q 
   fmt.Printf("\nResult of p %% q = %d", result5) 
```

##### Relational Operators


1. `==` (Equal To) operator checks whether the two given operands are equal or not. If so, it returns true. Otherwise, it returns false. For example, `5 == 5` will return true.
2. `!=` (Not Equal To) operator checks whether the two given operands are equal or not. If not, it returns true. Otherwise, it returns false. It is the exact boolean complement of the `==` operator. For example, `5 != 5` will return false.
3. `>` (Greater Than)operator checks whether the first operand is greater than the second operand. If so, it returns true. Otherwise, it returns false. For example, `6 > 5` will return true.
4. `<` (Less Than)operator checks whether the first operand is lesser than the second operand. If so, it returns true. Otherwise, it returns false. For example, `6 < 5` will return false.
5. `>=` (Greater Than Equal To) operator checks whether the first operand is greater than or equal to the second operand. If so, it returns true. Otherwise, it returns false. For example, `5 >= 5` will return true.
6. `<=` (Less Than Equal To)operator checks whether the first operand is lesser than or equal to the second operand. If so, it returns true. Otherwise, it returns false. For example, `5 <= 5` will also return true.

```go
   // ‘=='(Equal To) 
   result1:= p == q 
   fmt.Println(result1) 
      
   // ‘!='(Not Equal To) 
   result2:= p != q 
   fmt.Println(result2) 
      
   // ‘<‘(Less Than) 
   result3:= p < q 
   fmt.Println(result3) 
      
   // ‘>'(Greater Than) 
   result4:= p > q 
   fmt.Println(result4) 
      
   // ‘>='(Greater Than Equal To) 
   result5:= p >= q 
   fmt.Println(result5) 
      
   // ‘<='(Less Than Equal To) 
   result6:= p <= q 
   fmt.Println(result6) 
```

##### Logical Operators


1. Logical AND: The `&&` operator returns true when both the conditions in consideration are satisfied. Otherwise it returns false. For example, `a && b` returns true when both a and b are true (i.e. non-zero).
2. Logical OR: The `||` operator returns true when one (or both) of the conditions in consideration is satisfied. Otherwise it returns false. For example, `a || b` returns true if one of a or b is true (i.e. non-zero). Of course, it returns true when both a and b are true.
3. Logical NOT: The `!` operator returns true the condition in consideration is not satisfied. Otherwise it returns false. For example, `!a` returns true if a is false, i.e. when `a=0`.

```go
if(p!=q && p<=q){  
        fmt.Println("True") 
    } 
        
if(p!=q || p<=q){  
        fmt.Println("True") 
} 
        
if(!(p==q)){  
        fmt.Println("True") 
} 
```

##### Bitwise Operators


1. `&` (bitwise AND): Takes two numbers as operands and does AND on every bit of two numbers. The result of AND is 1 only if both bits are 1.
2. `|` (bitwise OR): Takes two numbers as operands and does OR on every bit of two numbers. The result of OR is 1 any of the two bits is 1.
3. `^` (bitwise XOR): Takes two numbers as operands and does XOR on every bit of two numbers. The result of XOR is 1 if the two bits are different.
4. `<<` (left shift): Takes two numbers, left shifts the bits of the first operand, the second operand decides the number of places to shift.
5. `\>\>` (right shift): Takes two numbers, right shifts the bits of the first operand, the second operand decides the number of places to shift.
6. `&^` (AND NOT): This is a bit clear operator.


```go
   // & (bitwise AND) 
   result1:= p & q 
   fmt.Printf("Result of p & q = %d", result1) 
      
   // | (bitwise OR) 
   result2:= p | q 
   fmt.Printf("\nResult of p | q = %d", result2) 
      
   // ^ (bitwise XOR) 
   result3:= p ^ q 
   fmt.Printf("\nResult of p ^ q = %d", result3) 
      
   // << (left shift) 
   result4:= p << 1
   fmt.Printf("\nResult of p << 1 = %d", result4) 
      
   // >> (right shift) 
   result5:= p >> 1
   fmt.Printf("\nResult of p >> 1 = %d", result5) 
      
   // &^ (AND NOT) 
   result6:= p &^ q 
   fmt.Printf("\nResult of p &^ q = %d", result6) 
```

##### Assignment Operators


1. `=` (Simple Assignment): This is the simplest assignment operator. This operator is used to assign the value on the right to the variable on the left.
2. `+=` (Add Assignment): This operator is a combination of `+` and `=` operators. This operator first adds the current value of the variable on left to the value on the right and then assigns the result to the variable on the left.
3. `-=` (Subtract Assignment): This operator is a combination of `-` and `=` operators. This operator first subtracts the current value of the variable on left from the value on the right and then assigns the result to the variable on the left.
4. `*=` (Multiply Assignment): This operator is a combination of `*` and `=` operators. This operator first multiplies the current value of the variable on left to the value on the right and then assigns the result to the variable on the left.
5. `/=` (Division Assignment): This operator is a combination of `/` and `=` operators. This operator first divides the current value of the variable on left by the value on the right and then assigns the result to the variable on the left.
6. `%=` (Modulus Assignment): This operator is a combination of `%` and `=` operators. This operator first modulo the current value of the variable on left by the value on the right and then assigns the result to the variable on the left.
7. `&=` (Bitwise AND Assignment): This operator is a combination of `&` and `=` operators. This operator first “Bitwise AND” the current value of the variable on the left by the value on the right and then assigns the result to the variable on the left.
8. `^=` (Bitwise Exclusive OR): This operator is a combination of `^` and `=` operators. This operator first “Bitwise Exclusive OR” the current value of the variable on left by the value on the right and then assigns the result to the variable on the left.
9. `|=` (Bitwise Inclusive OR): This operator is a combination of `|` and `=` operators. This operator first “Bitwise Inclusive OR” the current value of the variable on left by the value on the right and then assigns the result to the variable on the left.
10. `<<=` (Left shift AND assignment operator): This operator is a combination of `<<` and `=` operators. This operator first “Left shift AND” the current value of the variable on left by the value on the right and then assigns the result to the variable on the left.
11. `>>=` (Right shift AND assignment operator): This operator is a combination of `>>` and `=` operators. This operator first “Right shift AND” the current value of the variable on left by the value on the right and then assigns the result to the variable on the left.


```go
   // “=”(Simple Assignment) 
   p = q 
   fmt.Println(p) 
       
   // “+=”(Add Assignment) 
    p += q 
   fmt.Println(p) 
       
   //“-=”(Subtract Assignment) 
   p-=q 
   fmt.Println(p) 
       
   // “*=”(Multiply Assignment) 
   p*= q 
   fmt.Println(p) 
       
   // “/=”(Division Assignment) 
    p /= q 
   fmt.Println(p) 
      
    // “%=”(Modulus Assignment) 
    p %= q 
   fmt.Println(p) 
```

##### Misc Operators

1. `&`: This operator returns the address of the variable.
2. `*`: This operator provides pointer to a variable.
3. `<-`:The name of this operator is receive. It is used to receive a value from the channel.

```go

// Go program to illustrate the 
// use of Misc Operators 
package main 
    
import "fmt"
    
func main() { 
  a := 4
     
  // Using address of operator(&) and  
  // pointer indirection(*) operator 
  b := &a  
  fmt.Println(*b)  
  *b = 7 
  fmt.Println(a)  
} 
```

**Output**:
```go
4
7
```

### Loops

What if developer needs to repeated things or code or logical functions, loops 
will do the loopin or repeating the function code many times as you want.

**Syntax**:
```go
for init; condition; post {
    // Body Of Code
}
```

We use `for loop`,
start loop with defining varaible `init`,
add some condition to loops, 
and increment or decrement (`i++` & `i--`). 

**Snippet**:
```go
for i:=1; i<10; i++ {
    // Body Of Code
}
```

Here we, define i as 1, give condition run until i is less than 10, and increment, 
loops starts from 0, 1, 2, ... 8, 9. increments means numbers will adds in right direction of numbers line,
if decrement then it will be reverse order.

### Decision Making

We use Decision making when user need make an decision based on input or result,
example: if it's day then turn the light off, if not then turn it on.

#### If-Else-If-Else statements

We use `if` keyword for starting an if statement, 
then condition, if condition is true then executed code in the `{}` curly braces.

**Syntax**:

```go
if name == "Aniket" {
    // if name is equal to Aniket.
} else if name == "H4ck3r" {
    // if name is equal to H4ck3r.
} else {
    // if above code fare all false then executed.
    return // used return keyword to exit the program.
}
```

#### Switch Case

There are two types Switch Cases:

1. Expression Switch Case

Expression switch is similar to switch statement in C, C++, Java language. It provides an easy way to dispatch execution to different parts of code based on the value of the expression. 

**Snippets**:
```go
func main() { 
      
    // Switch statement with both  
    // optional statement, i.e, day:=4 
    // and expression, i.e, day 
    switch day:=4; day{ 
       case 1: 
       fmt.Println("Monday") 
       case 2: 
       fmt.Println("Tuesday") 
       case 3: 
       fmt.Println("Wednesday") 
       case 4: 
       fmt.Println("Thursday") 
       case 5: 
       fmt.Println("Friday") 
       case 6: 
       fmt.Println("Saturday") 
       case 7: 
       fmt.Println("Sunday") 
       default:  
       fmt.Println("Invalid") 
   } 
```

2. Type Switch Case

Type switch is used when you want to compare types. In this switch, the case contains the type which is going to compare with the type present in the switch expression.

**Snippets**:
```go
func main() { 
    var value interface{} 
    switch q:= value.(type) { 
       case bool: 
       fmt.Println("value is of boolean type") 
       case float64: 
       fmt.Println("value is of float64 type") 
       case int: 
       fmt.Println("value is of int type") 
       default: 
       fmt.Printf("value is of type: %T", q) 
         
   }
```

**Output**:
```go
value is of type: <nil>
```


### Functions

Functions are generally the block of codes or statements in a program that gives the user the ability to reuse the same code which ultimately saves the excessive use of memory, acts as a time saver and more importantly, provides better readability of the code. So basically, a function is a collection of statements that perform some specific task and return the result to the caller. A function can also perform some specific task without returning anything.

#### Function Declaration

Function declaration means a way to construct a function.

**Syntax**:
```go
func function_name(Parameter)Return_type{
    // function body.....
}
```

The declaration of the function contains:
 

1. `func`: It is a keyword in Go language, which is used to create a function.
2. `function_name`: It is the name of the function.
3. `Parameter`: It contains the name and the type of the function parameters.
4. `Return_type`: It is optional and it contain the types of the values that function returns. If you are using return_type in your function, then it is necessary to use a return statement in your function.

#### Function Calling

Function Invocation or Function Calling is done when the user wants to execute the function. The function needs to be called for using its functionality.

**Snippets**
```go
package main
import "fmt"
 
// area() is used to find the 
// area of the rectangle
// area() function two parameters,
// i.e, length and width
func area(length, width int)int{
     
    Ar := length* width
    return Ar
}
 
// Main function
func main() {
   
   // Display the area of the rectangle
   // with method calling
   fmt.Printf("Area of rectangle is : %d", area(12, 10))
}
```
**Output**:
```
Area of rectangle is : 120
```

#### Function Arguments

the parameters passed to a function are called actual parameters, whereas the parameters received by a function are called formal parameters.

> Note: By default Go language use call by value method to pass arguments in function.
> Go language supports two ways to pass arguments to your function:
 

- Call by value: : In this parameter passing method, values of actual parameters are copied to function’s formal parameters and the two types of parameters are stored in different memory locations. So any changes made inside functions are not reflected in actual parameters of the caller.

**Snippets**:
```go
package main
  
import "fmt"
  
// function which swap values
func swap(a, b int)int{
 
    var o int
    o= a
    a=b
    b=o
    
   return o 
}
  
// Main function
func main() {
 var p int = 10
 var q int = 20
  fmt.Printf("p = %d and q = %d", p, q)
  
 // call by values
 swap(p, q)
   fmt.Printf("\np = %d and q = %d",p, q)
}
```

**Output**:
```go
p = 10 and q = 20
p = 10 and q = 20
```

-  Call by reference: Both the actual and formal parameters refer to the same locations, so any changes made inside the function are actually reflected in actual parameters of the caller.

**Snippet**:
```go

// Go program to illustrate the
// concept of the call by reference
package main
  
import "fmt"
  
// function which swap values
func swap(a, b *int)int{
    var o int
    o = *a
    *a = *b
    *b = o
     
   return o 
}
  
// Main function
func main() {
 
 var p int = 10
 var q int = 20
 fmt.Printf("p = %d and q = %d", p, q)
  
 // call by reference
 swap(&p, &q)
   fmt.Printf("\np = %d and q = %d",p, q)
}
```

**Output**:
```
p = 10 and q = 20
p = 20 and q = 10
```