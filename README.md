
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

### Data Structures

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
```
Length of the string is:6
String is: Aniket
Type of str is: string
```

#### Struct

A struct (short for structure) is used to create a collection of members of different data types, into a single variable.

While arrays are used to store multiple values of the same data type into a single variable, structs are used to store multiple values of different data types into a single variable.

A struct can be useful for grouping data together to create records.

**Syntax**:
```go
type struct_name struct {
  member1 datatype;
  member2 datatype;
  member3 datatype;
  ...
} 
```

**Snippets**:
```go
 type Person struct {
  name string
  age int
  job string
  salary int
}
```

##### Accessing Values

Accessing Struct by passing require argument or key to return values.

**Snippets**:
```go
package main
import ("fmt")

type Person struct {
  name string
  age int
  job string
  salary int
}

func main() {
  var pers1 Person
  var pers2 Person

  // Pers1 specification
  pers1.name = "Hege"
  pers1.age = 45
  pers1.job = "Teacher"
  pers1.salary = 6000

  // Pers2 specification
  pers2.name = "Cecilie"
  pers2.age = 24
  pers2.job = "Marketing"
  pers2.salary = 4500

  // Access and print Pers1 info
  fmt.Println("Name: ", pers1.name)
  fmt.Println("Age: ", pers1.age)
  fmt.Println("Job: ", pers1.job)
  fmt.Println("Salary: ", pers1.salary)

  // Access and print Pers2 info
  fmt.Println("Name: ", pers2.name)
  fmt.Println("Age: ", pers2.age)
  fmt.Println("Job: ", pers2.job)
  fmt.Println("Salary: ", pers2.salary)
}
```

**Output**
```
Name: Hege
Age: 45
Job: Teacher
Salary: 6000
Name: Cecilie
Age: 24
Job: Marketing
Salary: 4500
```

#### Maps

Maps are used to store data values in key:value pairs. Each element in a map is a key:value pair. A map is an unordered and changeable collection that does not allow duplicates. The length of a map is the number of its elements. You can find it using the `len()` function. The default value of a map is nil. Maps hold references to an underlying hash table. Go has multiple ways for creating maps.

##### Create Maps Using `var` and `:=`

**Syntax**:
```go
var a = map[KeyType]ValueType{key1:value1, key2:value2,...}
b := map[KeyType]ValueType{key1:value1, key2:value2,...}
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = map[string]string{"brand": "Ford", "model": "Mustang", "year": "1964"}
  b := map[string]int{"Oslo": 1, "Bergen": 2, "Trondheim": 3, "Stavanger": 4}

  fmt.Printf("a\t%v\n", a)
  fmt.Printf("b\t%v\n", b)
}
```

**Output**:
```
a   map[brand:Ford model:Mustang year:1964]
b   map[Bergen:2 Oslo:1 Stavanger:4 Trondheim:3]
```

##### Create Maps Using `make()` Function:

**Syntax**:
```go
var a = make(map[KeyType]ValueType)
b := make(map[KeyType]ValueType)
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = make(map[string]string) // The map is empty now
  a["brand"] = "Ford"
  a["model"] = "Mustang"
  a["year"] = "1964"
                                 // a is no longer empty
  b := make(map[string]int)
  b["Oslo"] = 1
  b["Bergen"] = 2
  b["Trondheim"] = 3
  b["Stavanger"] = 4

  fmt.Printf("a\t%v\n", a)
  fmt.Printf("b\t%v\n", b)
}
```

**Ouput**:
```
a   map[brand:Ford model:Mustang year:1964]
b   map[Bergen:2 Oslo:1 Stavanger:4 Trondheim:3]
```

##### Create an Empty Map

There are two ways to create an empty map. One is by using the `make()` function and the other is by using the following syntax.

**Syntax**:
```go
var a map[KeyType]ValueType
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = make(map[string]string)
  var b map[string]string

  fmt.Println(a == nil)
  fmt.Println(b == nil)
}
```

**Output**:
```
false
true
```

**Allowed Key Types**

The map key can be of any data type for which the equality operator (==) is defined. These include:

