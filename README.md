# Unhandled Asynchronous Error in Node.js Express Server

This repository demonstrates a common error in Node.js applications: unhandled errors within asynchronous operations.  The example uses Express.js to create a simple server that simulates an asynchronous task which might throw an error. Without proper error handling, the server crashes upon encountering such errors.

The `bug.js` file showcases the problematic code. The `bugSolution.js` demonstrates the correct way to handle asynchronous errors, preventing crashes and providing graceful error handling.  This is crucial for production-ready Node.js applications.

## How to run

1. Clone the repository:
   ```bash
git clone <repository_url>
```
2. Navigate to the repository directory:
   ```bash
cd <repository_directory>
```
3. Install dependencies:
   ```bash
npm install express
```
4. Run the buggy version (`bug.js`):
   ```bash
npm start
```
5. Observe the server crashing (approximately 50% of the time due to the random nature of the error).  Then run the corrected version (`bugSolution.js`) and notice the graceful handling of the error.

## Key Learning Points

* Proper error handling is critical in Node.js applications due to their asynchronous nature.
* Always use `try...catch` blocks to handle potential errors within asynchronous callbacks.
* Employ appropriate logging to report errors and help with debugging.