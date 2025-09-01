# Ex.No:3  
# Ex.Name: Write a C++ program to do integer arithmetic operation using muliple inheritance( + and - operation in one class,* and / in another class).

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

class ArithmeticAddSub {
protected:
    int a, b;
public:
    void setValues(int x, int y) {
        a = x;
        b = y;
    }

    void addition() {
        cout << "The Result of the Addition is:" << (a + b) << endl;
    }

    void subtraction() {
        cout << "The Result of the Subtraction is:" << (a - b) << endl;
    }
};

class ArithmeticMulDiv : public ArithmeticAddSub {
public:
    void multiplication() {
        cout << "The Result of the Multiplication is:" << (a * b) << endl;
    }

    void division() {
        if (b != 0) {
            cout << "The Result of the Division is:" << (a / b) << endl;
        } else {
            cout << "Division by zero is not allowed." << endl;
        }
    }

    void modulo() {
        if (b != 0) {
            cout << "The Result of the Modulo is:" << (a % b) << endl;
        } else {
            cout << "Modulo by zero is not allowed." << endl;
        }
    }
};

int main() {
    int x, y;
    cin >> x >> y;

    ArithmeticMulDiv obj;
    obj.setValues(x, y);
    obj.addition();
    obj.subtraction();
    obj.multiplication();
    obj.division();
    obj.modulo();

    return 0;
}

```

## Output:
<img width="681" height="679" alt="image" src="https://github.com/user-attachments/assets/9fa460e5-a992-4e29-8f22-99ef24cd8fa5" />

## Result:
```
Input: 45 50

Output:
The Result of the Addition is:95
The Result of the Subtraction is:-5
The Result of the Multiplication is:2250
The Result of the Division is:0
The Result of the Modulo is:45
```
