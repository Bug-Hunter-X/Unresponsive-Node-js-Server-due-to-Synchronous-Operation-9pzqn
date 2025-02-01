# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler can make the server unresponsive.  The `server.js` file contains the buggy code, while `server-solution.js` provides a corrected version using asynchronous operations.

## Bug Description

The server performs a 5-second CPU-bound operation synchronously within the request handler. During this time, the server cannot accept or process any new requests, leading to unresponsiveness.

## Solution

The issue is resolved by replacing the synchronous operation with an asynchronous alternative.  This allows Node.js's event loop to continue handling other requests while the long operation is in progress.  See `server-solution.js` for the solution.