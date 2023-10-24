> Week 9 Practice Problems<br>[Topic: Objects and Classes]

<hr>

- Problem 1: What is the output?

```java
public class Main {
    public static void main(String[] args) {
        Halloween you = new Halloween();
        you.buyCandy(50);
        for (int i = 1; i <= 5; i++) {
            you.giveCandy(i);
        }
        System.out.printf("I end the night with %d piece(s) of candy.%n", you.getCandy());
    }
}

public class Halloween {
    private int candy;

    public Halloween() {
        this.candy = 0;
    }

    public Halloween(int candy) {
        this.candy = candy;
    }

    public int getCandy() {
        return this.candy;
    }

    public int buyCandy(int amount) {
        if (amount < 0) {
            System.out.println("Silly you, you can't buy negative pieces of candy :)");
        } else {
            System.out.printf("You went out and bought %d piece(s) of candy.%n", amount);
            this.candy = this.candy + amount;
        }

        return this.candy;
    }

    public int giveCandy(int amount) {
        if (amount < 0) {
            System.out.println("Silly you, you can't give negative pieces of candy :)");
        } else {
            System.out.printf("You gave out %d piece(s) of candy.%n", amount);
            this.candy = this.candy - amount;
        }

        return this.candy;
    }

    public void trickOrTreat(boolean treat) {
        if (treat) {
            System.out.printf("Here are %d pieces of candy!%n", 5);

        } else {
            System.out.printf("You have been tricked and had %d pieces of candy stolen from you :(%n", 2);
        }
    }
}
```

- Problem 2: Complete the coin machine class.

```java
public class Main {
    public static void main(String[] args) {
        CoinMachine cm = new CoinMachine(50, 50, 50, 50);

        cm.giveChange(50.00, 49.99);
        cm.giveChange(35.00, 27.99);
        cm.giveChange(32.00, 25.00);
        cm.giveChange(1.23, 0.95);
        cm.giveChange(0.75, 0.55);
        cm.giveChange(33.33, 27.75);
        cm.giveChange(0.92, 0.50);
        cm.inStorage();
    }
}

public class CoinMachine {
    private int quarter;
    private int dime;
    private int nickel;
    private int penny;

    public CoinMachine() {
        this.quarter = 0;
        this.dime = 0;
        this.nickel = 0;
        this.penny = 0;
    }

    public CoinMachine(int quarter, int dime, int nickel, int penny) {
        this.quarter = quarter;
        this.dime = dime;
        this.nickel = nickel;
        this.penny = penny;
    }

    private double round(double amount) {
        return Math.round(amount * 100) / 100.0;
    }

    public void giveChange(double payment, double price) {
        if (payment < price) {
            System.out.println("Customer did not pay enough.");
            return;
        }

        // keep count of amount of each coin that is going to be given to the user
        int q = 0;
        int d = 0;
        int n = 0;
        int p = 0;

        // payment - how much the user pays
        // price   - their total for the purchase
        // TODO: implement this
        double change = this.round(payment - price);

    }

    public void inStorage() {
        System.out.printf("%-10s%d%n", "25¢", this.quarter);
        System.out.printf("%-10s%d%n", "10¢", this.dime);
        System.out.printf("%-10s%d%n", "5¢", this.nickel);
        System.out.printf("%-10s%d%n", "1¢", this.penny);
    }

    public void addQuarter(int count) {
        if (count < 0) {
            System.out.println("Negative not allowed.");
        } else {
            this.quarter = this.quarter + count;
        }
    }

    public void addDime(int count) {
        if (count < 0) {
            System.out.println("Negative not allowed.");
        } else {
            this.dime = this.dime + count;
        }
    }

    public void addNickel(int count) {
        if (count < 0) {
            System.out.println("Negative not allowed.");
        } else {
            this.nickel = this.nickel + count;
        }
    }

    public void addPenny(int count) {
        if (count < 0) {
            System.out.println("Negative not allowed.");
        } else {
            this.penny = this.penny + count;
        }
    }
}
```
Expected Output
```
Coins used:
0 Quarter(s)
0 Dime(s)
0 Nickel(s)
1 Penny(s)
Coins used:
28 Quarter(s)
0 Dime(s)
0 Nickel(s)
1 Penny(s)
Coins used:
22 Quarter(s)
15 Dime(s)
0 Nickel(s)
0 Penny(s)
Coins used:
0 Quarter(s)
2 Dime(s)
1 Nickel(s)
3 Penny(s)
Coins used:
0 Quarter(s)
2 Dime(s)
0 Nickel(s)
0 Penny(s)
Coins used:
0 Quarter(s)
31 Dime(s)
49 Nickel(s)
3 Penny(s)
Coins used:
0 Quarter(s)
0 Dime(s)
0 Nickel(s)
42 Penny(s)
25¢       0
10¢       0
5¢        0
1¢        0
```