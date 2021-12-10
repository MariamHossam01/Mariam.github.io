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