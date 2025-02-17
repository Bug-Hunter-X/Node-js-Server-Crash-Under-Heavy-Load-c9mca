# Node.js Server Crash Under Heavy Load

This repository demonstrates a common issue in Node.js applications: server crashes or unresponsiveness under heavy load.  The problem stems from inefficient request handling that can lead to unhandled exceptions or memory leaks.

## Problem Description

The `server.js` file contains a simple HTTP server. When subjected to a large number of concurrent requests (simulated in the code), the server might crash or become unresponsive. This is often due to:

* **Unhandled Exceptions:** Errors during request processing are not caught, causing the process to terminate.
* **Memory Leaks:**  The server fails to release resources after processing requests, leading to memory exhaustion.

## Solution

The `serverSolution.js` file provides a solution addressing these issues.  Key improvements include:

* **Error Handling:**  Robust error handling using `try...catch` blocks and event listeners catches and logs exceptions, preventing server crashes.
* **Resource Management:**  Careful management of resources ensures that memory is released appropriately after each request.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository's directory in your terminal.
3. Run `node server.js` to start the server.
4. Observe the server's behavior under the simulated load.  You may need to adjust the number of requests in the loop to consistently reproduce the crash.

## How to Run the Solution

1. Run `node serverSolution.js` to start the improved server.
2. Repeat step 4 from the reproduction instructions. The improved server should handle the load more gracefully.
