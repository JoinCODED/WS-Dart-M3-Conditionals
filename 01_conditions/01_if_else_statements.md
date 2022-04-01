In this and upcoming lessons, we will learn about conditionals in dart, which allows us to write code to make decisions based on some conditions.

Suppose you have an airplane tickets program, and you want to sell the ticket based on those conditions:

If the age is less than 18 you will charge 10KWD for the ticket

otherwise, if the age is more or equal to 60 you will charge 12KWD for the ticket

otherwise the ticket is worth 14KWD.

Let's see how to code that in dart:

```dart
void main() {
    const age = 15;
    if (age<18) {
        print("Price is 10KWD");
    }
}
```

To digest what we wrote above, we start an `if` condition, with the `if` keyword, and within parenthesis we write our condition that once it's evaluated and results with a `true` value, the code will execute what's in the curly braces and it will print:

Output:

```
Price is 10KWD
```

And if we tried to change the `age` to `25` the evaluation of our condition will resolve to `false`, which means the code within the curly braces will not execute:

```dart
void main() {
    const age = 25;
    if (age<18) {
        print("Price is 10KWD");
    }
}
```

Output:

```

```

To translate the `otherwise` to code:

```dart
void main() {
    const age = 65;
    if (age < 18) {
        print("Price is 10KWD");
    } else if (age >= 60) {
        print("Price is 12KWD");
    }
}
```

In the code above, we wrote `else if` followed by another condition in a set of parenthesis and within the curly bracers we wrote what code we want to execute `if` the condition resolves to `true`.

So our program flow will be like this:

Dart: I have an integer called `age` with the value of `65`, if `65` is less than `18` I should print `Price is 10KWD` so i will ignore this block of code and I'll check the other condition, if `65` is bigger than `60` i should print `Price is 12KWD`. and it's true, `65` is more than `60`, so i will output:

```
Price is 12KWD
```

And you can set infinite amount of conditions as long as the first condition starts with `if` and every condition after it starts with `else if`.

Finally we need to handle the case of age being between 18 and 60.

```dart
void main() {
    const age = 25;
    if (age < 18) {
        print("Price is 10KWD");
    } else if (age > 60) {
        print("Price is 12KWD");
    } else if (age >= 18 && age < 60) {
        print("Price is 14KWD");
    }
}
```

But do we need to do this? we only have 3 possible conditions:

1. age is less than 18
2. age is more or equal to 60
3. age is equal or more to 18 and less than 65

The `else` keyword means if no condition is met, do what is within the curly braces, so if we wrote this:

```dart
void main() {
    const age = 25;
    if (age < 18) {
        print("Price is 10KWD");
    } else if (age > 60) {
        print("Price is 12KWD");
    } else {
        print("Price is 14KWD");
    }
}
```

You can see the output is correct, that's because `else` will cover the last condition we had.
