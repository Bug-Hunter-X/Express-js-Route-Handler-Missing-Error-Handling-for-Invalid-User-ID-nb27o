# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, this example focuses on a route that retrieves user data by ID.  If an invalid ID (non-numeric or not found) is provided, the application may crash or return unexpected results.

## Bug

The `bug.js` file contains an Express.js route handler that fetches a user by ID.  It lacks proper error handling for scenarios where the `userId` is not a valid number or a user with that ID is not found. This can lead to runtime errors or incorrect responses.

## Solution

The `bugSolution.js` file provides a corrected version of the route handler.  It includes comprehensive error handling, checking for non-numeric IDs and handling the case where a user is not found, resulting in a more robust and predictable application.

## How to reproduce

1. Clone the repository
2. Navigate to the repository directory
3. Run `npm install` to install dependencies
4. Run `node bug.js` and then navigate to `http://localhost:3000/users/abc` or some other invalid user ID in your browser
5. Compare the behavior with `node bugSolution.js` and the same URL