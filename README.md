EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
```
#include <stdio.h>
#include <math.h>  // For round()

int main() {
    float num = 23.65;
    int rounded;
    float *ptr = &num;  // pointer to float

    // Use pointer to access value and round it
    rounded = (int) round(*ptr);

    printf("Original number: %.2f\n", *ptr);
    printf("Rounded number: %d\n", rounded);

    return 0;
}
```
## OUTPUT:
![Screenshot 2025-05-25 140055](https://github.com/user-attachments/assets/1b7e3b82-d0d9-4d7c-8d89-4f9fc4584e6b)


## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:
```
#include <stdio.h>

// Recursive function to calculate product (factorial)
unsigned long long product(int n) {
    if (n == 1) {
        return 1;  // Base case
    } else {
        return n * product(n - 1);  // Recursive call
    }
}

int main() {
    int n = 12;
    unsigned long long result;

    result = product(n);

    printf("Product of first %d natural numbers is: %llu\n", n, result);

    return 0;
}

```
## OUTPUT:
![Screenshot 2025-05-25 140139](https://github.com/user-attachments/assets/1efb0bc0-2aae-4f79-8357-55399750f14e)
    		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:
```
#include <stdio.h>

int main() {
    int rows, cols;

    // Input matrix size
    printf("Enter number of rows: ");
    scanf("%d", &rows);

    printf("Enter number of columns: ");
    scanf("%d", &cols);

    int matrix[rows][cols];

    // Input matrix elements
    printf("Enter elements of the matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][j]);
        }
    }

    // Calculate and print sum of each row
    for (int i = 0; i < rows; i++) {
        int rowSum = 0;
        for (int j = 0; j < cols; j++) {
            rowSum += matrix[i][j];
        }
        printf("Sum of row %d = %d\n", i + 1, rowSum);
    }

    return 0;
}

```

## OUTPUT

![Screenshot 2025-05-25 140232](https://github.com/user-attachments/assets/ec8a5056-8f94-487a-9aeb-404bbb58e053)

 ## RESULT
 Thus the program has been executed successfully.


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:
```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows;

    printf("Enter a string: ");
    scanf("%s", str);

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    int len = strlen(str);
    int index = 0;

    for (int i = 1; i <= rows; i++) {      // for each row
        for (int j = 1; j <= i; j++) {     // print i chars
            printf("%c ", str[index]);
            index = (index + 1) % len;     // wrap around string
        }
        printf("\n");
    }

    return 0;
}

```

 ## OUTPUT
![Screenshot 2025-05-25 140336](https://github.com/user-attachments/assets/027d8975-87e5-4ccf-9877-cb43aa78031f)

 

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int arr[6];
    int *ptr = arr;  // Pointer to the first element

    // Input 6 elements using pointer
    printf("Enter 6 integers:\n");
    for (int i = 0; i < 6; i++) {
        scanf("%d", ptr + i);  // or &arr[i]
    }

    // Display elements using pointer
    printf("You entered:\n");
    for (int i = 0; i < 6; i++) {
        printf("%d ", *(ptr + i));
    }
    printf("\n");

    return 0;
}
```
## OUTPUT

 ![Screenshot 2025-05-25 140440](https://github.com/user-attachments/assets/ac62263f-47ef-450e-9551-43b81d2c4a97)


## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


