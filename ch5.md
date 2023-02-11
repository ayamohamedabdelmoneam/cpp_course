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
## Increment And Decrement Operators
  - "For incrementing And Decrementing Values"
     - Pre/Post Increment
     - Pre/Post Decrement
  ##  Example 3 :
````c++
#include <iostream>
using namespace std;

int main()
{
  int likes = 0;
  cout << likes-- << "\n"; // 0
  cout << likes << "\n";   // -1

  int views = 0;
  cout << --views << "\n"; // -1
  cout << views << "\n";   // -1
  return 0;
}
````
## comparison operators or Relational operators:
- used to compare values 
- you can use it in such have a program that restricted to the age of users must be greater than 18 year.
   -  `==` Equal
   - `!=` Not Equal
   - `>` Greater Than
   - `<`Less Than
   - `>=` Greater Than Or Equal
   - `<=` Less Than Or Equal
## Example 4:
````c++
#include <iostream>
using namespace std;
int main () {
    cout << (10 == 10) << "\n"; // =1 = true
    cout << (1000 == 200) << "\n"; // = false
    cout << (1000 != 200) << "\n"; // True
    cout << (10 != 10) << "\n";    // 0 => False
    cout << (40 > 18) << "\n"; // True
    cout << (20 < 30 ) << "\n"; // True
    cout << (18 > 18) << "\n"; // 0 => False
    cout << (40 >= 18) << "\n"; // 1 => True
    cout << (18 >= 18) << "\n"; // 1 => True
    return 0;
}
````
## Logical Operators
  - "For Logic Between Values"
       - `&&` And Must two condition get true
       - `||` Or
       - `!` Not
