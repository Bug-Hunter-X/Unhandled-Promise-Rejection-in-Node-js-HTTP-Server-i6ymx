# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js: unhandled promise rejections within an HTTP server.  The provided code simulates an asynchronous operation that can either resolve successfully or throw an error. The initial implementation lacks proper error handling, causing the server to behave unexpectedly when errors occur.

The solution demonstrates how to correctly handle these rejections to prevent crashes and ensure a robust server.

## How to Run

1. Clone the repository.
2. Navigate to the repository's directory.
3. Run `npm install` to install dependencies (although none are strictly required).
4. Run `node bug.js` to start the server with the buggy code.  Observe the behavior when the simulated error occurs.
5. Run `node bugSolution.js` to start the server with the corrected error handling. Observe the improved behavior.

## Key Learning Points

* **Importance of `catch` blocks:** Always handle potential errors in asynchronous operations using `.catch()`. Ignoring rejections can lead to application instability and unpredictable errors.
* **Sending meaningful error responses:** When errors occur, provide informative responses to clients instead of simply logging the error.
* **Robust error handling:** Implement comprehensive error handling strategies to prevent crashes and improve application resilience.