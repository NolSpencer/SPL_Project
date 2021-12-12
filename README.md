# Structure of Programming Languages - Project

C++ and R are both very influential in 

In the following example code, the following programming paradigms will be showcased:
1. [Compiled vs. Interpreted](#compiled-vs-interpreted)
2. [Automatic Garbage Collection vs. Manual Garbage Collection](#automatic-garbage-collection-vs-manual-garbage-collection)
3. [Pass by Value & Reference vs. Dynamic Passing](#pass-by-value--reference-vs-dynamic-passing)
4. [Static Typing vs. Dynamic Typing](#static-typing-vs-dynamic-typing) 

These paradigms are all present within the final [submission code](#project-submission).

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

GC automatically releases memory when an object is no longer used. It does this by tracking how many names point to each object, and when there are no names pointing to an object, it deletes that object.

## 





