# 15.-Exception-Handling

Aim: To study and implement Exception Handling.

Tools Used: VS Code or Programiz online compiler.

# Theory

## Exception Handling in Cpp
Exception handling in C++ is a mechanism to handle runtime errors and maintain normal program flow. It allows a program to catch and handle errors without crashing. The key keywords used are try, catch, and throw. Code that might generate an error is written inside a try block. When an exception occurs, it is thrown using the throw keyword and caught by a corresponding catch block. Multiple catch blocks can be used to handle different types of exceptions. Exception handling improves program reliability and makes debugging easier. It is especially useful in situations like division by zero, invalid inputs, or memory allocation failures. Proper use of exceptions ensures that resources are released and the program continues safely.

```

#include <iostream>
using namespace std;

int main() {
    try {
        // Code that may generate an exception
        // Example: int result = a / b;

        // If some error occurs, throw an exception
        // throw ExceptionType; 
    }
    catch (int e) { // Catch integer exceptions
        cout << "Integer exception caught: " << e << endl;
    }
    catch (const char* msg) { // Catch string/char exceptions
        cout << "Exception caught: " << msg << endl;
    }
    catch (...) { // Catch all other exceptions
        cout << "Unknown exception caught." << endl;
    }

    cout << "Program continues after exception handling." << endl;
    return 0;
}

```

--> **Key Points:-**

1. **Purpose:** Handles runtime errors to maintain normal program flow.
2. **Keywords:** `try`, `catch`, and `throw` are used for exception handling.
3. **Try Block:** Contains code that may generate an exception.
4. **Throw Statement:** Used to signal or raise an exception when an error occurs.
5. **Catch Block:** Catches and handles the exception; multiple catch blocks can handle different types.
6. **Default Catch:** `catch(...)` can catch any type of exception not specifically caught.
7. **Program Continuity:** After handling, the program continues without crashing.
8. **Applications:** Useful for division by zero, invalid inputs, memory allocation failures, file handling errors.
9. **Advantages:** Improves program reliability, readability, and debugging.

# Program-1: Division of two numbers
This program demonstrates exception handling in C++ using a division operation. The user inputs two numbers, and the program attempts to divide them inside a try block. If the divisor is zero, an exception is thrown using the throw keyword. The catch block catches the exception and displays an appropriate error message, preventing the program from crashing. If no exception occurs, the division result is displayed normally. This shows how exception handling ensures safe execution and handles runtime errors gracefully.

--> Algorithm:

1. Start the program.
2. Input two numbers num1 and num2 from the user.
3. Use a try block to perform division:
  --If num2 == 0, throw the value of num2 as an exception.
  --Else, calculate result = num1 / num2 and display it.
4. Catch the exception using a catch block:
  --Display the message "Exception: Division by zero is not allowed!".
5. End the program.

# Program-2: Voting Validity
This program demonstrates exception handling in C++ using an age check for voting eligibility. The user enters their age, and the program checks it inside a try block. If the age is less than 18, an exception is thrown using the throw keyword. The catch block catches the exception and displays an appropriate message, preventing the program from terminating unexpectedly. If the age is 18 or above, the program displays that the user is eligible to vote. This illustrates how exceptions can handle logical conditions and ensure safe program execution.

--> Algorithm:

1. Start the program.
2. Input the user’s age.
3. Use a try block to check the age:
  --If age < 18, throw the age as an exception.
  --Else, display "You are eligible to vote!".
4. Catch the exception using a catch block:
  --Display "Exception: You are below 18 years of age!".
5. End the program.

# Conclusion
Both programs demonstrate the use of exception handling in C++ to manage runtime and logical errors safely. The division program shows how to prevent a crash when dividing by zero by using throw and catch. The age eligibility program illustrates handling logical conditions, ensuring that the program responds appropriately when the user is below the required age. In both cases, the try block contains the code that may cause an error, and the catch block handles it gracefully. These examples highlight how exception handling improves program reliability, prevents abnormal termination, and ensures smooth execution.
