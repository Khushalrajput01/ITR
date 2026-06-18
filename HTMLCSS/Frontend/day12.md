JavaScript Day 12 — Mini DOM Projects
Date: June 16, 2026
Topics Covered
Digital Clock
Dynamic Font Resizer
DOM Manipulation
Event Handling
setInterval()
Date Object
Input Events
Project 1: Digital Clock
A real-time digital clock that continuously displays the current time in HH:MM format.
Features
24-hour format
Automatic updates every second
Two-digit formatting using padStart()
Responsive layout with Flexbox
Logic Flow
Get the current date and time.
Extract hours, minutes, and seconds.
Convert them into strings.
Add leading zeros using padStart().
Display the formatted time.
Repeat every second using setInterval().
Code
function updateTime() {
    const clock = document.getElementById("time");
    const now = new Date();

    const hours = now.getHours().toString().padStart(2, "0");
    const minutes = now.getMinutes().toString().padStart(2, "0");
    const seconds = now.getSeconds().toString().padStart(2, "0");

    const timeString = `${hours}:${minutes}:${seconds}`;

    clock.textContent = timeString;
}

updateTime();

setInterval(updateTime, 1000);
Important Concepts
Date Object
const now = new Date();
Used to retrieve the current date and time.
padStart()
"5".padStart(2,"0");
Output:
05
Ensures consistent two-digit formatting.
setInterval()
setInterval(updateTime, 1000);
Runs the function every 1000 milliseconds (1 second).
Project 2: Dynamic Font Resizer
A small utility that changes the font size dynamically using a range slider.
Features
Real-time text resizing
Slider input
Adjustable range from 10px to 72px
Displays current font size
Working Process
User moves the slider.
input event gets triggered.
Font size is read from the slider value.
Paragraph size updates instantly.
Current size label is refreshed.
Code
const sizeSlider = document.getElementById("sizeSlider");

const textContent =
document.getElementById("textContent");

const currentSize =
document.getElementById("currentSize");

sizeSlider.addEventListener("input", function () {

    const para = textContent.querySelector("p");

    const fontSize = sizeSlider.value + "px";

    para.style.fontSize = fontSize;

    currentSize.textContent =
    "Current Size: " + fontSize;

});
Technologies Used
Technology	Purpose
HTML5	Structure
CSS3	Styling and Layout
JavaScript ES6	DOM Manipulation
Date Object	Current Time
setInterval()	Repeated Execution
Event Listeners	User Interaction
Important Methods Used
getElementById()
document.getElementById()
Selects elements by ID.
querySelector()
element.querySelector()
Selects the first matching element.
addEventListener()
element.addEventListener()
Listens for events.
style
element.style.fontSize
Changes CSS properties dynamically.
Quick Revision
✅ Date() provides the current date and time.
✅ padStart() adds leading zeros.
✅ setInterval() executes code repeatedly.
✅ addEventListener("input") responds instantly to slider changes.
✅ textContent updates text inside an element.
✅ style.fontSize changes text size dynamically.
✅ DOM methods allow JavaScript to interact with HTML elements.
Mini Projects Summary
Project	Concepts Practiced
Digital Clock	Date, padStart, setInterval
Font Resizer	DOM, Events, Style Manipulation
Next Step
Continue with more DOM projects involving:
To-Do List
Calculator
Counter App
Color Changer
Password Generator
Modal Popup
Theme Switcher