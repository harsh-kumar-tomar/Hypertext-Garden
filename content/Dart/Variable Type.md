[[Dart]]

String 
int
double
num : to store both int and double
bool
var : to store any value



``` dart
const pi = 3.14;
```
## Error

```dart
var myVariable = 50; // You can also use int instead of var
myVariable = "Hello"; // this will give error
print(myVariable);
```

## Dynamic Type

```dart
dynamic myVariable = 50;
myVariable = "Hello";
print(myVariable);
```


## Enum

```dart
enum Weather{ sunny, snowy, cloudy, rainy}
```