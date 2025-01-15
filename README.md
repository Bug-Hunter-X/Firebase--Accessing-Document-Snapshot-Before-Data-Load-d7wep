# Firebase Asynchronous Data Access Error
This repository demonstrates a common error when working with Firebase and asynchronous operations: attempting to access data from a document snapshot before the data has fully loaded.  The `bug.js` file shows the problematic code, while `bugSolution.js` presents a corrected version using promises and `.then()` to ensure data is available before access.

## Reproducing the Bug
1.  Clone this repository.
2.  Ensure you have a Firebase project set up and the necessary credentials.
3.  Run `bug.js`. You should see an error indicating that a property is undefined.

## Solution
The corrected code in `bugSolution.js` demonstrates the proper way to handle this situation. By using `.then()`, the code waits for the promise to resolve before accessing the data, preventing the error.