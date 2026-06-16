# Arrays Intro

## Instructions

1. Choose one person in your group to share their screen. They will be in charge
   of typing your answers.
2. Select another person in the group to be responsible for sharing your answers
   with the class later on.
3. As a team, read each question out loud and reach a consensus on the answer before
   moving to the next question.

## Access elements of an array

An **array** is a data type that can hold a _sequence_ of values.

```js
const numbers = [3, 2, 1, 1, 0];
```

| Index   | 0   | 1   | 2   | 3   | 4   |
| ------- | --- | --- | --- | --- | --- |
| Element | 3   | 2   | 1   | 1   | 0   |

1. What **element** is at index 1 of the array?
2. **Bracket notation** is used to access an individual element of an array. For example,
   `numbers[2]` refers to the element at index 2 of `numbers`. How do you access the
   element at index 0 of `numbers`?
3. What is the value of `numbers[4]`?
4. The **length** of an array refers to how many elements it contains.
   At what index is the last element of an array with length 50?

## Access characters of a string

Much like arrays, strings can also be indexed.

```js
const word = "penguin";
```

| Index   | 0   | 1   | 2   | 3   | 4   | 5   | 6   |
| ------- | --- | --- | --- | --- | --- | --- | --- |
| Element | p   | e   | n   | g   | u   | i   | n   |

5. Which character is at index 3 of `word`?
6. What is the value of `word[0]`?
7. At what index is the character "i"?

## Modify array elements

Use a JavaScript REPL to help you answer the following questions.

```js
const numbers = [3, 2, 1, 1, 0];
numbers[0] = 8;
```

8. `numbers[0] = 8` assigns the value 8 to index 0 of the array `numbers`.
   How would you assign the value 15 to index 3 of an array named `foo`?
9. What is the final value of `numbers`?
10. What happens to the original value of `numbers[0]`?

We can use a loop to populate an initially-empty array, as follows.

```js
const badgers = [];
for (let i = 0; i < 10; i++) {
  badgers[i] = "badger";
}
```

11. What will the array `badgers` contain after the loop runs?
12. What is the final length of `badgers`?
13. How would you modify the code so that `badgers` is initialized with 2000 strings?
14. Why would a developer want to use a loop to initialize an array instead of
    **hard-coding** it?

## Iterate through array indexes

```js
const numbers = [0, 1, 1, 2, 3];
let i = 0;
while (i < numbers.length) {
  console.log("i:", i);
  i += 1;
}
```

15. How many times does the while loop run?
16. What does the variable `i` represent?
17. How would you modify the code to print the _elements_ of the array?
18. Rewrite the snippet to use a `for` loop instead.

## Iterate through array elements

**`for..of`** allows us to iterate directly through the elements of an array.

```js
const numbers = [0, 1, 1, 2, 3];
for (const number of numbers) {
  console.log(number);
}
```

19. What variable is used to represent each element of the array?
20. In what situation would a developer _not_ be able to use `for..of` to iterate
    through an array?

> [!TIP]
>
> You can iterate through strings the same way! Either use a regular loop
> through indexes, or use `for..of` to iterate through each character.

## Push and pop

```js
const fruits = ["watermelon", "grape", "cranberry"];
fruits.push("kiwi");
fruits.push("strawberry");
fruits.pop();
fruits.pop();
```

21. Inspect `fruits` as you run each line of code one at a time.
    1. Does `push` add to the front or back of an array?
    2. Does `pop` remove from the front or back of an array?
22. Write code to add "kiwi" to `fruits` _without_ using `push`.
23. Why might a developer prefer to use `push` or `pop` to mutate an array?

## Nest an array inside an array

When the elements of an array are _also_ arrays, it is called a **nested array**.
You may also hear the term "2D array". These may seem intimidating, but we
can use the same techniques we just learned!

```js
const grid = [
  ["X", "-", "O"],
  ["X", "O", "O"],
  ["-", "-", "X"],
  ["O", "X", "X"],
];
```

24. What does `grid.length` evaluate to?
25. What does `grid[0]` evaluate to?
26. What does `grid[0].length` evaluate to?
27. What does `grid[0][1]` evaluate to?
28. What does `grid[3][0]` evaluate to?
29. Write code to assign the value "O" to index 1 of `grid[2]`.
30. Write code to add a new row `["-", "-", "-"]` to the end of `grid`.

## Nest a loop inside a loop

How do you iterate through a nested array? With a nested loop!

```js
for (let i = 0; i < grid.length; i++) {
  for (let j = 0; j < grid[0].length; j++) {
    console.log(i, j, grid[i][j]);
  }
}
```

31. What are the different values of `i` in the **outer** loop?
32. What are the different values of `j` in the **inner** loop?
33. Run the snippet above and examine the output. How would you describe
    the relationship between the outer and inner loops?
