> Week 3 Practice Problems

- Problem 1: Create a method that takes in an integer and generates an integer array of that size, filled with random numbers from 1 to 100 (inclusive)

```java
import java.util.Arrays
```
```java
System.out.println(Arrays.toString(generateArray1to100(8)));
System.out.println(Arrays.toString(generateArray1to100(5)));
System.out.println(Arrays.toString(generateArray1to100(12)));
```
- Problem 2: Using the array of random numbers generator from Problem 1, print out the smallest even and odd number, and the largest even and odd number.
    - This problem may be a bit tricky. It is different from a standard find the smallest/largest problem. But a hint that may help is that the array from problem 1 is always numbers from 1 to 100.
    - Think about edge cases! If you aren't sure about it, just ask.

```java
int[] array = generateArray1to100(20);
System.out.println(Arrays.toString(array));
minMaxOddEven(array);
```
```
minEven: 8
maxEven: 96
minOdd: 13
maxOdd: 95
```