# Concepts

# RTOS 
The main feature of an real-time system is that it can garuntee that something will happen within a specific amount of time, it is deterministic by design. The Operating system built on top of the RTOS provides an layer of abstraction between the hardware & applications. 

Main components an RTOS must support: 
- Async/Sync I/O
- Memory Locking 
- Semaphores
- Shared Memory (Mapping Physical to Virtual Space)
- Scheduling
- Timers
- Interprocess Communication (Information shared between threads)
- Real-time files & threads 

Additional Requirements:
- Low overhead (context switch times and OS overhead should be minimal)
- Pre-emptive (Executing thread can be pre-empted by a higher priority thread)
- Deterministic Syncronization (Multiple threads can communicate between themselves in a predictable time)
- Priority levels 
- Pre-defined Latencies (API calls have expected latencies)

# Digital Logic 

## 2's Complement
Representation of a negative number in binary. 

Conversion: 
1. One's Compliment: Invert all 1's and 0's
2. Two's Compliment: Add 1 to the one's compliment

```c
int val = 5; // 0101
int val_ones_compliment = ~val; // 1010
int val_twos_compliment = val_ones_compliment + 1; // 1011

printf("%d\n", val_twos_compliment); // prints -5
```

## Endain
Endianness is the order in which bytes are stored in memory.
Value: `0x12345678`

**Little Endian**: Least significant byte is stored first.

Address| 0x1 | 0x2 | 0x3 | 0x4
---|---|---|---|---
Byte| 0x78 | 0x56 | 0x34 | 0x12

**Big Endian**: Most significant byte is stored first.

Address| 0x1 | 0x2 | 0x3 | 0x4
---|---|---|---|---
Byte| 0x12 | 0x34 | 0x56 | 0x78

### Determine Endianness
Since char is 1 byte whereas int is 2 or 4 bytes if the system is little endian then the LSB is stored first, which in this case is 1. Otherwise the MSB is stored first, which is 0. 
```c
bool is_little_endian(void){
    unsigned int val = 1;

    char *c = (char*)&val;
    if (*c) {
        return true;
    } else {
        return false;
    }
}
```

