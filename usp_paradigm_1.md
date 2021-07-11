# Introduction

The language Myth is a very easy to use and efficient language ,whose main ideas stem from the languages C, C++ and python.This language is not tied down to any one operating system. Our language has a variety of data types ranging from basic ones like int,float ,char to more complex derived data types like pointers ,arrays etc. and also allows you to create your own data types using the previously mentioned ones.

Our language covers all of the fundamental control flow statements required for making well structured programs; these range from the decision making(if -else) , selection of a specific case (switch) , looping with a termination case at the top (for, while) and a early loop exit in certain cases by ‘break’.

# Unique Selling Point

- For the users convenience, the language is developed to have more readability and efficiency. Although these two aspects of a programming language generally trades each other off, this programming language tries to find an effective middle ground. The user also has the option to use the specific in-built libraries to execute there program with parallel programming concepts, making the whole process a whole lot faster while trading off a little bit of the simplicity.
- Our language is designed in such a way that there are only minimal and affordable changes in syntax when compared to other mainstream programming languages. That way it is easier for a programmer to switch to this language from any mainstream programming background.
- This is a General purpose language providing readability and simplicity for end users and also enough flexibility for developers and programmers. Users can have higher productivity with the help of extensive in-built libraries.
- In this language the user can create their own libraries as well as link them to later codes as required. They can also call any pre-written code in a program. This will make this language a good fit for larger projects where multiple code files are needed. While importing the code from a pre-written code, the import will just paste the compiled output instead of the entire code to save memory.
- The Language also has extensive libraries to help working with popular data structures like stacks, queue etc. There are libraries to carry out certain popular algorithm like different sorting, searching etc along with maths libraries ranging from statistics, linear algebra and more.

# Programming Paradigm

### Imperative Language

In this language, we allow the user(programmer) to change the state of the program unlike a declarative language. The programmer has to specify the procedure for the program to follow in completing the given task.

### Static Typing Language

Static typing refers to when data types need to be static at run time. This means they need to be set properly at compilation and cannot change without a properly defined operation in the language or type casting into a new variable. e.g. 

```c
int variableName = 10;
```

## Programming Paradigms supported

### Procedural Programming

Procedural programming is a programming paradigm, derived from structured programming, based on the concept of the procedure call. Procedural programming breaks down a programming task into a collection of variables, data structures, and subroutines. As majority of new programmers learns procedural programming at the beginning, even a new programmer can have a good experience with our programming language.

### Object Oriented Programming

The programmer in our language is given the choice to organize software design around data, or objects, rather than functions and logic. The user can make their own classes with user-specified attributes and methods. These classes can be used to construct objects later. The programming language follows the 4 main concepts of object oriented programming i.e. Inheritance, Encapsulation, Polymorphism and Abstraction.

### Parallel Programming (Expanded later)

Parallel computing is a type of computation where many calculations or the execution of processes are carried out simultaneously. Since most modern computers have multiple cores, instead of using only a single core to execute our program, large problems can often be divided into smaller ones, which can then be solved at the same time. 

The main aim of the tutorial is to show the essential elements of the programming language that are enough to create a basic program,compile and run it, and we end up going into more complex parts as we go along.The basics consist of variables, the conditional statements , control flow, arithmetic operators, functions and the basics of input and output.

Let’s start with a set of examples that give us a good idea of the syntax that we have to follow to create a basic program and what errors to avoid.

Starting with the holy grail of all programming languages let us print ‘Hello World’.

## Do's and Don'ts

While declaring any variable we have to use lowercase alphabets since our language is case sensitive. So
int and INT have different meanings.

```
Int a               # WRONG
int a               # RIGHT
Float a             # WRONG
float a             # RIGHT
int a = 10          # RIGHT)
a = 10              # WRONG)
```

While printing, we can use '+' to concatenate multiple variables and strings.

```
int age = 25
print(" My age is ",  age)       #(WRONG), 
```

```
print(" My age is " + age)       #(RIGHT)
```

```
int a, b
input(a, b)           #(RIGHT)

input(a  b)           #wrong
input(a, ,b)          #wrong
```

Running a for loop to get 10 iterations

```
for(i in range(1,11))      # RIGHT 
for(i in range(1,10))      # WRONG : the loop will iterate only for 9 times, not considering the value 10
for i in range(1,11)       # WRONG : Syntax Error
```

Let i be an integer variable with a value between 1-10. Suppose if we want to use "if" statement if i
equals 5.

```
if(i == 5)                 # RIGHT
if(i = 5)                  # WRONG
while comparing 2 integers we use '==' instead of '='

if i == 5                  # WRONG
```