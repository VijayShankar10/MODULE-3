# Ex.No:3  
# Ex.Name: Write a C++ program to get two numbers from two base classes and display the income after the payment of tax in the derived class.  
(Illustrate Multiple Inheritance and use appropriate access specifier)  

## Date:  

## Aim:  
To write a C++ program using multiple inheritance, where one base class provides salary, another base class provides tax amount, and the derived class computes net income after the payment of tax.  

## Algorithm:  
1. Start the program.  
2. Define a base class `Salary` with a protected data member for salary and a function to get salary input.  
3. Define another base class `Tax` with a protected data member for tax and a function to get tax input.  
4. Define a derived class `Employee` which inherits **from both `Salary` and `Tax`**.  
5. In the derived class, define a member function to calculate income as:  income = salary - tax
6. Display the net income.  
7. In the `main()` function:  
- Read salary and tax from the user  
- Call base class input functions  
- Call the derived class function to compute and display income.  
8. Stop the program.  

## Program:
```cpp
#include <iostream>
using namespace std;
class getData
{
    public:
    void
}
```
## Output:
```
Input:
275000
12500

Output:
Income after the payment of Tax : 262500
```
##Result:
<img width="853" height="342" alt="image" src="https://github.com/user-attachments/assets/b8c31cac-a58b-4195-9f7f-d6ef44e6cf3c" />