- Booleans
- Numbers
- Strings
- Arrays
- Pointers
- Structs
- Interfaces (as long as the dynamic type supports equality)

Invalid key types are:

- Slices
- Maps
- Functions

These types are invalid because the equality operator `==` is not defined for them.

##### Access Map Elements

**Syntax**:
```go
value = map_name[key]
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = make(map[string]string)
  a["brand"] = "Ford"
  a["model"] = "Mustang"
  a["year"] = "1964"

  fmt.Printf(a["brand"])
}
```

**Output**:
```
Ford
```

##### Update and Add Map Elements

**Syntax**:
```go
map_name[key] = value
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = make(map[string]string)
  a["brand"] = "Ford"
  a["model"] = "Mustang"
  a["year"] = "1964"

  fmt.Println(a)

  a["year"] = "1970" // Updating an element
  a["color"] = "red" // Adding an element

  fmt.Println(a)
}
```

**Output**:
```
map[brand:Ford model:Mustang year:1964]
map[brand:Ford color:red model:Mustang year:1970]
```

##### Remove Element from Map

Removing elements is done using the `delete()` function.

**Syntax**:
```go
delete(map_name, key)
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = make(map[string]string)
  a["brand"] = "Ford"
  a["model"] = "Mustang"
  a["year"] = "1964"

  fmt.Println(a)

  delete(a,"year")

  fmt.Println(a)
}
```

**Output**:
```
map[brand:Ford model:Mustang year:1964]
map[brand:Ford model:Mustang]
```

##### Check For Specific Elements in a Map

**Syntax**:
```go
val, ok :=map_name[key]
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var a = map[string]string{"brand": "Ford", "model": "Mustang", "year": "1964", "day":""}

  val1, ok1 := a["brand"] // Checking for existing key and its value
  val2, ok2 := a["color"] // Checking for non-existing key and its value
  val3, ok3 := a["day"]   // Checking for existing key and its value
  _, ok4 := a["model"]    // Only checking for existing key and not its value

  fmt.Println(val1, ok1)
  fmt.Println(val2, ok2)
  fmt.Println(val3, ok3)
  fmt.Println(ok4)
}
```

**Output**:
```
Ford true
 false
 true
true 
```

Learn more about: [Maps](https://www.w3schools.com/go/go_maps.php)

#### Arrays

Arrays are used to store multiple values of the same type in a single variable, instead of declaring separate variables for each value. 

##### Declare an Array

- with `var` keyword:

**Syntax**:
```go
var array_name = [length]datatype{values} // here length is defined

or

var array_name = [...]datatype{values} // here length is inferred 
```

- with `:=` sign:

**Syntax**:
```go
array_name := [length]datatype{values} // here length is defined

or

array_name := [...]datatype{values} // here length is inferred 
```

> Note: The length specifies the number of elements to store in the array. In Go, arrays have a fixed length. 
> The length of the array is either defined by a number or is inferred (means that the compiler decides the length of the array, based on the number of values).


This example declares two arrays (arr1 and arr2) with inferred lengths:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var arr1 = [...]int{1,2,3}
  arr2 := [...]int{4,5,6,7,8}

  fmt.Println(arr1)
  fmt.Println(arr2)
}
```
**Output**:
```
[1 2 3]
[4 5 6 7 8] 
```

This example declares an array of strings:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var cars = [4]string{"Volvo", "BMW", "Ford", "Mazda"}
  fmt.Print(cars)
}
```

**Output**:
```
[Volvo BMW Ford Mazda]
```


##### Access Elements of an Array

You can access a specific array element by referring to the index number.

In Go, array indexes start at 0. That means that [0] is the first element, [1] is the second element, etc.

**Snippets**
```go
 package main
import ("fmt")

func main() {
  prices := [3]int{10,20,30}

  fmt.Println(prices[0])
  fmt.Println(prices[2])
} 
```

**Output**:
```
10
30 
```

##### Change Elements of an Array

You can also change the value of a specific array element by referring to the index number.

