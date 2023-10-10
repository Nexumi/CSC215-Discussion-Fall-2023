> Week 8 Practice Problems<br>[Topic: Objects]

<hr>

- Problem 1: What is the output of this code?

```java
import java.util.Arrays;
public class Main {
    public static int firstMethod(int[] arr, int x) {
        int z = 0;
        for (int i = 0; i < arr.length; i++) {
            z = z + arr[i] * x;
        }
        return z;
    }

    public static String secondMethod(int x, String str) {
        String s = "";
        for (int i = 0; i < x; i++) {
            s = s + str;
        }
        return s;
    }

    public static double[] thirdMethod(int x) {
        double[] arr = new double[x];
        for (int i = 0; i < x; i++) {
            arr[i] = x;
        }
        return arr;
    }

    public static void finalMethod(int x, String str, double[] arr) {
        System.out.printf("%d     %s     %s", x, str, Arrays.toString(arr));
    }

    public static void main(String[] args) {
        finalMethod(firstMethod(new int[]{5, 7, 35, 52}, 3), secondMethod(3, "xyz"), thirdMethod(5));
    }
}
```
```
297     xyzxyzxyz     [0, 5, 10, 15, 20]
```

- Problem 2: Create a method that generates a random String of length 6, using only 0-9 and a-f, then add `0x` in front of it. Also generate a random number from 1 to 16777215.
    - Fun fact: `0xfa12ce` is what we call a hexadecimal number.

```java
public static void main(String[] args) {
    Object[] numbers = generateRandomNumbers();
    String hex = (String) numbers[0];
    int dec = (int) numbers[1];
    System.out.printf("Random Hexadecimal Number: %s%n", hex);
    System.out.printf("Random Decimal Number: %d%n", dec);
}
```
```java
public static Object[] generateRandomNumbers() {
    Random rand = new Random();
    String hex = "0x";
    for (int i = 0; i < 6; i++) {
        char digit;
        if (rand.nextInt(2) == 0) {
            digit = (char) (rand.nextInt(10) + 48);
        } else {
            digit = (char) (rand.nextInt(6) + 97);
        }
        hex = hex + digit;
    }
    return new Object[]{hex, rand.nextInt(16777215) + 1};
}
```