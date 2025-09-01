# Ex.No:2  
# Ex.Name: Write a C++ program to calculate the electricity bill using multilevel inheritance.  
## Date:  

## Aim:  
To calculate the electricity bill using the concept of multilevel inheritance in C++.  

## Algorithm:  
1. Start the program.  
2. Define a base class `Customer` with customer details.  
3. Define a derived class `Consumption` to get the number of units consumed.  
4. Define another derived class `Bill` to calculate the bill amount using the formula.  
5. Display the customer details and the total bill amount.  
6. Stop the program.  

## Program:  
```cpp
#include <iostream>
using namespace std;

class Customer {
protected:
    string name;
    int id;
public:
    void readCustomer() {
        cin >> id >> name;
    }
};

class Consumption : public Customer {
protected:
    int units;
public:
    void readUnits() {
        cin >> units;
    }
};

class Bill : public Consumption {
    double amount;
public:
    void calculateBill() {
        if (units <= 100)
            amount = units * 1.20;
        else if (units <= 200)
            amount = (100 * 1.20) + (units - 100) * 2.00;
        else
            amount = (100 * 1.20) + (100 * 2.00) + (units - 200) * 3.00;
    }
    void displayBill() {
        cout << "Customer ID: " << id << endl;
        cout << "Customer Name: " << name << endl;
        cout << "Units Consumed: " << units << endl;
        cout << "Total Bill: " << amount << endl;
    }
};

int main() {
    Bill b;
    b.readCustomer();
    b.readUnits();
    b.calculateBill();
    b.displayBill();
    return 0;
}
```

## Output:
<img width="839" height="540" alt="image" src="https://github.com/user-attachments/assets/210c6d8a-00a6-4475-bad7-edc111121eab" />

## Result:
```
Input:  
1 ila 500 300

Output:  
service number:1
service name:ila
unit consumption:200
amount:500

```
