# Unresponsive Node.js Server: Synchronous Long-Running Task

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler blocks the event loop, making the server unresponsive.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The `bug.js` file creates an HTTP server.  The request handler includes a `while` loop that simulates a long-running task. This blocks the event loop, preventing the server from processing subsequent requests.  This results in the server becoming unresponsive during the 5-second delay.