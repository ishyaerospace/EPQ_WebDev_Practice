# async intro

async allows a program to start a long-running task like fetching data. it then continues with other tasks before the first one finishes.
this prevents program from freezing on client end.

async allows functions to run in the background and return a result after.
async code does not run immediately:
* timer: run after a specific number of ms
* events: run when triggered by an event
* network requests: run when data arrives 

promises --> tools to handle asynchornous operations cleanly 
async & await --> are modern way to handle async code

## parallel vs asynchronous

parallel does mutliple tasks at the same time with different processors whereas asynchronous switches between tasks.

single-threaded JS engine handles asynchronous tasks by using an event loop to switch between them rather than untilising multiple CPU cores. when finished it singnals the main thread via a callback/promise/event to handle the result
