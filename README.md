# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.


## PROGRAM
```
#include <stdio.h>

int main() {
    // Step 1: Assign values to variables
    int a = 44, b = 3;

    // Step 2: Perform left shift operation
    int result = a << b;

    // Step 3: Display the result
    printf("Original value: %d\n", a);
    printf("Value after left shifting by %d positions: %d\n", b, result);

    return 0; // Stop the program
}
```
## OUTPUT
```
Original value: 44
Value after left shifting by 3 positions: 352
```








## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    // Step 2: Declare two variables for input
    int num1, num2;

    // Step 2: Read two numbers
    printf("Enter the first number: ");
    scanf("%d", &num1);

    printf("Enter the second number: ");
    scanf("%d", &num2);

    // Step 3: Check if the numbers are equal
    if (num1 == num2) {
        // Step 4: If equal, display the message
        printf("Both numbers are equal.\n");
    } else {
        // Step 4: If not equal, display the message
        printf("Both numbers are not equal.\n");
    }

    return 0; // Step 5: Stop the program
}
```

## OUTPUT
```
 Enter the first number: 10
Enter the second number: 10
Both numbers are equal.
```         
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <ctype.h> // Required for tolower()

int main() {
    // Step 2: Declare string variable
    char str[100];

    // Step 2: Read the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);  // Using fgets to handle spaces in the input

    // Step 3: Convert each character to lowercase
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]); // Convert to lowercase
    }

    // Step 4: Display the result
    printf("Lowercase string: %s\n", str);

    return 0; // Step 5: Stop the program
}
```
## OUTPUT
```
Enter a string: Hello World!
Lowercase string: hello world!
```



## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    char str[1000];
    int i = 0, count = 0;

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    // Remove newline character from fgets if present
    str[strcspn(str, "\n")] = '\0';

    // Skip leading spaces
    while (isspace(str[i])) {
        i++;
    }

    do {
        // If the current char is a space and the previous one is not a space,
        // we have found the end of a word
        if (isspace(str[i]) && !isspace(str[i - 1])) {
            count++;
        }
        i++;
    } while (str[i] != '\0');
```
## OUTPUT
```
Enter a string: Hello, how are you today?
Total number of words: 5
```




## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    char c1[100], c2[100];
    int i = 0, flag = 0;

    printf("Enter the first string (can include spaces): ");
    scanf("%[^\n]", c1);

    // Clear input buffer before taking the second string
    getchar();

    printf("Enter the second string (no spaces): ");
    scanf("%s", c2);

    while (c1[i] != '\0' && c2[i] != '\0') {
        if (c1[i] != c2[i]) {
            flag = 1;
            break;
        }
        i++;
    }

    // If one string is longer than the other
    if (c1[i] != '\0' || c2[i] != '\
```

## OUTPUT
 ```
Enter the first string (can include spaces): Hello World
Enter the second string (no spaces): Hello
Strings are not same.
```

## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

