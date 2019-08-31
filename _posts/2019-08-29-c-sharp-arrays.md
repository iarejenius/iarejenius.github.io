---
title: Multidimensional arrays in C#
published: true
---

Quick question for you: what's the difference between this syntax
``` csharp
static void UseMultidimensionalArray(int[][] multidimensionalArray)
{
    Console.WriteLine(multidimensionalArray[0][0]);
}
```
and this syntax?
``` csharp
static void UseMultidimensionalArray(int[,] multidimensionalArray)
{
    Console.WriteLine(multidimensionalArray[0,0]);
}
```

I was recently working on a problem that involved a two-dimensional array and found myself stumbling over this small syntax difference. 

Now, I probably haven't had to deal with multidimensional array taking computer science classes in college and this was part of the problem. I was working in C++ and Java back then and if you wanted a `2x2` matrix, you declared or initialized it with those dimensions:
```cpp
// C++
int twoByTwo[2][2] = { {1,2}, {3,4} };
```
```java
// Java
int[][] twoByTwo = new int[2][2];
```

But in C#, if you ever find yourself writing `[2][2]` to declare or initialize an array, you're doing something wrong. This is a compilation error:
```csharp
var twoByTwo = new int[2][2];
```
But these aren't:
```csharp
var twoByTwo_v1 = new int[2][];
var twoByTwo_v2 = new int[2,2];
```
The first version is a _jagged array_, meaning that each array entry is an array of potentially different length _e.g._
```csharp
int[][] jaggedArray = new int[2][] {
    new int[1] {44},
    new int[3] {1,2,3}
};
Console.WriteLine(jaggedArray[1][1]); // 2
```
The second version is what we want if we're looking for rigid dimensions _e.g._
```csharp
int[,] twoByTwo = new int[2,2] {
    {1,2},
    {3,4}
};
Console.WriteLine(twoByTwo[0,1]); // 2
```

It boils down to the following in C#:

- Array dimensions are never specified in the declaration
- Array dimensions are required in the initialization
- [][] == jagged array
- [,] == multidimensional array