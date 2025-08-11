# POINTERS-IN-CPP


================================================================================
                                 ### AIM : POINTERS IN C++
================================================================================

## SOFTWARE USED : VS CODE

## THEORY

General Theory on Pointers in C++  
A pointer is a special variable used to store the memory address of another variable.  
In C++, pointers are widely used for direct memory access, dynamic memory allocation,  
and efficient handling of arrays and strings.

### 1. Pointer Basics  
A pointer is declared by placing an asterisk (*) before the variable name.  
Example:


### 2. Pointer Arithmetic  
Pointers can be incremented and decremented.  
When incremented (`ptr++`), the pointer moves to the next memory location of its data type:


For int*    → moves by 4 bytes (on most systems)
For double* → moves by 8 bytes
For char*   → moves by 1 byte


This allows traversal of arrays without using indexing.




### 3. Pointers and Arrays  
The name of an array acts like a pointer to its first element.  
Example: `arr` is equivalent to `&arr[0]`.

Elements can be accessed using pointer arithmetic:  
`*(arr + i)` is the same as `arr[i]`.

### 4. Strings and Pointers  
In C++, a string (in C-style) is stored as a character array ending with the null character `'\0'`.  
A `char*` pointer can be used to traverse each character until the null terminator is reached.

### 5. Common Pointer Applications  
- Traversing arrays without indexing.  
- Reversing arrays/strings by swapping elements using start and end pointers.  
- Summation and difference of values by dereferencing pointers.  
- Palindrome checking by comparing characters from both ends moving inward.

### 6. Advantages of Using Pointers  
- Efficient in accessing and modifying data.  
- Allows dynamic memory allocation.  
- Enables passing large data structures (like arrays) to functions without copying.

### 7. Precautions  
- Uninitialized pointers may cause undefined behavior.  
- Accessing memory outside valid range can cause crashes.  
- Always ensure a pointer points to valid memory before dereferencing.

---

## 1. Algorithm – Pointer Arithmetic on Different Data Types  
**Aim:** Demonstrate how pointer increment changes address depending on data type.

**Steps:**  
- Start  
- Declare variables of type int, double, and bool.  
- Create pointers pointing to each variable.  
- Print the initial address stored in each pointer.  
- Increment each pointer by 1.  
- Print the new address for each pointer.  
- Stop

---

## 2. Algorithm – Sum of Array Elements Using Pointers  
**Aim:** Calculate the sum of elements in an array using pointer arithmetic.

**Steps:**  
- Start  
- Declare and initialize an integer array.  
- Initialize a pointer to point to the first element of the array.  
- Initialize a variable sum = 0.  
- Repeat for each element in the array:  
  - Add the value pointed to by (pointer + i) to sum.  
- Print the total sum.  
- Stop

---

## 3. Algorithm – Reverse an Array Using Pointers  
**Aim:** Reverse the elements of an array using two pointers.

**Steps:**  
- Start  
- Declare and initialize an array.  
- Find the length of the array.  
- Initialize `ptr` to point to the first element, and `ptr1` to point to the last element.  
- Repeat until `ptr` is before `ptr1`:  
  - Swap the values pointed to by `ptr` and `ptr1`.  
  - Increment `ptr` and decrement `ptr1`.  
- Print the reversed array.  
- Stop

---

## 4. Algorithm – Check if a String is Palindrome Using Pointers  
**Aim:** Determine if a given string is a palindrome using two pointers.

**Steps:**  
- Start  
- Read the string from the user.  
- Initialize `start` to point to the first character, and `end` to point to the last character (before `'\0'`).  
- Repeat until `start` is before `end`:  
  - If `*start` is not equal to `*end`, print "Not a palindrome" and stop.  
  - Else, increment `start` and decrement `end`.  
- If loop completes, print "Palindrome".  
- Stop

---

## Conclusion  
Pointers are one of the most powerful features of C++, enabling direct interaction with memory and providing flexibility in data manipulation. However, they require careful handling to avoid errors like segmentation faults and memory leaks.

