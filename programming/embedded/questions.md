# Example Questions

## Question 1
Write a simple function to check if a value is even or odd. 

Answer:
```c
#include <stdbool.h>

// Documentation: 
// Perform a bitwise AND on the LSB, if the result is 1, then the number is odd, otherwise even.
bool is_odd(int *val){
    return *val & 1; 
}

// By contrast; 
bool is_even(int *val){
    return *val & 0; 
}
```

## Question 2
Write a simple function to calculate the factorial of a number.
```c
int factorial(int val){
    if (val < 1) 
        return 1; 
    else:
        return val * factorial(val - 1); 
}
```

## Question 3
Given an array where only one value occurs an odd number of times, find the value.
```c
// Documentation:
// Any values with bits that occur an even number of times will be 0 from the XOR operation. 
// Only bits that occur an odd number of times will be 1, since there is only 1 odd number 
// the left over bits are the value of that one odd number. 
int find_odd_occurrence(int *arr, int size){
    int result = 0; 
    for (int i = 0; i < size; i++){
        result ^= arr[i]; 
    }
    return result; 
}
```

## Question 4 
Swap two numbers without using a temporary variable in the fastest way possible.
```c
void swap(int *a, int *b){
    *a ^= *b; // Combine a and b bitwise 
    *b ^= *a; // Remove original b component, leaving only a
    *a ^= *b; // Remove original a component, leaving only b
}
```

## Question 5
Given an integer, determine the number of trailing zeros in its binary representation.
```c
int solve(int A) {

    int n = 0; 
    while(!(A & (1 << n))){
        n++;  
    }

    return n;
}
```

## Question 6
Given an integer array A containing N distinct integers, you have to find all the leaders in the array A. An element is leader if it is strictly greater than all the elements to its right side.

Solution: 
 * Start at the end, check if the n-m element is greater than the n-1 element
 * first element that is becomes a leader, then k = A[n-m] and the next value greater than k
 * is the next leader & repeat until the start of the array.
 ```c
 /**
 * @input A : Integer array
 * @input n1 : Integer array's ( A ) length
 * 
 * @Output Integer array. You need to malloc memory, and fill the length in len1
 *
 */
int* solve(int* A, int n1, int *len1) {
    *len1 = n1;
    int i;
    int count = 1;
    int *ret = (int*)malloc(*len1*sizeof(int));
    
    int k = A[n1-1];
    ret[0] = A[n1-1];
    for(i = n1-2; i>= 0; i--){
        if(A[i] > k){
            ret[count] = A[i];
            k = A[i];
            count++;
        }
    }

    *len1=count;
    return ret;
}
 ```

 ## Question 7
 Given a sorted linked list, delete all duplicates such that each element appears only once.
 ```c
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 * @input A : Head pointer of linked list 
 * 
 * @Output head pointer of list.
 */
listnode* deleteDuplicates(listnode* A) {
    listnode *head = A;
    listnode *current = A;

    while(current->next != NULL){
        if(current->val == current->next->val){
            current->next = current->next->next; 
        } else{
            current = current->next; 
        }
    }

    return head; 
}
 ```

 ## Question 8
Given an unsigned integer, return the sum of its digits.
 ```c
int digitSum(unsigned int num){
    if((num % 10) == 0)
        return 0; 

    return (num % 10) + digitSum(num/10);
}
 ```

## Question 9
Implement a function to perform matrix multiplication. 
```c

```