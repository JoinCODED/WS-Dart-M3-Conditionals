Suppose you have the following code:

```dart
void main() {
    const day = 1;
    if (day == 1){
        print("Sunday");
    } else if (day == 2){
        print("Monday");
    } else if (day == 3){
        print("Tuesday");
    } else if (day == 4){
        print("Wednesday");
    } else if (day == 5){
        print("Thursday");
    } else if (day == 6){
        print("Friday");
    } else {
        print("Saturday");
    }
}
```

As you can see, to write this logic, we need a lot of `if else` statements.

Instead, we can rewrite this logic using a `switch` statement:

```dart
void main() {
    const day = 1;
    switch (day) {

    }
}
```

We start by adding the `switch` keyword, and within parentheses, we place the variable that we want to check. In our case, we need to check the value of `day`.

Then, we open a set of curly braces and we start listing our cases:

```dart
void main() {
    const day = 1;
    switch (day) {
        case 1:
            print("Sunday");
        break;
    }
}
```

We added our first `case`, by writing the `case` keyword followed by the value that `if` matched, it will execute the code below it.

Then, we wrote the `break` keyword to ensure that we exited the `switch` statement.

Let's add the rest of our cases:

```dart
void main() {
    const day = 1;
    switch (day) {
        case 1:
            print("Sunday");
        break;
        case 2:
            print("Monday");
        break;
        case 3:
            print("Tuesday");
        break;
        case 4:
            print("Wednesday");
        break;
        case 5:
            print("Friday");
        break;
        case 6:
            print("Sunday");
        break;
    }
}
```

Like we have `else` to take care of the rest of the conditions, we have `default` in `switch` statements:

```dart
void main() {
    const day = 1;
    switch (day) {
        case 1:
            print("Sunday");
        break;
        case 2:
            print("Monday");
        break;
        case 3:
            print("Tuesday");
        break;
        case 4:
            print("Wednesday");
        break;
        case 5:
            print("Friday");
        break;
        case 6:
            print("Sunday");
        break;
        default:
            print("Saturday");
        break;
    }
}
```

Run the code. As you can see, it works similarly to our previous `if` statement.
