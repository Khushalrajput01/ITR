## CSS Part 3



## 1. CSS Units

CSS Units are measurement values used to define the size, width, height, margin, padding, and font size of elements on a webpage.

### Common CSS Units

* px (Pixels)
* % (Percentage)
* em
* rem
* vh (Viewport Height)
* vw (Viewport Width)

### Example

```css
h1{
    font-size: 20px;
}

div{
    width: 50%;
}
```

* `20px` → Absolute unit (fixed size)
* `50%` → Relative unit (depends on parent element)

---

## 2. em, rem and px

### px (Pixel)

A fixed-size CSS unit used to define exact dimensions for text and elements.

```css
font-size: 16px;
```

### em

A relative unit that depends on the font size of the parent element.

```css
font-size: 2em;
```

### rem

A relative unit that depends on the font size of the root (`html`) element.

```css
font-size: 2rem;
```

---

## 3. Viewport Units

Viewport units are relative CSS units based on the size of the browser window (viewport).

### Types

* `vw` → 1% of viewport width
* `vh` → 1% of viewport height

### Example

```css
div{
    width: 50vw;
    height: 50vh;
}
```

---

## 4. CSS Floats

The `float` property is used to position elements to the left or right of their container, allowing text and other elements to wrap around them.

### Example

```css
img{
    float: left;
}
```

### Values

* left
* right
* none

---

## 5. CSS Positions

The `position` property controls the placement of elements on a webpage.

### Types of Position

1. **Static** – Default position of elements.
2. **Relative** – Positioned relative to its normal position.
3. **Absolute** – Positioned relative to the nearest positioned ancestor.
4. **Fixed** – Positioned relative to the browser window.
5. **Sticky** – Behaves like relative until a scroll point is reached, then acts like fixed.

### Example

```css
.box{
    position: absolute;
    top: 20px;
    left: 30px;
}
```

---

