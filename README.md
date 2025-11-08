# Assignment-2-C-Programming.
1. What do you mean by structures?

A structure in C is a user-defined data type that allows you to combine variables of different data types under one name.
It is useful when you want to represent a record — for example, a student having name, roll number, and marks.

Syntax:

struct structure_name {
    data_type member1;
    data_type member2;
    ...
};

Example:

struct Student {
    int roll;
    char name[50];
    float marks;
};

This creates a new data type called struct Student, which can hold multiple pieces of related data.


---

2. What do you mean by array & pointer array?

Array:

An array is a collection of elements of the same data type stored in contiguous memory locations.

Example:

int numbers[5] = {10, 20, 30, 40, 50};

Here, numbers is an array of 5 integers.

Pointer Array (Array of Pointers):

An array of pointers is an array whose elements are pointers that can point to data or variables.

Example:

int a = 10, b = 20, c = 30;
int *arr[3] = {&a, &b, &c};

Here, arr is an array of 3 pointers to integers.


---

3. Compare two structure variables using comparison operators (== and !=)

C does not allow direct comparison of structure variables using == or !=.
However, you can compare each member individually.

Example:

#include <stdio.h>
#include <string.h>

struct Student {
    int roll;
    char name[20];
    float marks;
};

int main() {
    struct Student s1 = {1, "Alice", 85.5};
    struct Student s2 = {1, "Alice", 85.5};

    if (s1.roll == s2.roll && strcmp(s1.name, s2.name) == 0 && s1.marks == s2.marks)
        printf("Structures are equal.\n");
    else
        printf("Structures are not equal.\n");

    return 0;
}


---

4. Perform arithmetic operations on structures

You cannot directly perform arithmetic operations (like addition or subtraction) on structure variables.
But you can perform arithmetic on their members.

Example:

#include <stdio.h>

struct Point {
    int x;
    int y;
};

int main() {
    struct Point p1 = {10, 20};
    struct Point p2 = {5, 15};
    struct Point result;

    // Performing arithmetic operations on structure members
    result.x = p1.x + p2.x;
    result.y = p1.y - p2.y;

    printf("Result (x + y): x = %d, y = %d\n", result.x, result.y);
    return 0;
}

Output:

Result (x + y): x = 15, y = 5


---

✅ Summary Table

Concept	Description	Example

Structure	User-defined data type to store different types of data together	struct Student { int roll; char name[50]; float marks; };
Array	Collection of same-type elements	int a[5];
Pointer Array	Array storing pointers	int *ptr[3];
Compare Structures	Compare each member manually	if (s1.roll == s2.roll && strcmp(...))
Arithmetic on Structures	Perform arithmetic on individual members	result.x = p1.x + p2.x;



---
