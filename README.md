# Express.js Route Handler Bug: Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the provided code attempts to parse a user ID as an integer without checking if the input is valid. This can lead to unexpected errors or crashes.

## Bug Description
The `GET /users/:id` route attempts to find a user based on the ID provided in the URL.  However, if the `id` parameter is not a valid integer, the `parseInt` function will return `NaN`, causing the `find` method to fail silently or throw an error depending on how the application is configured.

## Solution
The solution involves adding input validation to ensure the `userId` is a valid integer before attempting to find the user.  This prevents errors and provides a more robust and user-friendly experience.