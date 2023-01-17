# Lecture 4 
## Variables:
- Is a data container With unique name `Identifiers`.
- Declare with value 
## Syntax:
- (Data-Type), (Variable_Name) = (Value of Variable)
- Must write variable name friendly related to thing you would store it .
`
````c++
#include <iostream>
int main () {
    // Variable syntax Make Declare The Variable
    int product_price = 100;

    std::cout << "price is" << product_price <<"\n";
    std::cout << "price is" << product_price + 50 <<"\n";
    std::cout << "price is" << product_price +100 << "\n";
    // Make update Variable
    product_price = 150;
    std::cout << "The New Price Is" << product_price;
return 0;
}

````
## What is Variable Naming Rules & Best Practice ?
 ### Naming Rules:
- 1- Must be Unique don't Repeat it.
- 2- Case Sensitive.
- 3-cannot start with numbers.
- 4- Nums Or Letters Or Underscore.
- 5- No White Space Or Special Characters like `#`, `@`.
- 6-Reserved Keywords `Class`, `Public`.
````c++
#include <iostream>
int main () {
    // Declare variable 
    int price = 100;
    price = 200; // Update Value 
    // cant start with number
    int 2num =300; //error
    //can be but anywhere but not at start
    int num2 = 300;
    
    return 0;
}
````
## Best Practices: we have writing coding style
- 1-Related Names : you should choose var describe the data you will store it .
- 2-Writing Style `camelCase`
## Why there a different between naming rules and best Practices?
- Because naming is rules must follow it to not make an error.
- but best practices don't make any error.


## Variables Advanced Knowledge :
- Declare Variable Without Value + Change Later.
- Declare Multiple Variables Without Value + Change Later.
- Declare Multiple Variables With Same Value.

```` c++
#include <iostream>
int main () {
// Declare With out value 
int d;
d= 100;
std::cout << d; //100
std::cout << "\n=====================\n";
// Declare Multiple var 
int a, b, c;
a= 10, b= 20, c= 30;
 std::cout << a + b + c;  // 60 
 std::cout << "\n=====================\n";
 // Declare var with same value.
 int v, e, r;
 v = e = r = 10;
 std::cout << v + e + r; //30
return 0;
}
````
## Variables Scope: 
- 1-Global Variable : any one can access this var 
- 2-Local Variable

````c++
#include <iostream>
using namespace std;

int a = 100; // Global Variable

int second()
{
  int b = 200; // Local Variable
  cout << a << " Coming From Second Function\n";
  cout << b << " Coming From Second Function\n";
  return 0;
}

int main()
{
  cout << a << " Coming From Main Function\n";
  // cout << b << " Coming From Main Function\n"; // Undefined
  second();
  return 0;
}
````
## Constant Variable:
- Read Only Value
- Can't Declare Without Value
````c++
#include <iostream>
using namespace std;
int main () {
    const int x = 100; //read only you can't update or change value.

return 0;

}

````
## Example 2:
````c++
#include <iostream>
using namespace std;
#define DAYS 9 // preprocessor will not like to be used prefer use const 

int main()
{
  const int day = 8;
  // int salary = 15000;
  const int num = 100;
  // num = 200;
  cout << num;
  // const int x;
  cout << "\n" << DAYS;
  return 0;
}
````
## Example3 : Calculate Your Age Application
````c++
#include <iostream>
using  namespace  std;
int  main() {
    int age;
    cin >> age;
    cout << age << "\n";
    int age_in_days = age * 365;
    int age_in_hours = age_in_days * 24;
    int age_in_min = age_in_hours * 60;
    int age_in_sec = age_in_min * 60;


    cout << "Age in days is :" << age_in_days << "Days\n";
    cout << "Age in hours is :" << age_in_hours << "Hours\n";
    cout << "Age in min is :" << age_in_min << "MIN\n";
    cout << "Age in sec is :" << age_in_sec << "SEc\n";

    return 0;
}

````
## Example4 : calculate the sum of two nums 
````c++
#include  <iostream>
using namespace  std;
int main() {
    int  num1;
    int num2;
    int sum ;
    cout << "Please Enter Your First Integer Number\n";
    cin >> num1;
    cout <<  "please Enter Your Second Integer Number\n";
    cin >> num2;
    sum = num1 + num2;
    cout << "The Summation Of Two Number is : "<< sum;
    return 0;
}

````