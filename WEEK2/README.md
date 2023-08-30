> Week 2 Practice Problems

For this week, you will be tested on materials that you should have learned in CSC 101. I understand that you might not have gotten to cover everything from CSC 101, so do the best you can and get as far as you can.

- Problem 1: Create a method that takes 2 integers, and returns the sum of the absolute value of both integers.

```java
System.out.println(absoluteAdd(-5, -7)); // 12
System.out.println(absoluteAdd(6, -2)); // 8
System.out.println(absoluteAdd(-3, 1)); // 4
System.out.println(absoluteAdd(9, 4)); // 13
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
- Problem 3: Create a method that takes 2 integers, print out the numbers from the first number to the second number changing by a count of 1.
    - Don't worry about how the output looks. As long as the numbers are printed in the right order.

```java
countingByOne(10, 5); // 10, 9, 8, 7, 6, 5
countingByOne(12, 19); // 12, 13, 14, 15, 16, 17, 18, 19
countingByOne(1, 1); // 1
```