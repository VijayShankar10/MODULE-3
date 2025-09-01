# Ex.No:1
# Ex.Name: Write a C++ program to swap two characters using class methods (methods defined outside class).
## Date:
## Aim:
To swap two characters using class methods defined outside the class.

## Algorithm:
1.Start the program.
2.Define a class with two character variables.
3.Define member functions to read input and swap characters (outside the class).
4.Display the swapped characters.
5.Stop.

## Program:
```cpp
#include <iostream>
using namespace std;

class Swap {
    char a, b;
public:
    void read();
    void swapChars();
};

void Swap::read() {
    cin >> a >> b;
}

void Swap::swapChars() {
    cout << "After swapping the 1st character is:" << b << endl;
    cout << "After swapping the 2nd character is:" << a << endl;
}

int main() {
    Swap s;
    s.read();
    s.swapChars();
    return 0;
}
```


## Output:
<img width="856" height="450" alt="image" src="https://github.com/user-attachments/assets/cc4ed02b-f1a9-44b8-bb09-e711d1c88531" />

## Result:
```
Input: a z
After swapping the 1st character is:z
After swapping the 2nd character is:a
```
