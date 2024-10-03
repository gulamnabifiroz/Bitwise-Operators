# Bitwise-Operators
This repository contains examples and explanations of bit manipulation and various bitwise operations implemented in C++. It is designed to help users understand and perform efficient low-level operations on binary data.
<br>
<br>
<p align="center">Experiment 4</p>
<br>

## Aim
To study various types of bitwise operations

## Software Used
- Dev C++

## Theory
Bitwise Operators are the operators that are used to perform operations on the bit level of the integers. While performing this operation integers are considered as sequences of binary digits. In C++, we have various types of Bitwise Operators.
<br>
<br>
### Types Of Bitwise Operators

1)Bitwise AND  (&):- The & (bitwise AND) in C++ takes two numbers as operands and does AND on every bit of two numbers. The result of AND is 1 only if both bits are 1.  
<br>
2)Bitwise OR  (|):- The | (bitwise OR) in C++ takes two numbers as operands and does OR on every bit of two numbers. The result of OR is 1 if any of the two bits is 1. 
<br>
<br>
3)Bitwise XOR  (^):- The ^ (bitwise XOR) in C++ takes two numbers as operands and does XOR on every bit of two numbers. The result of XOR is 1 if the two bits are different.
<br>
<br>
4)Bitwise NOT  (~):- The ~ (bitwise NOT) in C takes one number and inverts all bits of it.
<br>
<br>
5)Left Shift  (<<):- The << (left shift) in C takes two numbers, the left shifts the bits of the first operand, and the second operand decides the number of places to shift.
<br>
<br>
6)Right Shift  (>>): - The >> (right shift) in C takes two numbers, right shifts the bits of the first operand, and the second operand decides the number of places to shift. 
<br>
<br>

## Algorithm

Step 1: Start
<br>
Step 2: Declare Variables a and b
<br>
Step 3: Input a and b from the user
<br>
Step 4: Display Bitwise And of a and b (a&b)
<br>
Step 5: Display Bitwise Or of a and b (a|b)
<br>
Step 6: Display Bitwise XOR of a and b (a^b)
<br>
Step 7: Display Bitwise Not of a (~a)
<br>
Step 8: Display Bitwise Not of b (~b)
<br>
Step 9: Display Left Shift by 1 of a (a<<1)
<br>
Step 10: Display Right Shift by 1 of a (a>>1)
<br>
Step 11:End
<br>

## Code

```cpp
//Gulamnabi Khan
// 23070123503
//E&TC A3
#include <iostream>
using namespace std;
int main() {
    int a, b;
    cout << "Pls Enter A Number In Decimal: ";
    cin >> a;
    cout << "Pls Enter Another Number In Decimal: ";
    cin >> b;
    int binary_a = a;
    int binary_b = b;
    cout << "Bitwise AND: " << (binary_a & binary_b) << endl;
    cout << "Bitwise OR: " << (binary_a | binary_b) << endl;
    cout << "Bitwise Xor: " << (binary_a ^ binary_b) << endl;
    cout << "Bitwise Not of A: " << (~binary_a) << endl;
    cout << "Bitwise Not of B: " << (~binary_b) << endl;
    cout << "Left Shift of A: " << (binary_a << 1) << endl;
    cout << "Right Shift of A: " << (binary_a >> 1) << endl;
    return 0;
}
```

## Output

![image](https://github.com/user-attachments/assets/7119beca-7781-4b73-9b73-e081cb33320d)


## Conclusion

Thus, we have learned the different bitwise operations.


<br>
<br>
<p align="center">Experiment 4b</p>
<br>

## Aim
To set and reset bit in binary 

## Software Used
- Dev C++

## Theory
<p>Bit manipulation is a crucial programming technique involving direct operations on the bits of a binary number. This method is often used for performance optimization and efficient data handling.</p>
<p> This program utilizes two primary bitwise operations: OR and AND, to manipulate specific bits in the number. The program uses the bitwise OR operation to set a particular bit (change it to 1). It shifts the number 1 to the left by the position of the bit we want to change, creating a number with a 1 only at that position. The OR operation combines this number with the original number, changing the specified bit to 1 while keeping all other bits the same. The program uses the bitwise AND operation to reset a specific bit (change it to 0).It first creates a number with a 1 at the bit position to be reset, then flips all bits to make a number with 0 at that position and 1s elsewhere. The AND operation combines this with the original number, turning the specified bit to 0 while leaving other bits unchanged.</p>

## Algorithm

Step 1: Start
<br>
Step 2: Declare variables number, bitToSet, bitToReset, resultSet, and resultReset.
<br>
Step 3: Input a decimal number and store it in a number.
<br>
Step 4: Input the bit position to be set and store it in bitToSet.
<br>
Step 5: Input the bit position to be reset and store it in bitToReset
<br>
Step 6: Calculate resultSet by setting the specified bit in the number using the expression number | (1 << bitToSet)
<br>
Step 7: Calculate resultReset by resetting the specified bit in the number using the expression number & (~(1 << bitToReset))
<br>
Step 8: Display the original number
<br>
Step 9: Display the number after setting the specified bit (resultSet)
<br>
Step 10: Display the number after resetting the specified bit (resultReset)
<br>
Step 11: End
<br>

## Code

```cpp
//Gulamnabi Khan
// 23070123503
//ENTC A3
#include <iostream>
using namespace std;

int main() {
    int number;
    int bitToSet, bitToReset;
    int resultSet, resultReset;
    cout << "Please enter a number in decimal: ";
    cin >> number;
    cout << "Please enter the bit position to be set: ";
    cin >> bitToSet;
    cout << "Please enter the bit position to be reset: ";
    cin >> bitToReset;
    resultSet = number | (1 << bitToSet);
    resultReset = number & (~(1 << bitToReset));

    cout << "Original number: " << number << endl;
    cout << "Number after setting bit " << bitToSet << ": " << resultSet << endl;
    cout << "Number after resetting bit " << bitToReset << ": " << resultReset << endl;

    return 0;
}
```

## Output

![image](https://github.com/user-attachments/assets/67574776-8323-4317-a3ca-3d9280d0982e)

## Conclusion

Thus we learned how to manipulate bits in binary numbers by setting and resetting individual bits
