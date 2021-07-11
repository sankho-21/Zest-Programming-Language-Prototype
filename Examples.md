# Examples

## Lexical Rules

- Identifier can't start with digit/special character

```c
int a = 5
int a_1 = 10
```

```c
int 1_a = 10
int #number = 10
```

```c
void myfunc(){
print("This is the correct convention")
}
```

```c
void #myfunc(){
print("Function name cannot start with a special character and can have only '_' in special characters in between the name")
}

void 1stfunction(){
print("Function cannot start with a number as well but numbers can be used ain between or end of the name")
}
```

- Can't use keywords as variable names

```c
int floats = 10
```

```c
int float = 10  # float is a keyword
```

- Comments

```c
int a = 10  # This is a comment
```

```c
int a = 10 //this is not a comment 
```

- Escape characters

```c
print("line1 \n line2") # Prints line1 on first line and line2 on the second line
print('sun\'s flare')
print('Backslash can be printed by \\')
```

```c
print("line1 /n line2") # Prints : line1 /n line2
print('sun's flare')
print('This does not print a backslash \')
```

- string should always be in quotes

```c
print("This is a string")
print('This is a string as well')
```

```c
print(We must write strings in quotes)
```

## Syntax Rules

- Variable Declaration

```c
CONFORM
int a = 1 #variables with same type can be declared on two line
int b = 0

int a = 1, b = 0 #variables with same type can be declared on the same line as well
```

```c
DO NOT CONFORM
int a, float b #variables of different types cannot be declared on the same line
int a,int b    #Error
```

```cpp
CONFIRM
int a = 5
a = 10      #correct assignment acn be done any number of times
```

```cpp
DO NOT CONFIRM
int a = 5
int a = 10      #a variable cannot be declared more than once in a single block except if its in a sub-block
```

```c
STRING EXAMPLE
1
input/declaration
2
im/mutabale
3
adding two strings and storing it in first string
4
byte example

```

- Function parameters should separated by ','

```c
CONFORM
int power(int a, int b){
		int c = a ** b
		return c
}
int main(){
		int p = 10
		int r = power(p, 2)
		print(r)
}
```

```c
DO NOT CONFORM
int power(int a, int b){
		int c = a ** b
		return c
}
int main(){
		int p = 10
		int r = power(p; 2)  # Using a semicolon instead of comma will raise an error
		print(r)
}
```

- If statements

```c
CONFORM
if(a < b){
		print("B is greater")
}
else if(a > b){
		print("A is greater")
}
else{
		print("Both are equal")
}
```

```c
CONFORM
if(a < b){
		print("B is greater") 
}
if(a >= b){
		print("A is greater or equal to B")
}
```

```c
DO NOT CONFORM
else if(a > b){
			print("Error here") #Error : else if and else cannot be used without a if statement in the beginning
}
else{
		print("Error here as well")
}
```

```cpp
CONFIRM
if(a == 5){           # correct method to make comparisons
		#some code
}
```

```cpp
DO NOT CONFIRM
if(a = 5){        # to make comparisons we use "=="
   #some code
}
```

- Switch case

```c
CONFORM
int a
print("Enter a digit less than 3: ")
input(a)

switch(a){
		case(1){
				print("1")
				break
		}
		case(2){
				print("2")
				break
		}
		case(2){
				print("2")
				break
		}
		default{
				print("Default")
		}
}
```

```c
DO NOT CONFORM
int a
print("Enter a digit less than 3: ")
input(a)

switch(a){
		case(1):
				print("1")
				break
		case(2):
				print("2")
				break
		case(2):
				print("2")
				break
		default:
				print("Default")
}
```

- for -*****************

```cpp
CONFIRM
int array Array = {1, 2, 3, 4, 5, 6}
for(int i in Array){     #prints all the elements of the array 
		print(i)
}

**********************range example ********
```

```cpp
DO NOT CONFIRM
int array Array = {1,2,3,4,5,6}
for(int i in array Array){
		print(i)              #it will show an error as a new array is being declared (array is a data type in ZEST)
}
```

- skip***************

