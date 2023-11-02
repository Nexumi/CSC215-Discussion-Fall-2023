> Week 11 Practice Problems<br>[Topic: HAS-A]

<hr>

- Problem 1: What is the output of this code.

```java
public class Main {
    public static void main(String[] args) {
        A a = new A(17);
        B b = a.riddle();
        b.answer();
    }
}

public class A {
    private B b;
    private int c;

    public A() {
    }

    public A(int c) {
        this.b = new B(c);
        this.c = c * 2;
    }

    public B riddle() {
        System.out.println("My number is twice that of the other number.");
        System.out.println("Added together, our sum is " + (this.c + this.b.getC()) + ".");
        System.out.println("What are our numbers?");
        return this.b;
    }
}

public class B {
    private int c;
    
    public B() {
    }

    public B(int c) {
        this.c = c;
    }
    
    public int getC() {
        return this.c;
    }

    public void answer() {
        System.out.println("Our numbers are " + this.c + " and " + this.c * 2 + ".");
    }
}
```