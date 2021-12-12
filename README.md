# Structure of Programming Languages - Project

In the following example code, the following programming paradigms will be showcased:
1. [Compiled vs. Interpreted](#compiled-vs-interpreted)
2. [Automatic Garbage Collection vs. Manual Allocation and Deallocation](#automatic-garbage-collection-vs-manual-allocation-and-deallocation)
3. [Lexical Scoping vs Global, Local & Block Scoping](#lexical-scoping-vs-global-local--block-scoping)
4. [Final Code](#final-code)

## Code Submissions

Below, I showcase each programming paradigm and provide some sample code that illustrates it.
The Final Submission Section includes the explanation of the final code and paradigms.

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

## Automatic Garbage Collection vs Manual Allocation and Deallocation
For C++ there is no garbage collection so you have to allocate and deallocate manually. 

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
```
Output:
Global number: 1
Local number: 2
Block number: 3
```
R uses Lexical Scoping which in R programming means that the values of the free variables are searched for in the environment in which the function was defined.
```R
f <- function(x, y)
{
  x * y * z
}
```
z is the free variable in this

## Final Code
```C++
#include<iostream>
using namespace std;
 
int fib(int n)
{
    if (n <= 1)
        return n;
    return fib(n-1) + fib(n-2);
}
 
int main ()
{
    int n = 9;
    cout << fib(n);
    getchar();
    return 0;
}
```
We will compile this with 
```clang++ -std=C++11 Fib.cpp``` 
Then since we don't have to allocate any objects then we don't need garbage collection. Lastly, local scoping is used in the main function and fib.
```R
recurse_fibonacci <- function(n) {
if(n <= 1) {
return(n)
} else {
return(recurse_fibonacci(n-1) + recurse_fibonacci(n-2))
}
}
# take input from the user
nterms = as.integer(readline(prompt="How many terms? "))
# check if the number of terms is valid
if(nterms <= 0) {
print("Enter a positive integer: ")
} else {
print("Fibonacci sequence:")
for(i in 0:(nterms-1)) {
print(recurse_fibonacci(i))
}
}
```
In this the code is interpreted so we do not have to compile it. The garbage collection will automatically clean up any left over unused variables and such. Lastly, the lexical scoping will automatically pull any variable with the same name and use that.
