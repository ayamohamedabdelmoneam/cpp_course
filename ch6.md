# Arrays
## What Is Array ?
- Collection Of Elements Of The Same Type
- Placed in Contiguous Memory Locations
- Referenced By Index Started From 0
<hr>

## Why We Need Array ?
- Creating Array Syntax
- Check Array Size
- Create Array Without Size

## Example On Array Syntax :
````c++
#include <iostream>
using namespace std;

int main()
{
  int nums[4] = {100, 200, 300, 400}; // c- style array
  cout << sizeof(int) << "\n";  // 4 Bytes
  cout << sizeof(nums) << "\n"; // 16 Bytes

  double dos[4] = {100, 200, 300, 400};
  cout << sizeof(double) << "\n"; // 8 Bytes
  cout << sizeof(dos) << "\n";    // 32 Bytes

  int rands[]{100, 5000, 950};
  return 0;
}
````
- How To Access Array Elements ?
- How To Get Memory Location Of Element ? 
## Example:
````c++
#include <iostream>
using namespace std;
int main() {
    int nums[] {100, 200, 300};
    cout << "First Element:" << nums[0] << "\n"; // Access The First Element
    cout << "last Element:" << nums[2] << "\n"; // last = numbers of element - 1
    cout << "Location:" << &nums[0] << "\n"; // location of first element
    cout << "Location:" << &nums[1] << "\n"; // location of second element
    cout << "Location:" << &nums[2] << "\n"; // location of Last element
    return 0;

}
````

- How To Declare Empty Array?
- How Add Element to array or Update Values?
- How To Get  Length Of Array Using Size Of ?
````c++
#include <iostream>
using namespace std;
int main() {
    int nums[4];
    // To Add Element Or Update Values
   nums[0] = 100;
   nums[1] = 200;
   nums[2] = 300;
   nums[3] = 400;
   cout << "Element 1: " << nums[0] << "\n";
    cout << "Element 2: " << nums[1] << "\n";
    cout << "Element 3: " << nums[2] << "\n";
    cout << "Element 4: " << nums[3] << "\n";
   // Make Update To any Value
   nums[0] = 1000;
    cout << "Element 1: " << nums[0] << "\n";
   // To get length of array
    cout << sizeof (nums) / sizeof(nums[0]); //  16 / 4 = 4 elements
    return 0;

} 
````
- Two Dimensional Arrays AKA [2D Array]:
## Example:
````c++
#include <iostream>
using namespace std;

int main()
{
  int points_a[3] = {1, 2, 3};
  int points_b[3] = {4, 5, 6};
  int points_c[3] = {7, 8, 9};

  // Good Practice

  const int rows = 3;
  const int columns = 3;
  int points[rows][columns] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
  cout << points[1][2] << "\n"; // 6
  cout << points[2][0] << "\n"; // 7
  cout << points[2][2] << "\n"; // 9

  // Bad Practice
  // int points[3][3] = {1, 2, 3, 4, 5, 6, 7, 8, 9};
  // cout << points[1][2] << "\n"; // 6
  // cout << points[2][0] << "\n"; // 7
  // cout << points[2][2] << "\n"; // 9

  return 0;
}

````
<hr>

## Arrays:
- Array Class
- Test Methods
- Syntax:
    - Template<Type, Size> Identifier;
## Example:
````c++
#include <array>
#include <iostream>
using namespace std;

int main()
{
    array<int, 4> points = {1, 2, 3, 4};
    cout << points[0] <<"\n"; //1
    cout << points[1] <<"\n"; // 2
    cout << points[2] <<"\n"; //3
    cout << points[3] <<"\n"; //4
     // function of elements counts points.size = 4
    cout << "Elements Count Is:" << points.size() << "\n";
     points.fill(10); // go inside array then fill array with this element
    cout << points[0] <<"\n"; // 10
    cout << points[1] <<"\n"; // 10
    cout << points[2] <<"\n"; // 10
    cout << points[3] <<"\n"; // 10
    points.fill('A'); // go inside array then fill array with this element will put Ascii Value
    cout << points[0] <<"\n"; // 65
    cout << points[1] <<"\n"; // 65
    cout << points[2] <<"\n"; // 65
    cout << points[3] <<"\n"; // 65
    points.fill(true); // put 1 the value of boolean
    cout << points[0] <<"\n"; // 1
    cout << points[1] <<"\n"; // 1
    cout << points[2] <<"\n"; // 1
    cout << points[3] <<"\n"; // 1
   points.fill(false);
   cout << points[0] << "\n";
   cout << points[1] << "\n";
   cout << points[2] << "\n";
   cout << points[3] << "\n";
    return 0;
}
````
<hr>

## Array Methods:
- at.
- front.
- back.
- fill.
- size.
- empty.
## Example:
````c++
#include <array>
#include <iostream>
using namespace std;

int main()
{
   array<int, 4> nums = {100, 200, 300, 400};
   cout << nums[0] << "\n"; // 100
   cout << nums.front() <<"\n"; // 100
    cout << nums[3] << "\n"; // 400
    cout << nums.back() << "\n"; // 400
    cout << nums.at(1) << "\n";   // 200
    cout << nums.size() << "\n";  // 4
    cout << nums.empty() << "\n"; // 0 => False

    return 0;
}
````
<hr>

## Array Training :
- Guess The Number From Sequences Game.
````c++
#include <array>
#include <iostream>
using namespace std;

int main()
{
    int points = 0;
    int answers[3];
    cout << "Type The Missing Number In Sequences:\n";

    cout << "Sequence 1\n";
    cout << "1 | 5 | 10 | 16 | ?? \n";
    cin >> answers[0];
    cout << "Sequence 2\n";
    cout << "2 | 4 | 8 | 16 | ?? \n";
    cin >> answers[1];

    cout << "Sequence 3\n";
    cout << "1 | 1 | 2 | 3 | ?? \n";
    cin >> answers[2];
int seq[3][5] = {
        {1, 5, 10, 16, 23},
        {2, 4, 8, 16, 32},
        {1, 1, 2, 3, 5}
};
    if (answers[0] == seq[0][4] ) {
      points++;
    }
    if (answers[1] == seq[1][4]){
        points++;
    }
    if (answers[2] == seq[2][4]){
        points++;
    }
    cout << "Your Points Is: "<< points <<"From 3\n";

    return 0;
}
````
