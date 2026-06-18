# JavaScript Day 7 — Revision Notes

## Topics Covered
- JavaScript setup
- Variables and naming rules
- `var`, `let`, and `const`
- Strings and string methods
- Data types and type conversion
- Truthy and falsy values
- Operators and conditionals
- Loops
- Arrays and array methods
- Array cloning and destructuring

---

# 1. JavaScript Setup

```html
<script src="practice.js"></script>
```

```javascript
console.log("Hello JavaScript");
```

**Note:** Place the `<script>` tag at the end of the `<body>`.

---

# 2. Variables

```javascript
let firstName = "Yatin";
let age = 22;
const city = "Mumbai";
```

### Naming Convention

```javascript
let totalMarks = 95;
```

Use **camelCase**.

---

# 3. var, let, and const

| Keyword | Redeclare | Update |
|----------|-----------|--------|
| var | Yes | Yes |
| let | No | Yes |
| const | No | No |

Prefer **const** by default.

---

# 4. String Indexing

```javascript
let name = "Yatin";

console.log(name[0]);
console.log(name[name.length - 1]);
```

Strings start from index **0**.

---

# 5. String Methods

### toUpperCase()

```javascript
name.toUpperCase();
```

### toLowerCase()

```javascript
name.toLowerCase();
```

### trim()

```javascript
message.trim();
```

### slice()

```javascript
word.slice(0,4);
```

### Template Strings

```javascript
let about = `My name is ${name}`;
```

---

# 6. Data Types

```javascript
typeof "hello";
typeof 10;
typeof true;
```

### Number → String

```javascript
String(age);
```

### String → Number

```javascript
Number("95");
```

### Equality

```javascript
==
===
```

`===` checks both value and type.

---

# 7. Truthy and Falsy Values

Falsy values:

- false
- ""
- 0
- null
- undefined

---

# 8. Conditionals

### if...else

```javascript
if(age >= 18){
 console.log("Eligible");
}
```

### Logical Operators

```javascript
&&
||
```

### Ternary Operator

```javascript
let drink = age >= 18 ? "Coffee" : "Milk";
```

---

# 9. Loops

### while Loop

```javascript
while(i <= 5){
 i++;
}
```

### for Loop

```javascript
for(let i=0;i<=10;i++){
 console.log(i);
}
```

### break and continue

```javascript
break;
continue;
```

---

# 10. Arrays

```javascript
let fruits = ["apple","mango"];
```

### Methods

```javascript
push()
pop()
unshift()
shift()
```

### Check Array

```javascript
Array.isArray(fruits);
```

---

# 11. Looping Arrays

### for

```javascript
for(let i=0;i<fruits.length;i++){}
```

### for...of

```javascript
for(let fruit of fruits){}
```

### for...in

```javascript
for(let index in fruits){}
```

---

# 12. Array Cloning

```javascript
slice()
concat()
[...array]
```

---

# 13. Array Destructuring

```javascript
const [a,b] = myArray;
```

Rest operator:

```javascript
const [a,b,...rest] = myArray;
```

---

# Quick Revision

- Prefer `const`.
- Use `===` instead of `==`.
- Strings start from index 0.
- Arrays are reference types.
- Use loops to repeat tasks.
- Spread operator is useful for cloning arrays.
- Destructuring simplifies value extraction.
