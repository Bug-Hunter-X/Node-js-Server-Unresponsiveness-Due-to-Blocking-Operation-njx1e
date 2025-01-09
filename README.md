# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a server becomes unresponsive due to a blocking operation in a request handler.  The `server.js` file shows the problematic code, while `serverSolution.js` presents a solution using asynchronous programming.

## Problem

The provided server simulates a long-running task within the request handler.  This blocks the event loop, preventing the server from processing other requests, effectively causing a hang.

## Solution

The solution involves avoiding blocking operations and utilizing asynchronous techniques.  The ideal solution depends on the specific nature of the long-running task; in some cases, offloading it to worker threads or using promises is appropriate. In this simple case, using `setTimeout` for demonstration.