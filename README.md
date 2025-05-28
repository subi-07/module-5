## NAME : SUBITHRA R
## REGISTER NO : 212224110050
# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
int main()
 {
    float length, width;
    float *ptrLength = &length, *ptrWidth = &width;  
    printf("Enter the length of the rectangle: ");
    scanf("%f", ptrLength); 
    printf("Enter the width of the rectangle: ");
    scanf("%f", ptrWidth);  
    float area = (*ptrLength) * (*ptrWidth);
    printf("The area of the rectangle is: %.2f\n", area);

    return 0;
}

```
## OUTPUT
![Screenshot 2025-04-28 141236](https://github.com/user-attachments/assets/50510062-20e9-48fa-8a8f-7d375eac80ec)

		       	


## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>  

int main()
 {
    char *str = (char *)malloc(8 * sizeof(char));  
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0'; 
    printf("%s\n", str);
    free(str);

    return 0;
}


```
## OUTPUT
![Screenshot 2025-04-28 141614](https://github.com/user-attachments/assets/48af4278-1ef5-4e31-a804-07394f939937)



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM

```
#include <stdio.h>
#include <string.h>
struct Student {
    char name[50];
    int roll_no;
    float marks;
};

int main() {
    struct Student student1;  
    printf("Enter student name: ");
    fgets(student1.name, sizeof(student1.name), stdin); 
    student1.name[strcspn(student1.name, "\n")] = 0; 
    printf("Enter roll number: ");
    scanf("%d", &student1.roll_no);
    printf("Enter marks: ");
    scanf("%f", &student1.marks);
    printf("\nStudent Information:\n");
    printf("Name: %s\n", student1.name);
    printf("Roll Number: %d\n", student1.roll_no);
    printf("Marks: %.2f\n", student1.marks);

    return 0;
}


```
## OUTPUT

![Screenshot 2025-04-28 141820](https://github.com/user-attachments/assets/a4d72db8-0e97-4671-a22e-8a5ee368e437)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Employee 
{
    char name[50];
    float basic_salary;
    float gross_salary;
};

int main() {
    struct Employee employees[3];  
    for (int i = 0; i < 3; i++) {
        printf("\nEnter details for employee %d:\n", i + 1);
        printf("Enter name: ");
        fgets(employees[i].name, sizeof(employees[i].name), stdin);
        employees[i].name[strcspn(employees[i].name, "\n")] = 0;
        printf("Enter basic salary: ");
        scanf("%f", &employees[i].basic_salary);
        employees[i].gross_salary = employees[i].basic_salary + 
                                    (0.20 * employees[i].basic_salary) + 
                                    (0.10 * employees[i].basic_salary);
        getchar();
    }
    printf("\nEmployee Information and Gross Salary:\n");
    for (int i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("Name: %s\n", employees[i].name);
        printf("Basic Salary: %.2f\n", employees[i].basic_salary);
        printf("Gross Salary: %.2f\n", employees[i].gross_salary);
    }

    return 0;
}

```

 ## OUTPUT

 ![image](https://github.com/user-attachments/assets/c2db6a23-f263-4684-8256-e027a7e73ae1)


## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM

```

#include <stdio.h>
struct Student 
{
    char name[50];
    int marks[5];  
    float total;
    float average;
};

int main() 
{
    struct Student student; 
    printf("Enter student name: ");
    fgets(student.name, sizeof(student.name), stdin);

    printf("Enter marks for 5 subjects:\n");
    student.total = 0;
    for (int i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%d", &student.marks[i]);
        student.total += student.marks[i];  
    }
    student.average = student.total / 5;

    printf("\nStudent Name: %s", student.name);
    printf("Total Marks: %.2f\n", student.total);
    printf("Average Marks: %.2f\n", student.average);

    return 0;
}

```
## OUTPUT
![image](https://github.com/user-attachments/assets/0306a7fe-b7c3-4fd0-ba9a-529324bd8e5b)



## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


