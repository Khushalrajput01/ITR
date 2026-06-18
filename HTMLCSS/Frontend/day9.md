# JavaScript Day 13 — Array Methods & Useful Concepts

## Topics Covered
- Important Array Methods
- Iterables and Array-Like Objects
- Set and Map
- Optional Chaining
- Object Cloning

---

# 1. forEach()

Executes a callback for each element.

```js
users.forEach((user, index) => {
  console.log(user.firstName, index);
});
```

Does not return a new array.

---

# 2. map()

Creates a new transformed array.

```js
const names = users.map(user => user.firstName);
```

---

# 3. filter()

Returns elements that satisfy a condition.

```js
const evenNumbers = numbers.filter(num => num % 2 === 0);
```

---

# 4. reduce()

Converts an array into one final value.

```js
const total = cart.reduce((sum, item) => sum + item.price, 0);
```

---

# 5. find()

Returns the first matching element.

```js
users.find(user => user.userId === 4);
```

---

# 6. every() and some()

```js
numbers.every(num => num > 0);
numbers.some(num => num % 2 === 0);
```

---

# 7. sort()

```js
numbers.sort((a,b)=>a-b);
```

Mutates the original array.

---

# 8. fill()

```js
numbers.fill(0,3,7);
```

---

# 9. splice()

```js
array.splice(1,2,"A","B");
```

Can insert, delete, and replace values.

---

# Mutating Methods

- sort()
- fill()
- splice()
- push()
- pop()
- shift()
- unshift()

# Non-Mutating Methods

- map()
- filter()
- reduce()
- find()
- some()
- every()
- slice()

---

# Iterables

Examples:

- Strings
- Arrays
- Sets
- Maps

```js
for(let ch of firstName){
 console.log(ch);
}
```

---

# Array-Like Objects

Have:

- length property
- index access

Strings are iterable and array-like.

---

# Set

Stores unique values.

```js
const numbers = new Set([1,2,2,3]);
```

Useful methods:

- add()
- has()
- delete()
- clear()

---

# Map

Stores key-value pairs.

```js
const user = new Map();
user.set("name","Yatin");
```

Keys can be any type.

---

# Optional Chaining

```js
user?.address?.houseNumber;
```

Prevents errors when a property doesn't exist.

---

# Object Cloning

```js
const clone = Object.assign({}, obj);
```

or

```js
const clone = {...obj};
```

---

# Quick Revision

- map() transforms.
- filter() selects.
- reduce() calculates.
- find() returns first match.
- every() checks all.
- some() checks at least one.
- Set removes duplicates.
- Map stores flexible key-value pairs.
- Optional chaining prevents undefined errors.
- Spread operator and Object.assign() create shallow copies.
