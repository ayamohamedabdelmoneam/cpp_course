# Operators & Operands :
  -  "Symbols To Operate On Data"
        ## Arithmetic Operators
  - "For Mathematical Operations"
    -  `+` => Addition
    -  `-` => Subtraction
    -  `*` => Multiplication
    -  `/` => Division
    -  `%` => Modulo => Remainder After Division
      ## What Is Operand ?
  - The Part Of an Instruction Representing The Data Manipulated by The Operator.
## Example 1: 
````c++
#include <iostream>
using  namespace std;
int main () {
    cout << 10 + 10 << "\n"; // 20
    cout << sizeof(10 + 10) << "\n"; // 4 Bytes
    cout << 10.5f + 9.5f << "\n"; // return data type float = 20
    cout << sizeof(10.5f + 9.5f) << "\n"; // 4bytes
    cout << int(10.5 + 9.5) << "\n"; // If i need to return value in int = 20
    cout << sizeof(10.5 + 9.5) << "\n";      //  8 Double Data type
    cout << sizeof(int(10.5 + 9.5)) << "\n"; // 4 int data Type
    cout << 100 - 50 << "\n"; // = 50
    cout << 100 - -50 << "\n"; // =150

    cout << 10 * 5 << "\n"; // 50

    cout << 20 / 5 << "\n"; // 4
    cout << 12 / 5 << "\n"; // int / int = int = 2 not float
    cout << 12.f / 5 << "\n"; // float / int = float = 2.4

    cout << 20 % 5 << "\n"; // 0
    cout << 21 % 5 << "\n"; // 1
    cout << 24 % 5 << "\n"; // 4
    // cout << 24.5 % 5 << "\n"; // Problem
    return 0;
}
````
   ##  Assignment Operators:
  - "For Assigning Operations"
    - `=` Assign
    - `+=`Addition
    - `-=` Subtraction
    - `*=` Multiplication
    - `/=` Division
    - `%=` Modulo => Remainder After Division
## Example 2 :
````c++
#include <iostream>
using  namespace std;
int main () {
    int a = 10;
    a += 10; // a = 10 + 10 = 20  , a= a+10 = 20
    cout << a << "\n"; // 20
    int b = 20;
    b -= 10 ; // b = b -10 = 10, 20-10=10
    cout << b << "\n";
    int c = 5;
    c *= 10; // c = c * 10 = 50 , 5* 10 = 50
    cout << c << "\n";
    return 0;
}

````