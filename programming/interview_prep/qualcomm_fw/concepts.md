#  Algorithms in C

## Time Complexity

### Example 1
**O(N)**
- In the first iteration, the total iterations is 2 * N. 
- In the second iteration, the total iterations is N.
- In the third iteration, the total iterations is N/2.
- In the fourth iteration, the total iterations is N/4.

In general: `total iterations` = 2N + N/2 + N/4 + ... + N/2^k => This approaches 3N, which linaer time, hence O(N).
```
int count = 0;
for (int i = N; i > 0; i /= 2) {
    for (int j = 0; j < i; j++) {
        count += 1;
    }
}
```

### Example 2
The time complexity is N * N + N, which is O(N^2).
```
int a = 0, b = 0;    
for (i = 0; i < N; i++) {
    for (j = 0; j < N; j++) {
        a = a + j;
    }
}
for (k = 0; k < N; k++) {
    b = b + k;
}
```

### Example 3
**O(Log(N))**

Anything with binary search or divide and conquer characteristics. 
```
// log 2
for(int i = 1; i <= n; i = i * 2)
  print "hello";

// log 10
for(int i = 1; i <= n; i = i * 10)
  print "hello";
```

## Space Complexity

### Example 1
Since the only storage is variables A and B, the space complexity is O(1).
```
int a = 0, b = 0;    
for (i = 0; i < N; i++) {
    for (j = 0; j < N; j++) {
        a = a + j;
    }
}
for (k = 0; k < N; k++) {
    b = b + k;
}