```cpp
CONFORM
int i = 0         #suppose we want to print all numbers from 0-9 except 5
while(i < 10){		
		if(i==5){
				continue    #correct method (with continue only the current iteration is skipped)
		}
		print(i)            
		i++
}

int i = 0          #suppose we want to print all numbers from 0-9 except 5
while(i < 10){		
		if(i==5){
				break    #when we use break control moves out of the loop
		}
		print(i)            
		i++
}

```

```cpp
**********DO NOT
(int i < 10)
```

do while*************

OPERATOR PRECEDENCE

```cpp
CONFORM
int a = 10
int b = 6
int avg = (a+b)/2            #avg = 8  

# ZEST follows BODMAS for precedence of arithmethic operators

```

```cpp
DO NOT CONFIRM
int a = 10
int b = 6
int avg = a+b/2          #avg = 13

#since "/" has more precedence than "+"

```

```cpp
CONFORM
int a
int b = 5
int c = 10
a = b==c      #here first b==c is evaluated the a is assigned to "b==c" which is 0
```

```cpp
DO NOT CONFORM
int a
int b = 5
int c = 10
b==c = a      #here first b==c is evaluated which is 0 and 0 = a is invalid.
```

LOGICAL OPERATIONS

```cpp
CONFIRM
int a,b,c
input(a,b,c)
if(a==b && a==c){
		print("all the numbers are equal")
}
```

```cpp
DO NOT CONFIRM
int a,b,c
input(a,b,c)
if(a==b & a==c){          #the operator for logical "AND" is "&&" (single "&" is used for bitwise operations)
		print("all the numbers are equal")
}
```

```cpp
DO NOT CONFIRM
int a,b,c
input(a,b,c)
if(a==b and a==c){      #the operator for logical "AND" is "&&" ("and","or" and "not" are not a logical operator)
		print(all the numbers are equal)
}
```

## Typing Rules

TYPE CONVERSION

```cpp
CONFORM
int b = 5
int c = 2
float a = b/(float)c     #a = 2.5 (if one of the operands is more expressive, then the more expressive operation takes place like float is more expressive than int) 
												# so by float division 5/(float)2 = 2.5
```

```cpp
	DO NOT CONFORM		    
	int b = 5
	int c = 2
	float a = b/c       #a = 2 result of integer division is always an integer irrespective of the data type of a 
   
```

- Accessing out of size element of array

```c
CONFIRM
int main(){
		int array arr1
		for(int i in range(0,6))
		{
			arr1[i] = i
		}
		int a = arr1[2]
		print(a,arr1.len()) #prints 1 and 5
}
```

```c
DO NOT CONFIRM
int main(){
		int array arr1 = [1, 2, 3, 4, 5]
		int a = arr1[10] #Error : array arr1 is of size 5 therefore can't access an element at 10th position in the array
		print(a,arr1.len())
}
```

- Function prototype and function call

```c
CONFORM
int sum(int a, int b){
		int c = a + b
		return c
}

int main(){
		int p = 10
		int q = 5
		int r = sum(p, q)
		print(r)
}
```

```c
DO NOT CONFORM
int sum(int a, int b){
		int c = a + b
		return c
};

int main(){
		int p = 10
		int r = sum(p) #Error : Another variable of int type has to be passed as a parameter to function sum according to the function definition
		print(r)
}
```

FUNCTION OVERLOADING 

```cpp
CONFORM

float Average(int a, int b){    #*1
		return (a+b)/2
}

float Average(int a, int b, int c){   #*2
		return (a+b+c)/3
}

int main(){
		int avg1 = Average(2, 4)            #when called with 2 parameters *1 is called
		int avg2 = Average(5, 10, 20)       #when called with 3 parameters *2 is called  
}
```

```cpp
CONFIRM

float function(float a, float b){	   # *1
	return a+b;
}

float function(int a, int b){       # *2
	return a+b;
}

int main(){

	float sum1 = function(2.2, 3.0)   # when called with two floats *1 is called
	float sum2 = function(2,2)        # when called with two ints *2 is called
	
	
}
```

```cpp
DO NOT CONFIRM

int function(int a, int b){
		return a+b
}

float function(int a, int b){
		return a/b;
}

int main(){
		function(5, 10)     #not clear which function to call
}
```

RETURN TYPES

```cpp
CONFIRM
int function(int a, int b){
		#some code
		return a+b        #except for functions with void return type all other function should have a return statement
}
```

