# JavaScript Day 10 — Prototypes and Constructor Functions

## Topics Covered

* Prototype in JavaScript
* The `new` Keyword
* Constructor Functions and Prototype Methods
* `Object.create()`
* `hasOwnProperty()` and `for...in`
* Built-in Prototypes

---

# 1. Prototype in JavaScript

Every JavaScript **function** has a built-in property called `prototype`. It is used to store methods and properties that are shared among all objects created from that function.

```javascript
function hello(){}

console.log(hello.prototype); // {}
```

Regular objects do not have a prototype property.

```javascript
const obj = {
    name: "Yatin"
};

console.log(obj.prototype); // undefined
```

### Adding Properties and Methods to Prototype

```javascript
function hello(){}

hello.prototype.abcProperty = "abc";

hello.prototype.sing = function(){
    console.log("lalalala");
};

hello.prototype.sing();
```

### Prototype Chain

```
Person Instance
      ↓
Person.prototype
      ↓
Object.prototype
      ↓
null
```

### Key Points

* Only functions have a `prototype` property by default.
* Prototype is initially an empty object.
* Methods stored on prototype are shared by all instances.
* `Object.prototype` is the root of the inheritance chain.

---

# 2. The `new` Keyword

The `new` keyword creates a new object using a constructor function.

```javascript
function CreateUser(firstName, age){
    this.firstName = firstName;
    this.age = age;
}

const user1 = new CreateUser("Yatin", 22);
```

## What Happens Internally?

1. Creates an empty object.
2. Links the object's prototype to the constructor's prototype.
3. Binds `this` to the new object.
4. Returns the object automatically.

### Example

```javascript
function CreateUser(firstName, age){
    this.firstName = firstName;
    this.age = age;
}

CreateUser.prototype.about = function(){
    console.log(this.firstName, this.age);
};

const user1 = new CreateUser("Yatin",22);

user1.about();
```

### Key Points

* Constructor functions are written using PascalCase.
* `new` automatically links prototypes.
* Methods should be stored on prototype instead of inside the constructor.

---

# 3. Constructor Functions and Prototype Methods

Constructor functions are used to create multiple similar objects.

```javascript
function CreateUser(firstName, lastName, email, age){
    this.firstName = firstName;
    this.lastName = lastName;
    this.email = email;
    this.age = age;
}
```

### Shared Methods

```javascript
CreateUser.prototype.about = function(){
    return `${this.firstName} ${this.lastName}`;
};

CreateUser.prototype.is18 = function(){
    return this.age >= 18;
};
```

### Benefits

* Properties are unique for each object.
* Methods are shared among all objects.
* Memory efficient.

### Key Points

* Store methods on prototype.
* Objects created with `new` automatically inherit prototype methods.

---

# 4. `Object.create()`

`Object.create()` manually creates an object and links it to a prototype.

```javascript
function createUser(firstName, age){
    const user = Object.create(createUser.prototype);

    user.firstName = firstName;
    user.age = age;

    return user;
}
```

### Example

```javascript
createUser.prototype.is18 = function(){
    return this.age >= 18;
};
```

### `new` vs `Object.create()`

| Feature         | new Keyword | Object.create() |
| --------------- | ----------- | --------------- |
| Creates Object  | Automatic   | Manual          |
| Links Prototype | Automatic   | Manual          |
| Binds `this`    | Automatic   | Manual          |
| Returns Object  | Automatic   | Manual          |

### Key Points

* `Object.create()` provides manual prototype linking.
* It helps understand how `new` works internally.

---

# 5. `hasOwnProperty()` and `for...in`

`for...in` loops over both object properties and inherited properties.

```javascript
for(let key in user1){
    console.log(key);
}
```

To access only the object's own properties:

```javascript
for(let key in user1){
    if(user1.hasOwnProperty(key)){
        console.log(key);
    }
}
```

### Key Points

* `hasOwnProperty()` checks whether a property belongs directly to an object.
* It ignores inherited properties.
* `Object.keys()` returns only own enumerable properties.

---

# 6. Built-in Prototypes

Built-in objects such as arrays and dates also use prototypes.

```javascript
let numbers = [1,2,3];

console.log(Array.prototype);
console.log(Object.getPrototypeOf(numbers));
```

Array methods such as:

* `push()`
* `pop()`
* `map()`
* `filter()`

come from `Array.prototype`.

### Prototype Chain

```
Array Instance
      ↓
Array.prototype
      ↓
Object.prototype
      ↓
null
```

### Key Points

* Every built-in type has its own prototype.
* `Object.getPrototypeOf()` returns the prototype of an object.
* Modifying built-in prototypes is possible but discouraged.

---

# Quick Revision

✅ Only functions have a `prototype` property.

✅ Methods placed on prototype are shared by all objects.

✅ `new` creates objects automatically and links prototypes.

✅ Constructor functions are usually written using PascalCase.

✅ `Object.create()` allows manual prototype linking.

✅ `hasOwnProperty()` checks only an object's own properties.

✅ Array methods come from `Array.prototype`.

✅ `Object.prototype` is at the top of the prototype chain.
