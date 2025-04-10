Asynchronous programming in Python enables concurrent execution of code, improving efficiency, especially in I/O-bound operations. It allows a program to start a task, pause it while waiting for a result (like reading a file or a network request), and then continue with other tasks in the meantime. This approach avoids blocking the main program flow, leading to more responsive and efficient applications.
The asyncio library is a primary tool for asynchronous programming in Python. It provides an event loop to manage and schedule coroutines, which are functions that can be paused and resumed. The async and await keywords are central to this process: async defines a coroutine, and await pauses the execution of a coroutine until another coroutine or task completes.

- asyncio is a library to write concurrent code using the async/await syntax.

- asyncio is used as a foundation for multiple Python asynchronous frameworks that provide high-performance network and web-servers, database connection libraries, distributed task queues, etc.
- asyncio is often a perfect fit for IO-bound and high-level structured network code.



#### Resources
- https://github.com/xiaopeng163/asyncio-demo/tree/master
