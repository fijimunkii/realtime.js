realtime.js
===========

Schedule events to run at specific times of the day.

==========
Enjoy working with JavaScript? Me too.

I thought it was about time for a framework for calling functions at specific times.

One could always simply run:

var now = new Date();
var millisTill10 = new Date(now.getFullYear(), now.getMonth(), now.getDate(), 10, 0, 0, 0) - now;
if (millisTill10 < 0) {
     millisTill10 += 86400000; // it's after 10am, try 10am tomorrow.
}
setTimeout(function(){alert("It's 10am!")}, millisTill10);


But, what if you wanted a different function run every 5 minutes? That's a lot of copy and pasting. Luckily, I've done the hard work and felt like sharing. Feel free to optimize my code.
