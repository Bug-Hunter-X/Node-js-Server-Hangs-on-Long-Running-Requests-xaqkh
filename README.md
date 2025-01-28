# Node.js Server Hangs on Long-Running Requests

This repository demonstrates a common issue in Node.js where long-running synchronous operations block the event loop, causing the server to hang and become unresponsive.  The `server.js` file contains the problematic code, while `serverSolution.js` provides a solution using asynchronous operations.

## Problem

The original code simulates a long-running task within the request handler. This blocks the event loop, preventing the server from processing other requests or responding to existing ones. This leads to a poor user experience as users might observe timeouts or unresponsive behavior.

## Solution

The solution uses asynchronous operations to handle long-running tasks without blocking the event loop.  This ensures that the server remains responsive to other requests even while processing lengthy tasks.

## How to Run

1. Clone this repository.
2. Navigate to the repository's directory.
3. Run `node server.js` to observe the problematic behavior.
4. Run `node serverSolution.js` to see the improved, responsive server.
