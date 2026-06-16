# Day2 Topics Discussed....

## 1.CSS:-

CSS(CASCADING STYLE SHEETS) is a stylesheet language used to control the apperance and layout of webpages .It works together with HTML.

Example:-

HTML:-

<h1>Hello World</h1>

Without CSS the heading appears with default browser styling.

With CSS:-

h1{
    color: blue;
    font-size: 40px;
    text-align: center;
}

The heading becomes blue,larger, and centered.

Features of CSS:-
1.Easy to maintain
2.Faster webpage loading
3.Consistent design across pages
4.Reusable styles.

Types of CSS:-

1.Inline CSS
2.Internal CSS
3.External CSS

Topics:-

## 1.CSS styling ways

CSS(Cascading Style Sheets) is used to style HTML elements.

Types of CSS:-

1.Inline CSS

Written inside the HTML tag using style attribute.

Example:-

<h1 style="color:red;">Hello</h1>

2.Internal CSS

Written inside <style> tag in <head>.

Example:-

<style>
    h1{color:red; }
</style>

3.External CSS

Written in a separate .CSS file.

Example:-

<link rel="stylesheet"
href="style.css">

Most commonly used in projects.

## 2.CSS Fonts

Used to change the apperance of text.

Important Properties:-
1.font-family
2.font-size
3.font-weight
4.font-style

Example:-
CSS
p{
    font-family: Arial;
    font-size:20px;
    font-weight:bold;
}

## 3.CSS Colors

Used to set text and background colors.

Methods:-

1.Color Name

css

color:red;

2.RGB

css

color:rgb(255,0,0);

3.HEX

css

color:#ff0000;

4.HSL

css

color:hsl(0,100%,50%);

## 4.CSS Selectors

Selectors choose HTML elements to style.

Types:-
1.Element Selector
2.ID Selector
3.Class Selector
4.Universal Selector

## 5.Utility Class,ID and Class 

ID

1.Unique for one element.

HTML

<h1 id="header">Title</h1>

CSS

#header{
    color:blue;
}

Class

1.Can be used for multiple elements.

HTML
<p class="text">Hello</p>

CSS
.txt{
    color:red;
}

Difference between ID and Class:-

ID:- Unique,Uses #,Higher priority
Class:- Reusable,Uses ., Lower priority

## 6.More CSS Selectors

Group Selector
Descendent Selector
Child Selector
Adjacent Sibling

## 7.CSS Attribute Selector

Selects elements based on attributes.

Example:-

CSS

input[type="text"]{
    background-color:yellow;
}

HTML

<input type="text">

Uses:-
1.Styling Forms
2.Filtering Elements.