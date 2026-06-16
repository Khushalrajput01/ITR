# Day 5 





# 1. CSS Flexbox

Flexbox (Flexible Box Layout) is a one-dimensional layout model used to align and distribute space among items inside a container.

## Enable Flexbox

```css
.container{
    display: flex;
}
```

## Common Flexbox Properties

### flex-direction

Controls the direction of flex items.

```css
flex-direction: row;
flex-direction: column;
flex-direction: row-reverse;
flex-direction: column-reverse;
```

### justify-content

Aligns items along the main axis.

```css
justify-content: center;
justify-content: space-between;
justify-content: space-around;
justify-content: space-evenly;
```

### align-items

Aligns items along the cross axis.

```css
align-items: center;
align-items: flex-start;
align-items: flex-end;
align-items: stretch;
```

### flex-wrap

Controls whether items wrap to the next line.

```css
flex-wrap: wrap;
flex-wrap: nowrap;
```

### gap

Creates spacing between flex items.

```css
gap: 20px;
```

### flex-grow

Specifies how much an item should grow.

```css
flex-grow: 1;
```

### flex-shrink

Specifies how much an item should shrink.

```css
flex-shrink: 1;
```

### order

Changes the order of flex items.

```css
order: 2;
```

---

# 2. CSS Grid

CSS Grid is a two-dimensional layout system used to create rows and columns.

## Enable Grid

```css
.container{
    display: grid;
}
```

## Grid Properties

### grid-template-columns

Defines the number and size of columns.

```css
grid-template-columns: 1fr 1fr 1fr;
```

### grid-template-rows

Defines row sizes.

```css
grid-template-rows: 100px 100px;
```

### gap

Adds spacing between rows and columns.

```css
gap: 15px;
```

### grid-column

Controls column span.

```css
grid-column: 1 / 3;
```

### grid-row

Controls row span.

```css
grid-row: 1 / 3;
```

---

# 3. Media Queries

Media Queries are used to make websites responsive on different screen sizes.

## Syntax