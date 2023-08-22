<style> h1 { display: none; } </style>

> CSC215: Discussion Week 1

For this week, you will be tested on materials that you should have learned in CSC 101. I understand that you might not have gotten to cover everything from CSC 101, so do the best you can and get as far as you can.

- Problem 1: Create a method that takes 2 integers, and returns the sum of the absolute value of both integers.

```java
System.out.println(absoluteAdd(-5, -7)); // 12
System.out.println(absoluteAdd(6, -2)); // 8
System.out.println(absoluteAdd(-3, 1)); // 4
System.out.println(absoluteAdd(9, 4)); // 13
```
```java
public static int absoluteAdd(int a, int b) {
    return Math.abs(a) + Math.abs(b);
}
```
- Problem 2: What will get printed onto the console? No IDE!

```java
public class NestedMysteryCode {
    public static void main(String[] args) {
        nestedMysteryCode(5, 10, 3);
        nestedMysteryCode(7, 2, 7);
        nestedMysteryCode(4, 4, 4);
    }

    public static void nestedMysteryCode(int a, int b, int c) {
        if (a > b) {
            if (b < c) {
                System.out.println("Case 1");
            } else {
                System.out.println("Case 2");
            }
        } else if (a < b) {
            if (b > c) {
                if (c != 0) {
                    System.out.println("Case 3");
                } else {
                    System.out.println("Case 4");
                }
            } else if (b == c) {
                if (a >= 0) {
                    System.out.println("Case 5");
                } else {
                    System.out.println("Case 6");
                }
            } else {
                System.out.println("Case 7");
            }
        } else {
            if (b == c) {
                System.out.println("Case 8");
            } else if (b > c) {
                if (a % 2 == 0) {
                    System.out.println("Case 9");
                } else {
                    System.out.println("Case 10");
                }
            } else {
                if (c > 0) {
                    System.out.println("Case 11");
                } else {
                    System.out.println("Case 12");
                }
            }
        }
    }
}
```
```
Case 3
Case 1
Case 8
```
- Problem 3: Create a method that takes 2 integers, print out the numbers from the first number to the second number changing by a count of 1.

```java
countDown(10, 5); // 10, 9, 8, 7, 6, 5
countDown(12, 19); // 12, 13, 14, 15, 16, 17, 18, 19
countDown(1, 1); // 1
```
```java
public static void countDown(int a, int b) {
    if (a > b) {
        for (int i = a; i > b; i--) {
            System.out.print(i + ", ");
        }
        System.out.println(b);
    } else {
        for (int i = a; i < b; i++) {
            System.out.print(i + ", ");
        }
        System.out.println(b);
    }
}
```
- Problem 4: Create a method that takes in an integer and generates an integer array of that size, filled with random numbers from 1 to 100 (inclusive)

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
- Problem 5: Using the random number generator from Problem 3, print out the smallest even and odd number, and the largest even and odd number.
    - This problem may be a bit tricky. It is different from a standard find the smallest/largest problem. But a hint that may help is that the array from problem 3 is always numbers from 1 to 100.
    - Think about edge cases! If you aren't sure about it, just ask.

```java
int[] array = generateArray1to100(20);
System.out.println(Arrays.toString(array));
minMaxOddEven(array);
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