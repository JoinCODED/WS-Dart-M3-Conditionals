There's one more way to write an `if` `else` statement that is short and concise:

```dart
void main(){
const age = 28;
age > 18 ? print("You are older than 18") : print("You are younger than 18");
}
```

It's a weird syntax but got the job done with one line of code.
Let's explain it:

We started by the condition, and in this case, it was `age > 18`.

Then, we used a question mark `?`, and after it, we wrote the code that we want to execute if the condition is met.

Next, we used `:`, followed by the code that we want to execute if the condition is **not** met.
