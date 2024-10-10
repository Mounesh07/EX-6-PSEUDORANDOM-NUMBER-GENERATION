# EX-6-PSEUDORANDOM-NUMBER-GENERATION

## AIM :
To implement Pseudorandom Number Generation using Standard Library.

## ALGORITHM :
1. Get the number of random numbers to generate from the user.

2. Read the minimum and maximum values for the random number range.
3. Initialize the random seed using the current time.
4. Generate a random number by calculating the remainder of division with the range (max - min + 1) and adding the minimum value.
5. Repeat the random number generation for the specified count.
6. Print each generated random number.
7. End the program.

## PROGRAM :
```C
#include <stdio.h>

//Constants for LCG
#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

//Linear Congruential Generator function
unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("\n\n\n\n*****Pseudorandom number generator*****\n\n\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/af8cae45-203e-49b5-af21-1b8009c451d3)

## RESULT:
The program for Pseudorandom Number Generation is executed successfully.
