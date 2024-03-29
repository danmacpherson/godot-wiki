#  Introduction 

GDScript is a high level, dynamically typed programming language used to create content. It uses a syntax that is very similar to the Python language (blocks are indent-based) and it’s goal is to be very optimal and tigthly integrated with the engine, allowing great flexibility for content creation and integration.

#  History 

Initially, Godot was designed to support multiple scripting languages (this ability still exists today). However, only GDScript is in use right now. There is a little history behind this. 

In the early days, the engine used the [Lua](http://www.lua.org/) scripting language. Lua is fast, but creating bindings to an object oriented system (by using fallbacks) was complex and slow and took an enormous amount of code. After some experiments with [Python](http://www.python.org/), it also proved difficult to embed. 

The last third party scripting language that was used for shipped games was [Squirrel](http://squirrel-lang.org/), but it was also dropped too. At that point, it became evident that Godot would work more optimally by using a built-in scripting language, as the following barriers were met:

*  Godot embeds scripts in nodes, most languages are not designed with this in mind.
*  Godot uses several built-in datatypes for 2D and 3D math, script languages do not provide this, and binding them is inefficient.
*  Godot uses threads heavily for lifting and initializing data from the net or disk, script interpreters for common languages are not friendly to this.
*  Godot already has a memory management model for resources, most script languages provide their own, which resulted in duplicate effort and bugs.
*  Binding code is always messy and results in several failure points, unexpected bugs and general unmaintaniability.

Finally, GDScript was written. The language and interpreter for it ended up being smaller than the binding code itself for Lua and Squirrel, and equally as functional. With time, having a built in language ended up being a huge advantage.

#  Example 

Some people can learn better by just taking a look at the syntax, so here’s a simple example of how it looks.

```python
#a file is a class!

# inheritance

extends BaseClass

# member variables

var a=5 
var s="Hello"
var arr=[1,2,3]
var dict={"key":"value", 2:3}

# constants

const answer=42
const thename="Charly"

# built-in vector types

var v2 = Vector2(1,2)
var v3 = Vector3(1,2,3)

# function

func some_function(param1,param2):
    var local_var=5

    if param1 < local_var:
        print(param1)
    elif param2 > 5:
        print(param2)
    else:
        print("fail!")

    for i in range(20):
        print(i)

    while(param2!=0):
        param2-=1

    var local_var2 = param1+3
    return local_var2


# subclass

class Something:
    var a=10

# constructor

func _init():
    print("constructed!")
    var lv = Something.new()
    print(lv.a)
    
#pass

    
func emptyfunc():
     pass # pass does nothing, allows an empty function
     
```
    
#  Language 

##  Identifiers 

Any string that restricts itself to alphabetic characters (’a’ to ’z’ and ’A’ to ’Z’), digits (’0’ to ’9’) and ’_’ qualifies as an identifier. As an extra restriction, identifiers must not begin with a digit. Identifiers are case-sensitive (’foo’ is different to ’FOO’).

##  Keywords 

The following is the list of keywords supported by the language. Since keywords are reserved words (tokens), they can’t be used as identifiers:

**and break class const continue elif else enum export extends false for func if in null or pass return self tool true var while**

##  Operators 

The following is the list of supported operators and their precedence (TODO, change since this was made to reflect python operators)

| Operator              | Description                    |                            
| -------- | ----------- |                            
| `x[index]`          | Subscription, Highest Priority |                            
| x.attribute           | Attribute Reference            |                            
| extends               | Instance Type Checker          |                            
| `~`                 | Bitwise NOT                    |                            
| -x                    | Negative                       |                            
| * / %                 | Mult / Div / Remainder         |                            
| + -                   | Addition / Substraction        |                            
| `<< >>`             | Bit Shifting                   |                            
| &                     | Bitwise AND                    |                            
| `^`                 | Bitwise XOR                    |                            
| `                    | `                             | Bitwise OR                  |           
| `< > == != >= <=`   | Comparisons                    |                            
 in                    | Content Test                   |                            
| `! not`             | Boolean NOT                    |                            
| and &&                | Boolean AND                    |                            
| or `||`                          | Boolean OR | 
| `= += -= *= /= %= &= | =` | Assignment, Lowest Priority |           

##  Literals 

| Literal               | Name                         | 
| -------               | ----                         | 
| 45                    | Base 10 Integer              | 
| 0x8F51                | Base 16 (hex) Integer        | 
| 3.14, 58.1e-10        | Floating Point Number (real) | 
| ’Hello’, “Hi” | Strings                      | 
| @"Node/Label"         | Node Path or StringName      | 

##  Comments 

Anything from a ’#’ to the end of the line is ignored and is considered a comment.

```python
# This is a comment
```

#  Built-in Types 

##  Basic Bult-In Types 

A variable in GDScript can be assigned many of several built-in types.

###  null 

’null’ is a data type that contains no information, nothing assigned, and it’s just empy. It can only be set to one value: ’null’.

###  bool 

Boolean data type, can only contain ’true’ or ’false’.

###  int 

Integer data type, can only contain integer numbers, negative and positive.

###  float 

contains a floating point value (real).

###  String 

Sequence of characters in unicode format. Strings can contain the standard C escape sequences.

##  Vector Built-In Types 

###  Vector2/Size2 

2D vector type, containing x and y fields. Can alternatively access fields as width and height for readability. Can also be accessed as array.

###  Rect2 

2D Rectangle type. Contains 2 vectors fields, “pos” and size’’. Alternatively contains an “end” field which is “pos+size”.

###  Vector3 

3D vector type. Contains x, y and z fields. Can also be accessed as array.

###  Matrix32 

3x2 matrix used for 2D transforms.

###  Plane 

3D Plane type in normalized form. Contains a “normal” vector field and a “d” scalar distance.

###  Quat 

Quaternion, datatype used for representing a 3D rotation. It’s useful for interpolating rotations.

###  AABB/Box3 

Axis Aligned bounding box (or alternatively, 3D box). Contains 2 vectors fields, “pos” and size’’. Alternatively contains an “end” field which is “pos+size”.

###  Matrix3 

3x3 matrix used for 3D rotation and scale. Contains 3 vector fields x,y and z. Can also be accessed as array of 3D vectors.

###  Transform 

3D Transform, contains a Matrix3 field “basis” and a Vector3 field “origin”.

##  Engine Built-In Types 

###  Color 

Color datatype, contains r,g,b,a fields. Can also be accessed as h,s,v for hue/saturation/value.

###  Image 

Contains a 2D Image of custom format and allows direct access to the pixels.

###  NodePath 

Compiled path to a node, used mainly in the scene system. Can be easily asigned from/to a String.

###  RID 

Resource ID (RID). Servers use generic RIDs to reference opaque data.

###  Object 

Base class for anything not a built-in type.

###  InputEvent 

Events from input devices are contained in very compact form in InputEvent objects. Due to fact they can be received in high amounts from frame to frame, they are optimized in their own datatype.

##  Container Built-In Types 

###  Array 

Generic sequence of objects. It’s size can be changed to anything and starts from index 0.

```python
var arr=[]
arr=[1,2,3]
arr[0]="Hi!"
```
Arrays are allocated linearly in memory, so they are fast, but very large arrays (more than tens of thousands of elements) may cause fragmentation. 

There are specialized arrays (listed below) for some built-in datatypes which do not suffer from this and use  less memory, but they are atomic and generally run a little slower, so they are only justified for very large amount of data.

###  Dictionary 

Associative container which contains values referenced by unique keys.

```python
var d={4:5, "a key":"a value", 28:[1,2,3]}
d["Hi!"]=0
```

Lua-style table syntax is also supported, given it's easier to write and read:

```python

var d= {
    somekey=2,
    otherkey=[2,3,4],
    morekey="Hello"
}
```

###  ByteArray 

Array of bytes. Can only contains bytes (integers from 0 to 255). Optimized for memory usage, can’t fragment the memory.

###  IntArray 

Array of integers. Can only contain integers. Optimized for memory usage, can’t fragment the memory.

###  FloatArray 

Array of floats, can only contain floats. Optimized for memory usage, can’t fragment the memory.

###  StringArray 

Array of strings, can only contain strings. Optimized for memory usage, can’t fragment the memory.

###  Vector2Array 

Array of Vector2, can only contain 2D Vectors. Optimized for memory usage, can’t fragment the memory.

###  Vector3Array 

Array of Vector3, can only contain 3D Vectors. Optimized for memory usage, can’t fragment the memory.

###  ColorArray 

Array of Color, can only contains colors. Optimized for memory usage, can’t fragment the memory.

#  Data 

##  Variables 

Variables can exist as class members or local to functions. They are created with the “var” keyword and may be, optionally, be assigned a value upon initialization.

```python
var a # datatype is null by default
var b = 5
var c = 3.8
var d = b+c # variables are always initialized in order
```
##  Constants 

Constants are similar to variables, but must be constants or constant expressions and must be assigned on initialization.

```python
const a = 5
const b = Vector2(20,20)
const c = 10+20 # constant expression
const d = Vector2(20,30).x # constant expression: 20
const e = [1,2,3,4][0] # constant expression: 1
const f = sin(20) # sin() can be used in constant expression
const g = x+20 # invalid, not a constant expression!
```
##  Functions 

Functions always belong to a class. The scope priority for variable look-up is: local -> class member -> global. “self” is provided as an option for accessing class members but is not required always (and must *not* be defined as first parameter, like in Python). For performance reasons, functions are not considered class members, so they can’t be referenced directly. A function can return at any point. The default return value is null.

```python
    func myfunction(a,b):
    print(a)
    print(b)
    return a+b # return is optional, otherwise null is returned
```
###  Statements and Control Flow 

Statements are standard, and can be assignments, function calls, control flow structures, etc (see below). “;” as separator is entirely optional.

###  if/else/elif 

Simple conditions are created by using the *if/else/elif* syntax. Parenthesis around statements is allowed but not requiered. Given the nature of the tab-based indentation, elif can be used instead of else:/if: to mantain a level of indentation.

```python
if [expression]:
    statement(s)
elif [expression]:
    statement(s)
else:
    statement(s)
```
###  while 

Simple loops are created by using *while* syntax. Loops can be broken using *break*, or continued using *continue*:

```python
while [expression]:
    statement(s)
```
###  for 

To iterate a range, array or table a *for* loop is used. For loops store the index in the loop variable on each iteration.

```python
for i in [0,1,2]:
    statement # loop iterates 3 times, i being 0,1 and 2

var dict = {"a":0, "b":1, "c": 2}
for i in dict:
    print(dict[i]) # loop iterates the keys, i being "a","b" and c". It prints 0, 1 and 2.

for i in range(3):
    statement # similar to [0,1,2] but does not allocate an array

for i in range(1,3):
    statement # similar to [1,2] but does not allocate an array

for i in range(2,8,2):
    statement # similar to [2,4,6] but does not allocate an array
```
#  Classes 

By default, the body of a script file is an unnamed class, and it can only be referenced externally as a resource or file. Class syntax is meant to be very compact and can only contain member variables or functions. Static functions are allowed, but not static members (in the spirit of thread safety, since scripts can be initialized in separate threads without the user knowing). In the same way, member variables (including arrays and dictionaries) are initialized every time an instance is created.

##  Class File Example 

Example of a class file, imagine it being stored in a file like myclass.gd.

```python

var a=5

func print_value_of_a():
    print(a)
```
##  Inheritance 

A class-file can inherit from a global class, another file or a subclass inside another file. Multiple inheritance is not allowed. The “extends” syntax is used:

```python
# extend from some class (global)
extends SomeClass 

# optionally, extend from another file

extends "somefile.gd" 

# extend from a subclass in another file

extends "somefile.gd".Subclass 
```
##  Inheritance Testing 

It is possible to check if an instance inherits from a given class. For this the “extends” keyword can be used as an operator instead:

```python
const enemy_class = preload("enemy.gd") # cache the enemy class

[..]

if ( entity extends enemy_class ):
    entity.apply_damage()
```
##  Constructor 

A class can have an optional constructor, a function named “_init” that is called when the class is instanced.

##  Sub Classes 

A class file can have subclasses. Syntax should be straightforward:

```python
class SomeSubClass:
    var a=5
    func print_value_of_a():
        print(a)

func _init():
    var sc = SomeSubClass.new() #instance by calling built-in new
    sc.print_value_of_a()
```
##  Classes as Objects 

It may be desired at some point to load a class from a file and then instance it. Since the global scope does not exist, classes must be loaded as a resource. Instancing is done by calling the “new” function in a class object:

```python

#load the class (loaded every time the script is instanced)
var MyClass = load("myclass.gd")

# alternatively, using the preload() function preloads the class at compile time

var MyClass2 = preload("myclass.gd")

func _init():
    var a = MyClass.new()
    a.somefunction()
```
##  Exports 

Class members can be exported. This means their value gets saved along with a scene. If class members have initializers to constant expressions, they will be available for editing in the property editor. Exporting is done by using the export keyword:

```python
extends Button

export var data # value will be saved
export var number=5 # also available to the property editor
```

One of the fundamental benefits of exporting member variables is to have them visible in the property editor. This way artists and game designers can modify values that later influence how the program runs. For this, a special export syntax is provided for more detail in the exported variables:

```python
#if the exported value assigns a constant or constant expression, the type will be infered and used in the editor

export var number=5

# export can take a basic datatype as argument, which will be used in the editor

export(int) var number

# export can also take a resource type as hint

export(Texture) var character_face

# integers and strings hint enumerated values

export(int,"Warrior","Magician","Thief") var character_class # (editor will set them as 0,1 and 2) 
export(String,"Rebecca","Mary","Leah") var character_name 

# strings as paths

export(String,FILE) var f # string is a path to a file
export(String,DIR) var f # string is a path to a directory
export(String,FILE,"*.txt") var f # string is a path to a file, custom filter provided as hint

# integers and floats hint ranges

export(int,20) var i # 0 to 20 allowed
export(int,-10,20) var j # -10 to 20 allowed
export(float,-10,20,0.2) var k # -10 to 20 allowed, with stepping of 0.2

# color can hint availability of alpha

export(Color,RGB) var col # Color is RGB
export(Color,RGBA) var col # Color is RGBA

```
It must be noted that even if the script is not being run while at the editor, the exported properties are still editable (see below for “tool”).

##  Static Functions 

A function can be declared static. When static, it has no access to the instance member variables or “self”. This is mainly useful to make libraries of helper functions:

```python

static func sum2(a,b):
    return a+b
```
##  Tool Mode 

Scripts by default don’t run inside the editor, and only the exported properties can be changed. In some cases it is desired that they do (as long as they don’t execute game code or manually avoid doing so). For this, the “tool” keyword exists, and must be placed at the top of the file:

```python
tool
extends Button

func _init():
    print("Hello")
```
##  Memory Management 

If a class inherits from *Reference*, then instances will be freed when no longer in use. No garbage collector exists, just simple reference counting. By default, all classes that don’t define inheritance extend *Reference*. If this is not desired, then a class must inherit *Object* manually and must call instance.free(). To avoid reference cycles that can’t be freed, a weakref() function is provided for creating weak references.

##  Function References 

Functions can’t be referenced because they are not treated as class members. There are two alternatives to this, though. The “call” function or the funcref() helper.

```python
instance.call("funcname",args) # call a function by bane

var fr = funcref(instance,"funcname") #create a function ref
fr.exec(args)

```

 --- //[Juan Linietsky](reduzio@gmail.com) 2013/11/10 18:09//
