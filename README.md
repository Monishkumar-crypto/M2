# EX-06 - Looping
## AIM:
Write a C program to print even numbers ranging from M to N (including M and N values).

## ALGORITHM:
1.	Declare two integer variables to store the values of M and N.
2.	Use the printf function to prompt the user to enter the values of M and N.
3.	Use the scanf function to read the values of M and N from the user.
4.	Use a loop (for or while) to iterate from M to N.
5.	Inside the loop, check if the current number is even.
6.	If the current number is even, print it.
7.	Continue the loop until you have iterated through all numbers from M to N.

## PROGRAM:
#include <stdio.h>

int main() {
    int M, N;

    
    printf("Enter the value of M: ");
    scanf("%d", &M);

    printf("Enter the value of N: ");
    scanf("%d", &N);

    
    printf("Even numbers from %d to %d are:\n", M, N);
    for (int i = M; i <= N; i++) {
        if (i % 2 == 0) {
            printf("%d ", i);
        }
    }

    printf("\n"); 
    return 0;
}



## OUTPUT:



![Screenshot 2025-04-29 212457](https://github.com/user-attachments/assets/b20e4434-f0a8-49d1-98c6-4ed64135e836)







## RESULT:
Thus the program to print even numbers ranging from M to N (including M and N values) has been executed successfully
 
 


# EX-07-Nested-loop

## AIM:

Write a C program to print the given triangular pattern using loop.

## ALGORITHM:

1.	Declare a variable to store the number of rows in the triangle.
2.	Use the printf function to prompt the user to enter the number of rows.
3.	Use a loop (for or while) to iterate through each row.
4.	Inside the loop, use another loop to print the desired number of asterisks for each row.
5.	Continue the loop until you have printed the entire triangular pattern.

## PROGRAM:
#include <stdio.h>

int main() {
    int rows;

    // Step 1: Prompt user to enter number of rows
    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    // Step 2: Outer loop for rows
    for (int i = 1; i <= rows; i++) {
        // Step 3: Inner loop to print asterisks in each row
        for (int j = 1; j <= i; j++) {
            printf("* ");
        }
        // Move to the next line after printing each row
        printf("\n");
    }

    return 0;
}



## OUTPUT:

![Screenshot 2025-04-29 212804](https://github.com/user-attachments/assets/06d6f3b3-12be-4ca0-b2e2-ce9d8d7eeba2)




## RESULT:

Thus the program to print the given triangular pattern using loop has been executed successfully
 
 


# EX-08-Functions

## AIM:

Write a C program to perform addition and subtraction of two numbers using functions (with argument and without return type).

## ALGORITHM:

1.	Declare two functions, one for addition and one for subtraction. Both functions should take two integer arguments.
2.	Inside the addition & subtraction function, add & subtract the two numbers and print the result.
3.	In the main function, declare two integer variables and read their values from the user.
4.	Call the addition and subtraction functions, passing the two numbers as arguments.

## PROGRAM:
#include <stdio.h>

// Step 1: Declare functions
void add(int a, int b);       // Function for addition
void subtract(int a, int b);  // Function for subtraction

int main() {
    int num1, num2;

    // Step 3: Get input from the user
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Step 4: Call the functions
    add(num1, num2);
    subtract(num1, num2);

    return 0;
}

// Step 2: Define the functions
void add(int a, int b) {
    int result = a + b;
    printf("Addition result: %d\n", result);
}

void subtract(int a, int b) {
    int result = a - b;
    printf("Subtraction result: %d\n", result);
}



## OUTPUT:



![Screenshot 2025-04-29 213033](https://github.com/user-attachments/assets/100223c1-a16b-47a5-9621-250064362a81)



## RESULT:

Thus the program to perform addition and subtraction of two numbers using functions has been executed successfully
 
 


# EX-09-Use For Loop

## AIM:

Write a c program to find the sum of odd digits using for loop

## ALGORITHM:

1.	Declare variables to store the input number and the sum of odd digits.
2.	Initialize the sum of odd digits to 0.
3.	Use a for loop to iterate through each digit of the input number.
4.	Inside the loop, extract the rightmost digit of the number (using the modulo operator % and division by 10).
5.	If the digit is odd, add it to the sum of odd digits.
6.	Print the sum of odd digits.

## PROGRAM:
#include <stdio.h>

int main() {
    int number, digit, sum = 0;

    // Step 1: Read input number
    printf("Enter a number: ");
    scanf("%d", &number);

    // Step 2: Use a for loop to process each digit
    for (; number > 0; number /= 10) {
        digit = number % 10;          // Step 4: Extract rightmost digit
        if (digit % 2 != 0) {         // Step 5: Check if digit is odd
            sum += digit;             // Add to sum if odd
        }
    }

    // Step 6: Display result
    printf("Sum of odd digits: %d\n", sum);

    return 0;
}


## OUTPUT:


![Screenshot 2025-04-29 213347](https://github.com/user-attachments/assets/54c94bb1-4b75-4b56-bac6-2ba4aa9435ab)


## RESULT:

Thus the program to find the sum of odd digits using for loop has been executed successfully.




# EX – 10 - Factorial of a Number Using a Function
## AIM:
To write a C program that calculates the factorial of a given number using a user-defined function.
## ALGORITHM:
1.	Start
2.	Declare the function fact().
3.	In the main() function, call the fact() function.
4.	In fact() function:
a.	Declare variables i, N, and fact (initialized to 1).
b.	Read an integer N from the user.
c.	Use a for loop from 1 to N:
i.	Multiply fact by i in each iteration.
d.	After the loop, print the factorial value.
5.	End

## PROGRAM:
#include <stdio.h>

// Step 2: Declare the function
void fact();

int main() {
    // Step 3: Call the fact() function
    fact();
    return 0;
}

// Step 4: Define the fact() function
void fact() {
    int i, N;
    unsigned long long factorial = 1; // Use long long to handle large results

    // Step 4b: Read input from user
    printf("Enter a positive integer: ");
    scanf("%d", &N);

    // Step 4c: Check for negative input
    if (N < 0) {
        printf("Factorial is not defined for negative numbers.\n");
        return;
    }

    // Step 4c: Use a for loop to calculate factorial
    for (i = 1; i <= N; i++) {
        factorial *= i;
    }

    // Step 4d: Print the result
    printf("Factorial of %d is %llu\n", N, factorial);
}


## OUTPUT:

![Screenshot 2025-04-29 213524](https://github.com/user-attachments/assets/7f880ad1-578c-455f-83db-8fd15bf27749)

## RESULT:
The program correctly computes the factorial of a given number using a separate function and displays the result.
 
