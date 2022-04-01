There's one more way to write an `if` `else` statement that is short and concise:

```dart
void main(){
const age = 28;
age > 18 ? print("You are older than 18") : print("You are younger than 18");
}
```

A weird syntax, but got the job done with one line of code, so let's explain it:

We start by the condition, and this case it was `age > 18`.

Then we use a question mark `?` and after it we write what code to execute if the condition is met.

Then we use `:` and after it we write what code to execute if the condition is **not** met.