**Snippets**:
```go
package main
import ("fmt")

func main() {
  prices := [3]int{10,20,30}

  prices[2] = 50
  fmt.Println(prices)
}
```

**Output**:
```
[10 20 50] 
```

##### Array Initialization

If an array or one of its elements has not been initialized in the code, it is assigned the default value of its type.

> `Tip`: The default value for int is 0, and the default value for string is `""`.

**Snippets**:
```go
package main
import ("fmt")

func main() {
  arr1 := [5]int{} //not initialized
  arr2 := [5]int{1,2} //partially initialized
  arr3 := [5]int{1,2,3,4,5} //fully initialized

  fmt.Println(arr1)
  fmt.Println(arr2)
  fmt.Println(arr3)
}
```

**Output**:
```
[0 0 0 0 0]
[1 2 0 0 0]
[1 2 3 4 5] 
```

##### Initialize Only Specific Elements

This example initializes only the second and third elements of the array: 

**Snippets**:
```go
package main
import ("fmt")

func main() {
  arr1 := [5]int{1:10,2:40}

  fmt.Println(arr1)
}
```

**Output**:
```
[0 10 40 0 0] 
```

The array above has 5 elements.

- `1:10` means: assign `10` to array index `1` (second element).
- `2:40` means: assign `40` to array index `2` (third element).

**Find the Length of an Array**

The `len()` function is used to find the length of an array:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  arr1 := [4]string{"Volvo", "BMW", "Ford", "Mazda"}
  arr2 := [...]int{1,2,3,4,5,6}

  fmt.Println(len(arr1))
  fmt.Println(len(arr2))
}
```

**Output**:
```
4
6 
```

#### Slices

Slices are similar to arrays, but are more powerful and flexible. Like arrays, slices are also used to store multiple values of the same type in a single variable. However, unlike arrays, the length of a slice can grow and shrink as you see fit. In Go, there are several ways to create a slice:

- Using the []datatype{values} format
- Create a slice from an array
- Using the make() function

##### Create a Slice With []datatype{values}

**Syntax**:
```go
slice_name := []datatype{values} 
```

A common way of declaring a slice is like this:

**Snippets**:
```go
myslice := []int{}
```

The code above declares an empty slice of 0 length and 0 capacity.

To initialize the slice during declaration, use this:

**Snippets**:
```go
myslice := []int{1,2,3}
```

The code above declares a slice of integers of length 3 and also the capacity of 3.

In Go, there are two functions that can be used to return the length and capacity of a slice:

- len() function - returns the length of the slice (the number of elements in the slice)
- cap() function - returns the capacity of the slice (the number of elements the slice can grow or shrink to)

This example shows how to create slices using the `[]datatype{values}` format:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  myslice1 := []int{}
  fmt.Println(len(myslice1))
  fmt.Println(cap(myslice1))
  fmt.Println(myslice1)

  myslice2 := []string{"Go", "Slices", "Are", "Powerful"}
  fmt.Println(len(myslice2))
  fmt.Println(cap(myslice2))
  fmt.Println(myslice2)
}
```

**Output**:
```
0
0
[]
4
4
[Go Slices Are Powerful]
```

##### Create a Slice From an Array

You can create a slice by slicing an array:

**Syntax**:
```go
var myarray = [length]datatype{values} // An array
myslice := myarray[start:end] // A slice made from the array
```

**Snippets**:
```go
package main
import ("fmt")

func main() {
  arr1 := [6]int{10, 11, 12, 13, 14,15}
  myslice := arr1[2:4]

  fmt.Printf("myslice = %v\n", myslice)
  fmt.Printf("length = %d\n", len(myslice))
  fmt.Printf("capacity = %d\n", cap(myslice))
}
```

**Output**:
```
myslice = [12 13]
length = 2
capacity = 4
```

##### Create a Slice With The make() Function

The `make()` function can also be used to create a slice.

**Syntax**:
```go
slice_name := make([]type, length, capacity)
```

> Note: If the capacity parameter is not defined, it will be equal to length.

