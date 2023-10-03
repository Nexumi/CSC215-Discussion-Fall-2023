> Week 7 Practice Problems<br>[Topic: Arrays]

<hr>

- Problem 1: Create a method that takes a 2D array of characters, and prints them out in a grid pattern.
    - Output must match the sample output (spaces between each symbol and a new line for each row)
- Problem 2: What type and what method did I use to create the `symbols2D` array?

```java
char[][] symbols2D = {
    {'!', '@', '#'},
    {'$', '%', '^'},
    {'&', '*', '(', ')'}
}
```
```
! @ #
$ % ^
& * ( )
```

- Problem 3: Create a method that takes a 3D array of characters and print them out as followed.
    - Output must match the sample output (headers for each row, a tab (\t), then the symbols)
    - Hint:
        - Row is the first [2]
        - Each row in the row is the [3]
            - Hence 3 rows
        - The number of symbols per row of each row is the last [2]
- Problem 4: What type and what method did I use to create the `symbols3D` array?

```java
char[][][] symbols3D = new char[2][3][2];
symbols3D[0][0][0] = '!';
symbols3D[0][0][1] = '@';
symbols3D[0][1][0] = '#';
symbols3D[0][1][1] = '$';
symbols3D[0][2][0] = '%';
symbols3D[0][2][1] = '^';
symbols3D[1][0][0] = '&';
symbols3D[1][0][1] = '*';
symbols3D[1][1][0] = '(';
symbols3D[1][1][1] = ')';
symbols3D[1][2][0] = '-';
symbols3D[1][2][1] = '=';
```
```
Row 1:
    ! @
    # $
    % ^
Row 2:
    & *
    ( )
    - =
```