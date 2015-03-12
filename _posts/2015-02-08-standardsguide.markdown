---
layout: post
title:  "Left Shark"
date:   2015-02-07 14:46:39
categories: bizleg
---
Splattershmup Coding Style/Standards Sheet
==================================

## C-Sharp
### Spacing

##### Spaces
Use four spaces for indenting. Do not use a hardware tab to indent.

##### Braces
Put braces on the next line, everywhere (if, else, functions, structures, class definitions, etc.)

```
if(condition)
{
	// Code
}
```

The else statement starts on the next line after the last closing brace.

```
if(condition)
{
	// Code
}
else
{
	// More Code
}
```

### Floating Point Precision
Use precision specification for floating point values unless there is an explicit need for a double.

```
float f = 0.5f;
```


Instead of

```
float f = 0.5;
```


And

```
float f = 1.0f;
```


Instead of

```
float f = 1.f;
```

### Naming Conventions
##### Methods
Method names should be [pascal cased](http://c2.com/cgi/wiki?UpperCamelCase)

```
void Foo();
void FooAndBar();
```

##### Variables
Variable names should be [camel cased](http://c2.com/cgi/wiki?LowerCamelCase)

```
int health;
int hitCounter;
```

Private Variables should start with an underscore:

```
int _myPrivateInt;
```

Variables that are intended to have a constant value (although are changed in the Unity Editor) should be in all caps with underscores between words.

```
int MAX_PARTICLES = 100;
```

Variables that are public and will be edited in the editor will have their initial values specified on their declaration line rather than in the constructor.
##### Structs and Classes
Struct and class names should be [pascal cased](http://c2.com/cgi/wiki?UpperCamelCase)

```
struct ExplosionData;
```

##### Enums
Enum names use the same naming convention as Classes. The enum constants should be all caps with underscores between words.

```
enum Contact
{
	NONE,
	EDGE,
	MODEL_VERTEX,
	TRM_VERTEX
};
```

### Commenting
Everything should use Microsoft's C# XML Comments. If you are unsure of how to do this please read [this guide](http://msdn.microsoft.com/en-us/library/aa288481(v=vs.71).aspx)

### Line Length
Avoid having lines with a length greater than 80 characters. The hard limit for line length is 120 characters, at this point you should split the function call  or whatever you're doing among different lines with appropriate indenting on the next line down.


This page was heavily inspired by the [Dash Coding Standards Sheet](https://github.com/Circular-Studios/Dash/wiki/Coding-Standards)
