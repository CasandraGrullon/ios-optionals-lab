# Optionals lab

Fork and clone this repo. On your fork, answer and commit the follow questions. When you are finished, submit the link to your repo on Canvas.


## Question 1

a. Given the variable `userNameOne` below, print *"The username is Test User"*.  Use *Optional Binding* (`if let`) to print the name.

```swift
var userNameOne: String? = "Test User"
```
Answer:
```swift
if let validUserName = userNameOne {
    print("The username is \(validUserName)")
}
```

b. Given the variable `userNameTwo` below, print *"The username is undefined"*.  Use the *nil coalescing operator* (`??`).

```swift
var userNameTwo: String? = nil
```
Answer:
```swift
let usernameInput = userNameTwo ?? "undefined"
print("the username is \(usernameInput)")
```

## Question 2

a. Given the variables `rectOneWidth` and `rectOneHeight` below, print "The area of rectOne is 50".  Use *Optional Binding* (`if let`) to print the area.

```swift
var rectOneWidth: Double? = 5
var rectOneHeight: Double? = 10
```
Answer:
```swift
if let height = rectOneHeight, let width = rectOneWidth {
        area += (height * width)
    }
print("The area of rectOne is \(area)")
```

b. Given the variables `rectTwoWidth` and `rectTwoHeight` below, print "The are of rectTwo is not able to be calculated".  Use *Optional Binding* (`if let`) to print this message.

```swift
var rectTwoWidth: Double? = nil
var rectTwoHeight: Double? = nil
```

## Question 3

a. Given the variables `userOneName`, `userOneAge`, and `userOneHeight` below, write code that prints "Hello Anne!  You are 15 years old and 5.8 feet tall" (1 foot = 12 inches).  Use optional binding.


```swift
var userOneName: String? = "Anne"
var userOneAge: Int? = 15
var userOneHeight: Double? = 70
```
Answer:
```swift
if let height = userOneHeight, let age = userOneAge, let name = userOneName {
    //heightInFeet += (height / 12.0).rounded()
    let formattedHeight = String(format: "%.1f", height / 12)
    print("Hello \(name)! You are \(age) years old and \(formattedHeight) feet tall")
}
```

b. Given the variables `userTwoName`, `userTwoAge` and `userTwoHeight` below, write code that prints "Hello user!  You are 15 years old and I don't know how tall you are".  Use optional binding

```swift
var userTwoName: String? = nil
var userTwoAge: Int? = 15
var userTwoHeight: Double? = nil
```
Answer:
```swift
if let height = userTwoHeight, let age = userTwoAge, let name = userTwoName {
    print("Hello \(name)! You are \(age) years old and \(height) feet tall")
} else {
    print("Hello user! You are 15 years old and I don't know how tall you are...")
}
```

## Question 4

Give the variable `favoriteNumber`, write code that either prints "Your favorite number is " followed by the number, or "I don't know what your favorite number is"

`favoriteNumber` is of type Int? and will either be `nil` or a random number between 0 and 10.  It will change each time you run your Playground.

```swift
var favoriteNumber = Bool.random() ? Int.random(in: 0...10) : nil
```
Answer:
```swift
if let num = favoriteNumber {
    print("Your favorite number is \(num)")
} else {
    print("I don't know what your favoite number is...")
}
```


## Question 5

Given the variables `numOne`, `numTwo` and `numThree`, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numOne = Bool.random() ? Int.random(in: 0...10) : nil
var numTwo = Bool.random() ? Int.random(in: 0...10) : nil
var numThree = Bool.random() ? Int.random(in: 0...10) : nil
```
Answer:
```swift
var sumOfNum123 = (numOne ?? 0) + (numTwo ?? 0) + (numThree ?? 0)
```
## Question 6

a. Given the variable `numbers` below, write code that prints "The sum of all the numbers is " followed by their sum.  If a number is `nil`, don't add it to the sum.  If all numbers are `nil`, the sum is zero.

```swift
var numbers = [Int?]()

for _ in 0..<10 {
    numbers.append(Bool.random() ? Int.random(in: 0...100) : nil)
}
```
Answer: 
```swift
var sumofSomeNumber = 0

for num in numberZ {
    if let someNumber = num {
    sumofSomeNumber += someNumber
    }
}
print(sumofSomeNumber)
```
b. Using the same variable, find the average of all non-nil values.

## Extra Questions

https://github.com/joinpursuit/Pursuit-Core-iOS-Extra-Optionals-Questions/blob/master/README.md
