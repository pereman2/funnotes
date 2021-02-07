# Competitive programming notes

## Bitwise operations

even -> `x & 1 == 0`
odd -> `x & 1 == 1`
divisible by 2^k if -> `x & (2^k - 1) == 0`
not -> ~x = -x - 1
**shifting**
x << k shift k bits to the left to x == x * 2^k
x >> k shift k bits to the right to x == x / 2^k

modify kth bit:
    `x & (1 << k)` 
    `x | (1 << k)` kth bit to 1 
    `x | ~(1 << k)` kth bit to 1 
    `x ^ (1 << k)` kth bit invert

builtin functions for g++ compiler
```c++
int x = 5328; // 00000000000000000001010011010000
cout << __builtin_clz(x) << "\n"; // 19 number of zeros at the beggining
cout << __builtin_ctz(x) << "\n"; // 4 number of zeros at the end
cout << __builtin_popcount(x) << "\n"; // 5 the number of ones in the number
cout << __builtin_parity(x) << "\n"; // 1 parity of the number of ones
```
## DP

**properties**

- Overlapping subproblems
    -> store subproblems to not recompute

- Optimal substructure
    -> optimal path from i to j, if x is between i and j, then the optimal path 
    is the union of optimal path from i to x and x to j