This example shows how to create slices using the make() function:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  myslice1 := make([]int, 5, 10)
  fmt.Printf("myslice1 = %v\n", myslice1)
  fmt.Printf("length = %d\n", len(myslice1))
  fmt.Printf("capacity = %d\n", cap(myslice1))

  // with omitted capacity
  myslice2 := make([]int, 5)
  fmt.Printf("myslice2 = %v\n", myslice2)
  fmt.Printf("length = %d\n", len(myslice2))
  fmt.Printf("capacity = %d\n", cap(myslice2))
}
```

**Output**:
```
myslice1 = [0 0 0 0 0]
length = 5
capacity = 10
myslice2 = [0 0 0 0 0]
length = 5
capacity = 5
```

##### Access Elements of a Slice

You can access a specific slice element by referring to the index number.

In Go, indexes start at `0`. That means that `[0]` is the first element, `[1]` is the second element, etc.

This example shows how to access the first and third elements in the prices slice:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  prices := []int{10,20,30}

  fmt.Println(prices[0])
  fmt.Println(prices[2])
}
```

**Output**:
```
10
30
```

##### Change Elements of a Slice

You can also change a specific slice element by referring to the index number.

This example shows how to change the third element in the prices slice:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  prices := []int{10,20,30}
  prices[2] = 50
  fmt.Println(prices[0])
  fmt.Println(prices[2])
}
```

**Output**:
```
10
50
```

##### Append Elements To a Slice

You can append elements to the end of a slice using the `append()` function:

**Syntax**:
```go
slice_name = append(slice_name, element1, element2, ...)
```

This example shows how to append elements to the end of a slice:

**Snippet**:
```go
package main
import ("fmt")

func main() {
  myslice1 := []int{1, 2, 3, 4, 5, 6}
  fmt.Printf("myslice1 = %v\n", myslice1)
  fmt.Printf("length = %d\n", len(myslice1))
  fmt.Printf("capacity = %d\n", cap(myslice1))

  myslice1 = append(myslice1, 20, 21)
  fmt.Printf("myslice1 = %v\n", myslice1)
  fmt.Printf("length = %d\n", len(myslice1))
  fmt.Printf("capacity = %d\n", cap(myslice1))
}
```

**Output**:
```
myslice1 = [1 2 3 4 5 6]
length = 6
capacity = 6
myslice1 = [1 2 3 4 5 6 20 21]
length = 8
capacity = 12
```

##### Append One Slice To Another Slice

To append all the elements of one slice to another slice, use the append()function:

**Syntax**:
```go
slice3 = append(slice1, slice2...)
```
> Note: The '...' after slice2 is necessary when appending the elements of one slice to another.

This example shows how to append one slice to another slice:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  myslice1 := []int{1,2,3}
  myslice2 := []int{4,5,6}
  myslice3 := append(myslice1, myslice2...)

  fmt.Printf("myslice3=%v\n", myslice3)
  fmt.Printf("length=%d\n", len(myslice3))
  fmt.Printf("capacity=%d\n", cap(myslice3))
}
```

**Output**:
```
myslice3=[1 2 3 4 5 6]
length=6
capacity=6
```

##### Change The Length of a Slice

Unlike arrays, it is possible to change the length of a slice.

This example shows how to change the length of a slice:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  arr1 := [6]int{9, 10, 11, 12, 13, 14} // An array
  myslice1 := arr1[1:5] // Slice array
  fmt.Printf("myslice1 = %v\n", myslice1)
  fmt.Printf("length = %d\n", len(myslice1))
  fmt.Printf("capacity = %d\n", cap(myslice1))

  myslice1 = arr1[1:3] // Change length by re-slicing the array
  fmt.Printf("myslice1 = %v\n", myslice1)
  fmt.Printf("length = %d\n", len(myslice1))
  fmt.Printf("capacity = %d\n", cap(myslice1))

  myslice1 = append(myslice1, 20, 21, 22, 23) // Change length by appending items
  fmt.Printf("myslice1 = %v\n", myslice1)
  fmt.Printf("length = %d\n", len(myslice1))
  fmt.Printf("capacity = %d\n", cap(myslice1))
}
```

**Output**:
```
myslice1 = [10 11 12 13]
length = 4
capacity = 5
myslice1 = [10 11]
length = 2
capacity = 5
myslice1 = [10 11 20 21 22 23]
length = 6
capacity = 10
```

##### Memory Efficiency

When using slices, Go loads all the underlying elements into the memory.

If the array is large and you need only a few elements, it is better to copy those elements using the copy() function.

The `copy()` function creates a new underlying array with only the required elements for the slice. This will reduce the memory used for the program. 

**Syntax**:
```go
copy(dest, src)
```

The `copy()` function takes in two slices dest and src, and copies data from src to dest. It returns the number of elements copied.

This example shows how to use the copy() function:

**Snippets**:
```go
package main
import ("fmt")

