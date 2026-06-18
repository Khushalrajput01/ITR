# JavaScript Day 13–16 — Factory Functions, Prototypes & Memory Optimization

---

# Topics Covered

* Object Literal Problem
* Factory Functions
* Memory Duplication Issue
* Shared Method Objects
* `Object.create()`
* Prototype Chain
* Prototypal Factory Functions
* Object Introspection

---

# 1. Object Literal Problem

Creating objects manually becomes repetitive and difficult to maintain.

```javascript
const user1 = {
    firstName: "Yatin",
    age: 24
};

const user2 = {
    firstName: "Siddesh",
    age: 22
};
```

### Problems

* Repeated code
* Hard to maintain
* Poor scalability

---

# 2. Factory Functions

Factory functions automate object creation.

```javascript
function createUser(firstName, lastName, email, age, address) {

    const user = {};

    user.firstName = firstName;
    user.lastName = lastName;
    user.email = email;
    user.age = age;
    user.address = address;

    user.about = function () {
        return `${this.firstName} is ${this.age} years old`;
    };

    user.is18 = function () {
        return this.age >= 18;
    };

    return user;
}
```

---

## Problem: Memory Duplication

Every object gets its own copy of methods.

```javascript
user1.about !== user2.about;
```

This wastes memory when thousands of objects are created.

---

# 3. Shared Method Store

Methods are stored separately and reused.

```javascript
const userMethods = {

    about() {
        return `${this.firstName} is ${this.age} years old`;
    },

    is18() {
        return this.age >= 18;
    }
};
```

Factory function:

```javascript
user.about = userMethods.about;
user.is18 = userMethods.is18;
```

---

## Advantage

✔ Reduces memory usage

---

## Drawback

Manual assignment becomes difficult as methods increase.

---

# 4. Object.create()

Creates objects with prototype linkage.

```javascript
const user = Object.create(userMethods);
```

Now JavaScript automatically searches methods inside `userMethods`.

---

## Example

```javascript
const userMethods = {

    about() {
        return `${this.firstName}`;
    },

    is18() {
        return this.age >= 18;
    }

};
```

```javascript
function createUser(firstName, age) {

    const user = Object.create(userMethods);

    user.firstName = firstName;
    user.age = age;

    return user;
}
```

---

# 5. Prototype Chain

```text
user
 ↓
userMethods
 ↓
Object.prototype
 ↓
null
```

JavaScript searches properties from top to bottom.

---

# 6. Prototypal Lookup

If a property is missing inside the object:

```javascript
user.about()
```

JavaScript searches:

1. Current object
2. Prototype object
3. Object.prototype
4. null

---

# 7. Object Introspection

### Get Prototype

```javascript
Object.getPrototypeOf(user);
```

---

### Check Own Properties

```javascript
user.hasOwnProperty("firstName");
```

---

### Compare References

```javascript
user1.about === user2.about;
```

Output:

```javascript
true
```

Both objects share the same method.

---

# Architecture Evolution

## Stage 1

Object Literals

```text
Manual Objects
```

↓

## Stage 2

Factory Functions

```text
Reusable Object Creation
```

↓

## Stage 3

Shared Method Objects

```text
Reduced Memory Usage
```

↓

## Stage 4

Object.create()

```text
Automatic Prototype Lookup
```

↓

## Stage 5

Constructor Functions & Prototypes

```text
Modern Efficient Architecture
```

---

# Key Concepts

| Concept                 | Purpose                    |
| ----------------------- | -------------------------- |
| Factory Function        | Create objects dynamically |
| Shared Methods          | Avoid duplicate functions  |
| Object.create()         | Prototype linking          |
| Prototype Chain         | Property lookup mechanism  |
| Object.getPrototypeOf() | Inspect prototype          |
| hasOwnProperty()        | Check own properties       |
| Method Sharing          | Memory optimization        |

---

# Quick Revision

✅ Factory functions create objects dynamically.

✅ Methods inside factory functions create memory duplication.

✅ Shared method objects reduce memory usage.

✅ `Object.create()` establishes prototype linkage.

✅ JavaScript searches properties through the prototype chain.

✅ `Object.getPrototypeOf()` returns an object's prototype.

✅ `hasOwnProperty()` checks direct properties only.

✅ Shared methods improve performance and memory efficiency.

---

# Learning Flow

```text
Object Literals
      ↓
Factory Functions
      ↓
Shared Methods
      ↓
Object.create()
      ↓
Prototype Chain
      ↓
Constructor Functions
      ↓
Classes
```
