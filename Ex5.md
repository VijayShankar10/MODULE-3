# Ex.No:5  
# Ex.Name: Write a C++ program to add the two numbers using inheritance.  
(Declare two input variable as protected in base class and read one value in one derived class and read another value in its derived class and do the addition operation in its derived class.)  

## Date:  

## Aim:  
To write a C++ program using multilevel inheritance, where the base class stores two numbers, the first derived class reads the first number, the second derived class reads the second number, and performs the addition operation.  

## Algorithm:  
1. Start the program.  
2. Define a base class with **protected** data members `a` and `b`.  
3. Define class `First` derived from base class to read the first number.  
4. Define class `Second` derived from `First` to read the second number.  
5. In `Second`, define a function to calculate and display the sum of the two numbers.  
6. In `main()`, read two numbers from the user.  
7. Pass the values into respective derived classes.  
8. Perform addition and display the result.  
9. Stop the program.  

## Program:  
```cpp
#include <iostream>
using namespace std;
class Base {
      protected:
      int a,b;
};
class derived:public Base{
    public:
    void get(){
        cin>>a>>b;
    }
    void print(){
        cout<<"The Result is:"<<a+b;
    }
    
};
int main(){
    derived d;
    d.get();
    d.print();
    return 0;
}
```

## Output:
<img width="868" height="362" alt="image" src="https://github.com/user-attachments/assets/e21af922-043b-4f69-998e-659839b4879c" />

## Result:
```
Input:
10 20

Output:
The Result is:30
```
