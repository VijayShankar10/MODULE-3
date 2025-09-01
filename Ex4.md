# Ex.No:4  
# Ex.Name: Write a C++ program to find the circumference of a circle using simple inheritance.  
(Give private access of a base class to derived class. Calculate the circumference value using a member function of base class and display the result using a member function of derived class.)  

## Date:  

## Aim:  
To write a C++ program using simple inheritance, where the base class stores the radius of a circle and the derived class calculates and displays the circumference.  

## Algorithm:  
1. Start the program.  
2. Define a base class `Circle` with a **private** data member `radius`.  
3. Provide a setter function `setRadius()` in the base class to assign the radius.  
4. Provide a getter function `getRadius()` in the base class to retrieve the value of radius.  
5. Derive a class `Circumference` from `Circle`.  
6. In the derived class, define a function to calculate circumference as:  2*3.14*radius (accessing `radius` via `getRadius()`).  
7. Display the circumference from the derived class.  
8. In `main()`, read the radius from the user, set its value, and call the display method.  
9. Stop the program.  

## Program:  
```cpp
#include<iostream>
using namespace std;
class Child
{
    public: 
    int r;
    void circumference()    
    {
        cin>>r;
    }
};
class Base:public Child
{
    public:
    int r;
    void circumference()
    {
        cin>>r;
        cout<<"Circumference of a circle is : "<<3.14*2*r<<endl;
    }
};
int main()
{
    Base s;
    s.circumference();
    s.Child::circumference();
    return 0;
}
```

## Output:
<img width="853" height="366" alt="image" src="https://github.com/user-attachments/assets/ffd6240d-7dc8-4bdd-82aa-ee8a3d0113bb" />

## Result:
```
Input:
10

Output:
Circumference of a circle is : 62.8
```
