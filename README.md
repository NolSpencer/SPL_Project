# Structure of Programming Languages - Project

In the following example code, the following programming paradigms will be showcased:
1. [Compiled vs. Interpreted](#compiled-vs-interpreted)
2. [Automatic Garbage Collection vs. Manual Garbage Collection](#automatic-garbage-collection-vs-manual-garbage-collection)
3. [Lexical Scoping vs Global, Local & Block Scoping](#lexical-scoping-vs-global-local--block-scoping)

## Code Submissions

Below, I showcase each programming paradigm and provide some sample code that illustrates it.

# Paradigms

## Compiled vs Interpreted
R is an interpreted language because it will automatically run the scripts and thus doesn't need compiled.
![image](https://user-images.githubusercontent.com/77764696/145339180-f0066faf-04c8-41b6-96bf-31b46c7364a9.png)

C++ needs to be compiled to run

```C++
int main(){
  std::cout << "Hello World" << endl;
}
```
To compile and run
```
clang++ -std=c++11 main.cpp
./a.out
```

## Automatic Garbage Collection vs Manual Garbage Collection
C++ You manually will have to deallocate resources

```C++
n = new sample_object;
delete n;
```
For R
GC automatically releases memory when an object is no longer used. It does this by tracking how many names point to each object, and when there are no names pointing to an object, it deletes that object.

## Lexical Scoping vs Global, Local & Block Scoping
In C++ there are 3 types of scoping. Global Scoping, Local Scoping, and Block Scoping. An example of each is below.

C++ Scoping
```C++
//Scoping
int num = 1;
int main ()
{
  cout << "Global number: " << num << endl;
  int num = 2;
  cout << "Local number: " << num << endl;
  {
    int num = 3;
    cout << "Block number: " << num << endl;
  }
  return 0;
}
```
Output:
Global number: 1
Local number: 2
Block number: 3

R uses Lexical Scoping which in R programming means that the values of the free variables are searched for in the environment in which the function was defined.
```R
f <- function(x, y)
{
  x * y * z
}
```
z is the free variable in this


