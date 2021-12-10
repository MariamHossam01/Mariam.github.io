# CMP2241_Task 3 --> Const and & Report


## A) Usage of _const_ keyword

### 1- Constant Variables 

To make a variable constant. The variable need to be initialized.

If you make any variable as constant, using const keyword, you cannot change its value.

```
const int x = 1;
```
### 2- Pointers 

To point to a const variable. 

```
const int* l;
int const* l; // same meaning
```
or to have a constant address but variable data.  
```
int x = 1;
int* const w = &x; 
```
### 3-  const Function Arguments and Return types\

We can make the return type or arguments of a function as const. so we cannot change any of them.

```
void f(const int i) // const argument
{
   ...
}

const int g() //const return
{
    return 1;
}
```
### 4- Defining Class Data members as const

To define data variables as constants without initializing them. 
They would be initialized during constructor calling.     
```
class con
{
const int i;
public:
con(int x):i(x)
{
cout << i;
}
};

int main()
{
con t(10);
con x(20);
}
O/P:1020
```
### 5- Defining Class Object as const
To define an object such that it's data can never change.

### 6-  Defining Class's Member function as const

```
return_type function_name() const;
```


## B) Usage of _&_ operator

### 1- declaring a reference to a type
When used in the left-hand side of the variable declaration,a reference of the declared variable is expected. 

```
int  z=9;
int& x = z; // both  variables point to the same address and therfor value
```

### 2- To get the address of a variable

When used in the right-hand side of the variable declaration,it can be used in variable assignments
it's useful in pointers as when it's used it will return the address instead of the value. 

```
int z=9;
int* x;
x = &z; // x is a pointer that points to z
```
### 3- bitwise operator


It is the bitwise AND.Which means it takes 2 numbers as inputs and do AND
operation on each bit.


|       | 8       | 4     | 2      |0      |
|-------|--------|-------|--------|--------|
| 10    |      1 |      0|       1|       0|
| 3     |      0 |      0|       1|       1|
|10&3= 2|      0 |      0|       1|       0|

```
cout<<(10&3); // O/P: 2
```
### 4- logical expression

Used as the AND operator when used as double ampersands **'&&'**. 

### 5- declaring rvalue references

rvalue are values which are not saved in the memory unlike the lvalues
```
string l = "hello" // l is a lvalue whereas "hello" is a rvalue  
```
### 6- declaring universal references

### 7- function overloading
