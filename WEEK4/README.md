> Week 4 Practice Problems<br>[Topic: Arrays && Loops]

<hr>

- Problem 1: Create a method that takes in an array and squares each element in the array.
- Pre-problem 2: What will the average method return? No IDE, calculate by hand (or with a calculator) before attempting Problem 2.
- Problem 2: Create a method that takes the array from Problem 1, and calculate the average.

```java
import java.util.Arrays;
```
```java
// Problem 1 Test Case
int[] array = {7, 1, 4, 9, 18, 72, 36, 65};
squareUp(array);
System.out.println(Arrays.toString(array));
// [49, 1, 16, 81, 324, 5184, 1296, 4225]

// Problem 2 Test Case
System.out.println(average(array));
```