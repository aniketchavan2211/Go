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

#### Datatypes

Every values we store in variables have different datatypes,
means a is differenet from 0, 1, 2. alphabets are different from numbers.

1. `int`: integer or numbers or digits. examples: -1, 0, 2, ...etc.

2. `uint`: unsigned integer, Go langauge has other integer datatypes which can't be negative, examples: 0, 1, 2 ...etc.

3. `float64`: floating-point numbers or decimal numbers. examples: 0.1, 2.4 ..etc.
                `64` is bytes, `float32` 32 memory spaces or bytes are alloted.

4. `bool`: Boolean values, `true` or `false`, used in Decision making.

### Input / Output

#### Input

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

Conditonal Operators

1. `==` or `equal to`.
2. `!=` or `not equal to`.
3. `<=` or `less than or equal to`.
4. `>=` or `greater than or equal to`.
5. `<` or `less than`. 
6. `>` or `greater than`.

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
