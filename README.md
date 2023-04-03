1. What is the Event Loop
The Event Loop is the mechanism that manages the scheduling and running and code in Javascript in an asynchronous way. It runs infinitely, collecting events and callbacks, schedule them in the task queue to be allocated in the call stack for execution.

2. What are the six phases of the event loop
The Node.js Event Loop can be summarized the following phases

* Timer: When a asynchronous code is scheduled to be run, it is added to the timer phase. This phase handles timers scheduled by setTimeout, setInterval and from event handlers listening to DOM Events.
* Pending callbacks: This phase handles executing I/O related callbacks that where scheduled to the next iteration of the loop.
* Idle, Prepare: This runs internal node.js tasks
* Poll: This phase retrieves new I/O events and execute their callbacks. This phase will block for any slow callbacks. If also timers are also completed in the timer phase. It they will be executed in here immediately.
* Check: This phases runs callbacks scheduled by setImmediate()
* Close callbacks: This phase handles executing close callbacks

3. Best practices learned from server-side programming
* Reducing the amount of variables initialized
* Avoid using sync-style methods for I/O operations like readFileSync, writeFileSync
* Always try to avoid code that may block the event loop

4. What is NPM?
It's a tool for downloading and managing JavaScript packages.

5. How do you initialize a package in npm
run npm init.
