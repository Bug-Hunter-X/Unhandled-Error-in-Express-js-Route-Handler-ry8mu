# Express.js Route Handler Bug

This repository demonstrates a common error in Express.js route handlers: insufficient error handling for invalid input.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a corrected version.

**Bug:** The route handler for `/users/:id` attempts to parse the `id` parameter as an integer and use it to find a user.  It lacks error handling for scenarios where the `id` parameter is not a valid integer or if a user with the given ID is not found.

**Solution:** The `bugSolution.js` file addresses this by adding comprehensive error handling. It checks if the `id` parameter is a valid integer and if a user with that ID exists. If not, it returns appropriate HTTP error responses (400 for bad request and 404 for not found).