## Example 5 :
````c++
#include <iostream>
using namespace std;
int main () {
    int age;
    int points;
    cout << "please enter your age \n";
    cin >> age ;
    cout << "please enter your Points \n";
    cin >> points;
    cout << (age>= 18 && points>= 500) << endl;
    cout << (age>= 18 || points>= 500) << endl; // one of them get true
    cout << (10 == 10) << endl;   // 1 => True
    cout << !(10 == 10) << endl;  // 0 => False
    cout << !(100 == 10) << endl; // 1 => True

````
## Operators Precedence 
  - "Which One Has Higher Precedence"
- Refernce
  - Operators Precedence Table
- Search
    - Bitwise Operators 
    - Spaceship Operator
- Training
    - Try Operators Yourself Before Browsing References
## Example:
````c++
#include <iostream>
using namespace std;

int main()
{
  cout << 10 + 5 * 5 << "\n";
  // 5 * 5 = 25
  // 10 + 25 = 35
  cout << 10 - 5 * 5 << "\n";
  // 5 * 5 = 25
  // 10 - 25 = -15
  cout << 20 / 5 * 4 << "\n";
  // 20 / 5 = 4
  // 4 * 4 = 16
  cout << 10 + 20 / 5 * 4 << "\n";
  // 10 + 16 = 26
  // 20 / 5 = 4
  // 4 * 4 = 16
  cout << (10 + 5) * 5 << "\n"; // (15) * 5 = 75
  return 0;
}
````
<hr>

## Control Flow :
- if Condition .
- syntax:
  - if(condition get true) { // Do Something }
## Example:
````c++
#include <iostream>
using namespace std;
int main() {
    int age;
    cout << "please Enter Your Age\n";
    cin >> age;
    if (age < 18 ) {
        cout << "This Program Is Not Suitable For You \n";
    }
    cout << "Hello\n";

    main ();
}

````
<hr>

## Control Flow
- If ... else if ... else

- Syntax
- if (Condition Is True)
{
// Do Something
}
## Example 
````c++
#include <iostream>
using namespace std;
int  main() {
    int age,
    points,
    rank;
    cout<< "Please Enter Your Age\n";
    cin >> age;
    cout<< "Please Enter Your Points\n";
    cin >> points;
    cout << "please Enter Your rank\n";
    cin >> rank;
    if (age >= 18) {
        cout << "Your Age Is Ok\n";
    } else if (points > 500) {
        cout << "Your Points Is Ok\n";

    }else if (rank > 5) {
        cout << "Your Rank Is Ok\n";

    } else {
        cout << "Iam Sorry\n";
    }
    main();
}
````
##  Nested If Conditions:
## Example:
````c++
#include <iostream>
using namespace std;

int main()
{
  int age = 25;
  int points = 1500;

  if (age >= 18)
  {
    cout << "Welcome Your Age Is OK\n";
    if (points >= 1000)
    {
      cout << "You Are VIP\n";
    }
  }

  return 0;
}
````
## Ternary Operator
- Syntax
   - (Condition) ? True : False;
  ## Example:
````c++
#include <iostream>
using namespace std;

int main()
{
  int age = 15;

  if (age >= 18)
  {
    cout << "Your Age Is OK\n";
  }
  else
  {
    cout << "Your Age Is Not OK\n";
  }

  cout << (age >= 18 ? "Age Is OK\n" : "Age Is Not OK\n");

  string msg = age >= 18 ? "Age Is OK\n" : "Age Is Not OK\n";

  cout << msg;

  return 0;
}
````
<hr>

## Nested Ternary Operator
- Syntax:
   - (Condition Is True) ? True : False;
## Example:
````c++
#include <iostream>
using namespace std;

int main()
{
  int age = 15;
  int points = 450;

  if (age >= 18)
  {
    cout << "OK\n";
  }
  else
  {
    if (points >= 500)
    {
      cout << "OK Because Of Points\n";
    }
    else
    {
      cout << "No Age Or Points\n";
    }
  }

  cout << (age >= 18 ? "OK\n" : (points >= 500 ? "OK P\n" : "No P\n"));

  cout << (points >= 500 ? "OK P\n" : "No P\n");

  if (age >= 18)
    cout << "OK\n";
  else
    cout << "Not OK\n";

  return 0;
}
````
#  If Condition Trainings:
## App 1:
- Even / Odd Checker:
````c++
#include <iostream>
using namespace std;
int  main() {
    int num;
    cout << "Please Enter Number\n";
    cin >> num;
    if (num %2 == 0) {
        cout<< "This Number is Even\n";
    }else
    {
        cout << " This Number Is Odd\n";
    }
    main();
} 
````
<hr>

## App2:
- Find Greatest Number:
````c++
#include <iostream>
using namespace std;
int  main() {
    int a,b,c;
    cin >> a >> b >> c;
    if (a > b && a > c)
    {
        cout << a << " Is The Greatest Number\n";
    }
    else if (b > a && b > c)
    {
        cout << b << " Is The Greatest Number\n";
    }
    else
    {
        cout << c << " Is The Greatest Number\n";
    }
main();
}
````
<hr>

## App3:
- User Rank Checker:
````c++
#include <iostream>
using namespace std;
int main () {
    int points;
    cin >> points;
    if (points > 0 && points <= 500 ){
        cout << "Not Bad\n";
    }else if (points > 500 && points <= 1000){
        cout << "The points Is Very Good\n";
    }else{
        cout << " VIP\n";
    }
    return 0;
} 
````
<hr>

## App4:
- Simple Calculator:
````c++
#include <iostream>
using namespace std;
int main () {
    int num1, num2, operation;
    cout << "Add Number One\n";
    cin >> num1;
    cout << "Add Number Two\n";
    cin >> num2;
    cout << "Add Type Of Operation\n";
    cin >> operation;
    if (operation == 1) {
        cout << " you Request sum of two Number" << num1 + num2 << "\n";
    }else if (operation == 2) {
        cout << num1 - num2 << "\n";
    }else if (operation == 3) {
        cout << num1 * num2 << "\n";
    }else if (operation == 4) {
        cout << num1 / num2 << "\n";
    }else{
        cout << "Operation Is Not Valid\n";
    }
    return 0;
} 

````