```cpp
DO NOT CONFIRM
int function(int a, int b){
		#some code
		return        #the return statement should return something
}
```

## OOP and function overlaoding(pratyush and Sujeeth)

```cpp
class  Myclass{
		int a        #public
    int .b       #private
		int ..c      #protected

}
```

```cpp
  class First{
				int operand1      #when just declared the Access Specifier is assumed to be public
        int operand2
        float result
  }

	int main()
	{
			First calc
      calc.operand1 = 10
			calc.operand2 = 6
			calc.result = calc.operand1+calc.operand2
			return 0
	}
```

```cpp
class First{
     int .roll_no
     int score 
}

int main()
{
		First result
		result.roll_no  = 5    #Error:can't manipulate the variables declared as private
    result.score = 95
    return 0
}
```

```cpp
class Try{
		void output(){
				 print("Hello")
		}
}

int main()
{
		Try myObj
    myObj.output()
		return 0
}
```

  

```c
DO NOT CONFORM
class Try{
		void output()
}
void Try::output(){
		print("Hello")
}

int main()
{
		Try myObj
    myObj.output()
		return 0
}
```

```cpp
   class Try{
		void output(){
				 print("Hello")
		}
		}
		
		int main()
		{
				Try myObj
		    output()    #Error: have to refer to object created to access a method of that class
				return 0
		}
```

```cpp
class Try{
		void .output(){    
				 print("Hello")
		}
}

int main()
{
		Try myObj
    myObj.output()  #Error: as the method has been declared as private we cannot access it
		return 0
}
```

```cpp
class Try{
		void output(int a){    
				 print("Hello ",a)
		}
}

int main()
{
		Try myObj
    myObj.output(10)  
		return 0
}
```

```c
class  Aeroplane{
		int max_speed
    string model
    Aeroplane(int speed, string y){   #constructor may or may not have input
				max_speed=speed
				model=y
		}	
}

```

```cpp
class  Aeroplane{
		int max_speed
    string model
    Assign(int speed, string y){   #Error:the constructor's name should be that of the class
				max_speed=speed
				model=y
		}	
}
```

## Inheritance

```cpp
class Parent{
		int parent_id
}
class Child inherits Parent{            #here the mode of access from the parent //class is public by default
		int child_id
}

int main(){
	Child object
	object.parent_id=0
	object.child_id=1
	print("Child id="+ object.child_id + "Parent id=" + object.parent_id)
}
```

```cpp
class Vehicle{
	string type
}
class No_of_wheels{
	int wheels
}
class Car inherits Vehicle,No_of_wheels{          #multilevel inheritance is also permitted
	int model_no
}
```

## Encapsulation

```cpp
CONFORM
class Encapsulation 
{  
        
        int .x   #here x is private
          
        void set(int a)    #the functions is called by the object to change the private variable
        { 
	            x = a 
        } 
          
        int get()  #function returns the value of the private variable
        { 
            return x
        } 
}

int main(){
	Encapsulation test
	test.set(10)
	print(test.get())
}
```

```cpp
DO NOT CONFORM
class Encapsulation 
{  
        
        int .x   #here x is private
          
        void set(int a)    #the functions is called by the object to change the private variable
        { 
	            x = a 
        } 
          
        int get()  #function returns the value of the private variable
        { 
            return x
        } 
}

int main(){
	Encapsulation test
	test.x=5     #error as we can't initialize or modify a private variable
	print(test.get())
}
```

## Polymorphism

```cpp
# static overloading
class Polymorphism{
	int sum(int a,int b){
		return a+b
	}
}
class morpher inherits Polymorphism{
	int sum(float a,float b){
		return a+b
	}
}
int main(){
	morpher test
	int result1,result2
	result2=test.sum(1.1,2.2)
	print(result2)        #prints 3.3  
```

### ************************Function Overloading

```cpp
int  repeat(int a)        #the return types may be different
int  repeat(int a,int b)
```

```cpp
int sum(int a, int b)
float sum(float a, float b)
```

```cpp
bool compare(int a, float b)
bool compare(float a, int b)
```

```cpp
void create(int a, int b)
int create(int a, int b)  #declaring two functions with same name and parameters but different return types doesn't lead to function overloading

```