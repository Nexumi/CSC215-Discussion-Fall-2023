> Week 6 Practice Problems<br>[Topic: Arrays]

<hr>

- Problem 1: Create a method that takes in a string array. Then print out all words that are of length 6 or more.

```java
String[] words = {
	"apple", "banana", "cherry", "dog", "elephant", "fish",
	"grape", "hat", "igloo", "jacket", "kangaroo",
	"lemon", "monkey", "noodle", "orange", "penguin",
	"quilt", "rabbit", "snake", "tiger", "umbrella",
	"vanilla", "watermelon", "xylophone", "yogurt", "zebra",
	"sun", "moon", "star", "flower", "ocean", "mountain",
	"river", "cloud", "rain", "snow", "fire", "earth",
	"wind", "volcano", "island", "desert", "forest",
	"castle", "dragon", "knight", "princess", "wizard",
	"unicorn"
};
```

- Problem 2: Create a method that takes in a 2D string array. Then print out all words that are of length 6 or more.

```java
String[][] words2D = {
    {"apple", "banana", "cherry"},
    {"dog"},
    {"elephant", "fish", "grape", "hat"},
    {"igloo", "jacket", "kangaroo"},
    {"lemon", "monkey"},
    {"noodle"},
    {"orange", "penguin", "quilt", "rabbit", "snake"},
    {"tiger", "umbrella", "vanilla", "watermelon", "xylophone"},
    {"yogurt", "zebra"},
    {"sun", "moon", "star", "flower"},
    {"ocean"},
    {"mountain", "river", "cloud", "rain"},
    {"snow"},
    {"fire", "earth", "wind", "volcano", "island"},
    {"desert", "forest", "castle", "dragon", "knight"},
    {"princess", "wizard"},
    {"unicorn"}
};
```

<u>Expected Out For Both Problems</u>

```
banana
cherry
elephant
igloo
jacket
kangaroo
monkey
noodle
orange
penguin
rabbit
umbrella
vanilla
watermelon
xylophone
yogurtflower
mountain
volcano
island
desert
forestcastle
dragon
knight
princesswizard
unicorn
```