func main() {
  numbers := []int{1,2,3,4,5,6,7,8,9,10,11,12,13,14,15}
  // Original slice
  fmt.Printf("numbers = %v\n", numbers)
  fmt.Printf("length = %d\n", len(numbers))
  fmt.Printf("capacity = %d\n", cap(numbers))

  // Create copy with only needed numbers
  neededNumbers := numbers[:len(numbers)-10]
  numbersCopy := make([]int, len(neededNumbers))
  copy(numbersCopy, neededNumbers)

  fmt.Printf("numbersCopy = %v\n", numbersCopy)
  fmt.Printf("length = %d\n", len(numbersCopy))
  fmt.Printf("capacity = %d\n", cap(numbersCopy))
}
```

**Output**:
```
// Original slice
numbers = [1 2 3 4 5 6 7 8 9 10 11 12 13 14 15]
length = 15
capacity = 15
// New slice
numbersCopy = [1 2 3 4 5]
length = 5
capacity = 5
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

Go language has three functions to output text:

- Printf()
- Println()
- Print()

##### Printf()

Using `Printf()` formating function defined in fmt package, 
to display output on screen.

```go
fmt.Printf("Hello %v", name)
// Output: Hello, Aniket
```

Here, we use `PrintF()` function display `Hello, Aniket` accessing name variable.

`%d`: for digit
`%f`: for floating-point number

Learn more about:[Formating Verbs](https://www.w3schools.com/go/go_formatting_verbs.php)

##### Println()

The `Println()` function that a whitespace is added between the arguments, and a newline is added at the end

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var i,j string = "Hello","World"

  fmt.Println(i,j)
}
```

**Output**:
```
Hello World
```

##### Print()

The Print() function prints its arguments with their default format.

**Snippets**:
```go
package main
import ("fmt")

func main() {
  var i,j string = "Hello","World"

  fmt.Print(i)
  fmt.Print(j)
}
```

**Output**:
```
HelloWorld
```

### Operators

#### Arithmetic Operators


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

#### Relational Operators


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

#### Logical Operators


1. Logical `AND`: The `&&` operator returns true when both the conditions in consideration are satisfied. Otherwise it returns false. For example, `a && b` returns true when both a and b are true (i.e. non-zero).
2. Logical `OR`: The `||` operator returns true when one (or both) of the conditions in consideration is satisfied. Otherwise it returns false. For example, `a || b` returns true if one of a or b is true (i.e. non-zero). Of course, it returns true when both a and b are true.
3. Logical `NOT`: The `!` operator returns true the condition in consideration is not satisfied. Otherwise it returns false. For example, `!a` returns true if a is false, i.e. when `a=0`.

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

#### Bitwise Operators


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

#### Assignment Operators


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

#### Misc Operators

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
```
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

Learn more about: [Loops](https://www.w3schools.com/go/go_loops.php)

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

1.**Expression Switch Case**

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

2. **Type Switch Case**

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
```
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
```
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

### Reference

**Official Go DEV**: [Go Developer](https://go.dev/)

1. [GeeksForGeeks.org](https://www.geeksforgeeks.org/golang/)

2. [CodeAcademy.com](https://www.codecademy.com/learn/learn-go)

3. [W3Schools.com](https://www.w3schools.com/go/index.php)