# Express.js Route Handler Missing Error Handling for Invalid User IDs

This repository demonstrates a common error in Express.js route handlers: missing error handling for invalid input.  Specifically, this example shows a route that fetches a user by ID, but fails to handle cases where the ID is not a valid number.

## The Bug

The `bug.js` file contains an Express.js route handler that fetches a user by ID. However, it doesn't handle the case where the `userId` parameter is not a number.  This can lead to errors if a user attempts to access a route with a non-numeric ID.

## The Solution

The `bugSolution.js` file provides a corrected version of the route handler that includes error handling.  It checks if the `userId` parameter can be parsed as an integer and handles the case where it cannot.  It also handles the case where a user with the specified ID does not exist.