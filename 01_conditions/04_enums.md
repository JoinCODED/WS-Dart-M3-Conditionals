Enums stands for `enumeration`. Let's see how it works:

In our previous code, we had some integers from 1 to 7 that represent the days of the week. We can make our code more readable, carry more meaning, and explicitly define allowed values, we don't want a user to try to enter that 8th day of the week!

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

Outside the main method, we will define an `enum` by using the keyword `enum` followed by the name of our `enum` in `PascalCase`:

```dart
enum Day {

}
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

Then, we start filling the possible values of this `enum`:

```dart
enum Day {
    sunday,
    monday,
    tuesday,
    wednesday,
    thursday,
    friday,
    saturday
}
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

What we did above is not just defining an `enum`, we actually defined a new `type` of dart. Remember the types `String`, `int`, and `double`? We just created one called `Day`.

We use this type as we did with the other types:

```dart
void main(){
    Day today = Day.sunday
}
```

When you type `Day.`, you will start seeing a dropdown with all the possible values of this `enum`.

Let's use this enum in our `switch` statement:

```dart
enum Day {
    sunday,
    monday,
    tuesday,
    wednesday,
    thursday,
    friday,
    saturday
}
void main() {
    Day today = Day.sunday;
    switch (today) {
        case Day.sunday:
            print("Sunday");
        break;
        case Day.monday:
            print("Monday");
        break;
        case Day.tuesday:
            print("Tuesday");
        break;
        case Day.wednesday:
            print("Wednesday");
        break;
        case Day.thursday:
            print("Thursday");
        break;
        case Day.friday:
            print("Prayer time!");
        break;
        case Day.saturday:
            print("Saturday");
        break;
    }
}
```

When you find yourself needing a `pre-defined` set of values, consider declaring an `enum` type.
