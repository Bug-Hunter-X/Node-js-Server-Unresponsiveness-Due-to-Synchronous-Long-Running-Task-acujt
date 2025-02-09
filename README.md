# Node.js Server Unresponsiveness

This repository demonstrates a common Node.js issue: server unresponsiveness caused by a long-running synchronous operation that blocks the event loop.  The `server.js` file contains the buggy code, while `serverSolution.js` provides a corrected version using asynchronous programming.

## Problem

The original code uses a `while` loop to simulate a 5-second task that blocks the event loop.  During this time, the server is unable to handle any new incoming requests, leading to unresponsiveness.

## Solution

The solution uses asynchronous operations to prevent blocking the event loop.  Asynchronous programming allows Node.js to continue processing other events while the long-running task is in progress.