1. Your main method should look like this:

```dart
void main() {
  String fullName = " John doe";
}
```

2. Print out the output using string interpolation:

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName} and my last name length is ${fullName}")
}
```

3. To get only ` John` out of ` John doe` we will use the `subString` method, let's count the starting point and the ending point, we will start from the index `0` and count: white space :0, J :1, o :2, h :3, n :4

And for substring we provide the end point as **To but not including** so the end point would be `5`.

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName.subString(0,5)} and my last name length is ${fullName}")
}
```

output:

```
My name is  John and my last name length is John doe
```

4. Next, we will use the `toUpperCase()` method and chaining:

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName.subString(0,5).toUpperCase()} and my last name length is ${fullName}")
}
```

output:

```
My name is  JOHN and my last name length is John doe
```

5. Now for the last name, we will use `subString()` method again from the index of `6` which is the index of the letter `d` and we won't provide a second argument and that means the end point is the last index of the given string:

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName.subString(0,5).toUpperCase()} and my last name length is ${fullName.subString(6)}")
}
```

output:

```
My name is  JOHN and my last name length is doe
```

6. To get a length of a string we use the `length` method:

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName.subString(0,5).toUpperCase()} and my last name length is ${fullName.subString(6).length}")
}
```

output:

```
My name is  JOHN and my last name length is 3
```

### 🍋 White Spaces

The method we gonna use is the `trim()` method which removes white spaces in the beginning and the end of a string:

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName.subString(0,5).toUpperCase().trim()} and my last name length is ${fullName.subString(6).length}")
}
```

output:

```
My name is JOHN and my last name length is 3
```

### 🌶 Does My Last Name Starts With The Letter d?

The method to use here is `startsWith` method which returns true or false:

```dart
void main() {
  String fullName = " John doe";

  print("My name is ${fullName.subString(0,5).toUpperCase().trim()} and my last name length is ${fullName.subString(6).length}")
  print(fullName.substring(6).startsWith("d"));
}
```

output:

```
My name is JOHN and my last name length is 3
true
```

# Another solution

```dart
void main() {
String fullName = " John doe";
String firstName = fullName.substring(0,5);
String lastName = fullName.substring(6);
print("My name is ${firstName.toUpperCase().trim()} and my last name length is ${lastName.length}");
print(lastName.startsWith("d"));
}
```
