> Week 5 Practice Problems<br>[Topic: 101 Review]

<hr>

- Problem 1: Create a method that repeatedly asks the user for an integer, then output the day of the week that number is. 0 is Sunday, 1 is Monday, 2 is Tuesday, etc. End when the user inputs an invalid day of the week.
	- Write 2 methods, one using if/else if/else statements, and another using switch/case statements.
	- If the user inputs something other than 0-7, display something like "Invalid day of the week"

```
Enter a day of the week (0 - 6): 3
3 is Wednesday
Enter a day of the week (0 - 6): 6
6 is Saturday
Enter a day of the week (0 - 7): 15
15 is an invalid day of the week
```
```java
if (day == 0) {
	System.out.println("0 is Sunday");
} else if (day == 1) {
	System.out.println("1 is Monday");
} else if (day == 2) {
	System.out.println("2 is Tuesday");
} else if (day == 3) {
	System.out.println("3 is Wednesday");
} else if (day == 4) {
	System.out.println("4 is Thursday");
} else if (day == 5) {
	System.out.println("5 is Friday");
} else if (day == 6) {
	System.out.println("6 is Saturday");
} else {
	System.out.println(day + " is an invalid day of the week")
}
```
```java
switch (day) {
	case 0:
		System.out.println("0 is Sunday");
		break;
	case 1:
		System.out.println("1 is Monday");
		break;
	case 2:
		System.out.println("2 is Tuesday");
		break;
	case 3:
		System.out.println("3 is Wednesday");
		break;
	case 4:
		System.out.println("4 is Thursday");
		break;
	case 5:
		System.out.println("5 is Friday");
		break;
	case 6:
		System.out.println("6 is Saturday");
		break;
	default:
		System.out.println(day + " is an invalid day of the week")
}
```

- Problem 2: Create a method that repeatedly asks the user for an integer until either 10 numbers are entered or a negative number is entered. Sum up all the numbers entered by the user, excluding the negative number.
	- Write 3 versions, using a different type of loop each time.
		- Loops: While | Do-While | For
```
Enter a number: 6
Enter a number: 9
Enter a number: 1
Enter a number: 5
Enter a number: 3
Enter a number: 7
Enter a number: 6
Enter a number: 8
Enter a number: 4
Enter a number: 3
Sum of all the numbers you entered is 52
```
```
Enter a number: 3
Enter a number: 4
Enter a number: 9
Enter a number: 1
Enter a number: -2
Sum of all the numbers before the negative number is 17
```
```java
import java.util.Scanner;
```
```java
Scanner sc = new Scanner(System.in);

int sum = 0;
for (int i = 0; i < 10; i++) {
	int num = sc.nextInt();
	
	if (num < 0) {
		break;
	}
	
	sum = sum + num; // sum += num;
}
```
```java
Scanner sc = new Scanner(System.in);

int sum = 0;
int i = 0;
while (i < 10) {
	int num = sc.nextInt();

	if (num < 0) {
		break;
	}
	
	sum = sum + num; // sum += num;
	i++;
}
```
```java
Scanner sc = new Scanner(System.in);

int sum = 0;
int i = 0;
do {
	int num = sc.nextInt();

	if (num < 0) {
		break;
	}

	sum = sum + num; // sum += num;
	i++;
} while (i < 10);
```