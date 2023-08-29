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
```java
public static int[] generateArray1to100(int a) {
    int[] arr = new int[a];
    
    for (int i = 0; i < a; i++) {
        arr[i] = 1 + (int) (Math.random() * 100);
    }
    
    return arr;
}
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
```java
public static void minMaxOddEven(int[] arr) {
    int minOdd = 0;
    int minEven = 0;
    int maxOdd = 0;
    int maxEven = 0;
    
    for (int i = 0; i < arr.length; i++) {
        if (arr[i] % 2 == 0) {
            if (minEven == 0) {
                minEven = arr[i];
                maxEven = arr[i];
            } else {
                if (arr[i] > maxEven) {
                    maxEven = arr[i];
                }
                if (arr[i] < minEven) {
                    minEven = arr[i];
                }
            }
        } else {
            if (minOdd == 0) {
                minOdd = arr[i];
                maxOdd = arr[i];
            } else {
                if (arr[i] > maxOdd) {
                    maxOdd = arr[i];
                }
                if (arr[i] < minOdd) {
                    minOdd = arr[i];
                }
            }
        }
    }
    
    if (minEven == 0) {
        System.out.println("minEven: None");
        System.out.println("maxEven: None");
    } else {
        System.out.println("minEven: " + minEven);
        System.out.println("maxEven: " + maxEven);
    }
    
    if (minOdd == 0) {
        System.out.println("minOdd: None");
        System.out.println("maxOdd: None");
    } else {
        System.out.println("minOdd: " + minOdd);
        System.out.println("maxOdd: " + maxOdd);
    }
}
```