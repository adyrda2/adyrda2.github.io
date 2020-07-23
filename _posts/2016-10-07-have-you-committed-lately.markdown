---
layout: post
title: Value vs Reference Types
date:   2020-23-07
categories: iOS, Swift
location:
tags: iOS, Swift
---

**Value Types** usually represented as a struct, enum, or tuple are types that keep a unique copy of its data.
For example, let's create a `Home` struct, and create an instance of it below in a variable called `summerHome`. Next we assign that instance to another property called `floridaHome` and change it's `name` property. Notice the name property of `floridaHome` changes, but becuase it contains a unique copy of that instance, the `name` property of `summerHome` does not change.

```
struct Home {
  var name: String
}

var summerHome = Home(name: "Summer Home")
var floridaHome = summerHome
floridaHome.name = "Florida Home"
floridaHome.name //"Florida Home"
summerHome.name //"Summer Home"
```

**Reference types**, usually represented as a class on the otherhand, share a single copy of the data.
The example below defines a `Person` class, and an instance of a person in a variable named `joe` has been created. When we assign this instance to another variable named `john` and change it's name property to `John`, the name property of `joe` also changes because they point to the same instance.

```
class Person {
  var name: String
  var age: Int
  
  init(name: String, age: Int) {
    self.name = name
    self.age = age
  }
}

var joe = Person(name: "Joe", age: 24)
var john = joe
john.name = "John"
john.name //"John"
joe.name //"John"
```
