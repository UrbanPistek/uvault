#  Algorithms in C

## Return indexes of two nums that add to target 

- Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.
- You may assume that each input would have exactly one solution, and you may not use the same element twice.
- You can return the answer in any order.

**Brute Force Solution:** 
- Time: O(n^2) -> 1 nested for loop
- Space: O(1) -> Space remains constant regradless of input size
```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* twoSum(int* nums, int numsSize, int target, int* returnSize){
    
    static int* return_nums; // Create pointer first
    *returnSize = 2;
    return_nums = (int*) malloc(2 * sizeof(int)); // Allocate memory 

    for(int i = 0; i < numsSize; i++){
        for(int j = i+1; j < numsSize; j++){
            if((nums[i] + nums[j]) == target){
                
                return_nums[0] = i; 
                return_nums[1] = j;
                // printf("%d %d || %d %d", i, j, return_nums[0], return_nums[1]);
                
                return return_nums; 
            }
        }
    }
    
    return NULL;
}
```
**One Pass Hash Solution:**
Interate through array mapping each value at its index to a hashmap, then check if the hashmap contains the compliment. 
- Time: O(n) -> Iterate through loop once
- Space: O(n) -> Hash map grows linearly with input size
```c
/**
 * Sudo code: 
 */
int* twoSum(int* nums, int numsSize, int target, int* returnSize){
    
    static int* return_nums; // Create pointer first
    *returnSize = 2;
    return_nums = (int*) malloc(2 * sizeof(int)); // Allocate memory 

    for(int i = 0; i < numsSize; i++){
        int compliment = target - nums[i];
        if (hashMapContains(compliment)){
            return_nums[0] = hashMapGet(compliment);
            return_nums[1] = i; 

            return return_nums;  
        }

        hashMapAdd(nums[i], i)
    }
    
    return NULL;
}
```

##  Remove Duplicates from Sorted Array 

- Given an integer array nums sorted in non-decreasing order, remove the duplicates in-place such that each unique element appears only once. The relative order of the elements should be kept the same.
- Do not allocate extra space for another array. You must do this by modifying the input array in-place with O(1) extra memory.
- If there are k elements after removing the duplicates, then the first k elements of nums should hold the final result

**Two Pointers Solution:** 
- Time: O(n) -> Only at most n interations needed
- Space: O(1) -> Space remains constant - only using 2 pointers regradless of input size
```c
int removeDuplicates(int* nums, int numsSize){

    // Input checks
    if (numsSize == 0){
        return 0; 
    }
    
    if (numsSize == 1){
        return 1; 
    }
    
    // For numsSize > 1
    int i = 0; 
    for(int j = 1; j < numsSize; j++){

        // If the numbers are equal, skip over
        // If not equal, store
        if(nums[i] != nums[j]){
            i++; 
            nums[i] = nums[j]; 
        }
    }
    
    return i + 1; 
}
```

## Invert Binary Tree 

```c
/**
 * Definition for binary tree
 * struct TreeNode {
 *     int val;
 *     struct TreeNode *left;
 *     struct TreeNode *right;
 * };
 * 
 * typedef struct TreeNode treenode;
 *
 * @input root : Root pointer of the tree 
 * @Output root pointer of tree.
 */

treenode* invertTree(treenode* root) {
    if(root != NULL)
    {
        treenode* temp = invertTree(root->left);
        root->left = invertTree(root->right);
        root->right = temp;
    }
    return root;
}
```

## Intersection of 2 Arrays 
Assume both arrays are sorted and that the output returns 
```c
/**
 * @input A : Read only Integer array
 * @input n1 : Integer array's ( A ) length
 * @input B : Read only Integer array
 * @input n2 : Integer array's ( B ) length
 * 
 * @Output Integer array. You need to malloc memory, and fill the length in len1
 */

 #define MAX(a, b) (a>b?a:b)

int* intersect(const int* A, int n1, const int* B, int n2, int *len1) {
    int *result = (int *)malloc(MAX(n1,n2) * sizeof(int));
    int i = 0, j = 0, size = 0;
    
    while (i < n1 && j < n2) {
        if (A[i] == B[j]) {
            result[size] = A[i];
            size++;
            i++;
            j++;
        } else if (A[i] < B[j]) {
            i++;
        } else {
            j++;
        }
    }
    
    *len1 = size;
    return result;
}
```

## Reverse Singlely Linked List

```c
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     struct ListNode *next;
 * };
 */

struct ListNode* reverseList(struct ListNode* head){
    
    struct ListNode* current;
    struct ListNode* previous = NULL; 
    struct ListNode* next;
    current = head; 
    
    while(current != NULL){
        
        next = current->next; // set next to next
        current->next = previous; // reverse current
        
        previous = current; // update previous to current
        current = next; // move current to next node
        
    }
    
    // return previous since current should be at NULL
    return previous;
}
```

## Max Depth of Binary Tree

```c
/**
 * Definition for binary tree
 * struct TreeNode {
 *     int val;
 *     struct TreeNode *left;
 *     struct TreeNode *right;
 * };
 * 
 * typedef struct TreeNode treenode;
 *
 * @input A : Root pointer of the tree  
 * @Output Integer
 */
int maxDepth(treenode* A) {

    if(A == NULL)
        return 0; 
    else{
        int depthA = maxDepth(A->left); 
        int depthB = maxDepth(A->right);

        if(depthA > depthB)
            return depthA + 1;
        return depthB + 1;  
    }
}
```

## Determine single number in array of numbers
Store the value and XOR it - essentially if the stored value contains the same set of bits, the XOR will reset them to 0.
This way only the bits of the number that appears once remains. 
```c
int singleNumber(const int* A, int n1) {
    int res=0;
    int i;
    for(i = 0; i < n1; ++i) {
        res = res ^ A[i]; // ^ = XOR
    }
//    printf("%d\n",res);
    return res;
}
```

## Return the Sum of the Min/Max of an Array 
```c
/**
 * @input A : Integer array
 * @input n1 : Integer array's ( A ) length
 * 
 * @Output Integer
 */
int solve(int* A, int n1) {

    int max = -1000000000; // -10^9
    int min = 1000000000; // 10^9 
    int i; 

    for(i = 0; i < n1; i++){
        if(A[i] > max)
            max = A[i];
        if(A[i] < min)
            min = A[i];
    }

    return max + min; 
}
```

## Balanced Parentheses in a String 
- Create stack 
- Traverse string. If '(' push to stack. If ')' pop from stack if value popped is '(' then continue, else return false. 
- If after traversal the stack has a '(' left then return false.
```
```