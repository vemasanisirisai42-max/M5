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
int main() 
{
    double num = 23.65;
    double *ptr = &num;
    *ptr = 25.0;
    printf("Modified value: %.2f\n", num);
    return 0;
}
```
## OUTPUT:
 	
<img width="925" height="501" alt="image" src="https://github.com/user-attachments/assets/7f67594a-c10e-4142-9fcf-dc71d358afdd" />











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
unsigned long long calculateProduct(int n) 
{
    if(n == 1) 
    return 1;
    else
    return n * calculateProduct(n - 1);
}
int main() 
{
    int n = 12;
    unsigned long long product;
    product = calculateProduct(n);
    printf("Product of first %d natural numbers is: %llu\n", n, product);
    return 0;
}
```
## OUTPUT:
 <img width="941" height="429" alt="image" src="https://github.com/user-attachments/assets/51e4e23a-a5b4-4852-9c5a-59d4ae5c6756" />
    		
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
int main() 
{
    int rows, cols;
    scanf("%d", &rows);
    scanf("%d", &cols);
    int matrix[rows][cols];
    for(int i = 0; i < rows; i++) 
    {
        for(int j = 0; j < cols; j++) 
        {
            scanf("%d", &matrix[i][j]);
        }
    }
    for(int i = 0; i < rows; i++) 
    {
        int sum = 0;
        for(int j = 0; j < cols; j++) 
        {
            sum += matrix[i][j];
        }
        printf("Sum of row %d: %d\n", i+1, sum);
    }
    return 0;
}
```

## OUTPUT

<img width="896" height="735" alt="image" src="https://github.com/user-attachments/assets/e201fbfa-275e-42d2-ba00-c6ad02d955dd" />

 
 

 ## RESULT
 


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
int main() 
{
    char str[100];
    int rows;
    printf("Enter a string: ");
    scanf("%s", str);
    printf("Enter number of rows: ");
    scanf("%d", &rows);
    int len = strlen(str);
    for(int i = 1; i <= rows; i++) 
    {
        for(int j = 1; j <= i; j++) 
        {
            printf("%c ", str[(j-1) % len]);
        }
        printf("\n");
    }
    return 0;
}
```

 ## OUTPUT

 <img width="905" height="618" alt="image" src="https://github.com/user-attachments/assets/92bc94ce-9106-49c4-8772-f623701d7687" />


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
int main()
{
    int arr[10];      
    int *parr = arr;  
    int n, i;
    scanf("%d", &n);
    if(n > 6 || n < 1) 
    return 1;
    printf("Enter %d integer elements:\n", n);
    for(i = 0; i < n; i++) 
    {
        scanf("%d", parr + i);  
    }
    printf("The elements of the array are:\n");
    for(i = 0; i < n; i++) 
    {
        printf("%d ", *(parr + i));
    }
    printf("\n");
    return 0;  
}
```
## OUTPUT

 
<img width="906" height="596" alt="image" src="https://github.com/user-attachments/assets/d6a5a11f-11b7-42f4-9ebe-420cb355680b" />

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


