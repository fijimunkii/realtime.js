realtime.js
===========
Schedule events to run at specific times of the day.
===========


I thought it time for a JavaScript framework to call functions at specific times of the day.

This is the native way way to schedule a function:
```
var now = new Date();
var millisTill10 = new Date(now.getFullYear(), now.getMonth(), now.getDate(), 10, 0, 0, 0) - now;
if (millisTill10 < 0) {
     millisTill10 += 86400000; // it's after 10am, try 10am tomorrow.
}
setTimeout(function(){alert("It's 10am!")}, millisTill10);
```
But, what if you wanted a different function run every 5 minutes? That's a lot of copy and pasting. My code is quite verbose, I have repeated myself a lot. There's definitely a way to generate a method and then loop through a javascript object containing the times. Please help me figure this out.
