In this lesson and the upcoming lessons, we will learn about conditionals in Dart. Conditionals allow us to write code to make decisions based on some conditions.

Suppose that you have an airplane tickets program, and you want to sell the ticket based on the following conditions:

If the age is less than 18, you will charge 10 KWD for the ticket.

If the age is more than or equal to 60, you will charge 12 KWD for the ticket.

Otherwise the ticket is worth 14 KWD.

Let's see how to code that in Dart:

```dart
void main() {
    const age = 15;
    if (age<18) {
        print("Price is 10 KWD");
    }
}
```

To digest what we wrote above, we start an `if` condition with the `if` keyword. we write our conditions between parentheses, once they're evaluated and result with a `true` value, the code will execute what's in the curly braces and it will print:

Output:

```
Price is 10KWD
```

If we tried to change the `age` to `25`, the evaluation of our condition will resolve to `false`, which means the code within the curly braces won't be executed:

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

To translate the `otherwise` to a code:

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

In the code above, we wrote `else if` followed by another condition in a set of parentheses, and between the curly bracers we wrote the code we want to execute `if` the condition resolves to `true`.

Our program flow will be as follows:

Dart: I have an integer called `age` with the value of `65`, if `65` is less than `18` I should print `Price is 10KWD`. If it's not, I will ignore this block of code and I'll check the other condition. If `65` is bigger than `60`, I should print `Price is 12KWD`. In our case, `65` is bigger than `60`, so I will output:

```
Price is 12KWD
```

You can set an infinite amount of conditions as long as the first condition starts with `if`, and every condition after starts with `else if`.

Finally, we need to handle the case of age being between 18 and 60.

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

1. Age is less than 18.
2. Age is more than or equal to 60.
3. Age is equal to or more than 18 and less than 65.

The `else` keyword means if no condition is met, do what is within the curly braces, so if we wrote the following conditions:

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

You can see correct output, that's because `else` will cover the last condition we had.
