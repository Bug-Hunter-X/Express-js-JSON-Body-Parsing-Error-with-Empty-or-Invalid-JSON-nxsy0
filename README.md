# Express.js JSON Body Parsing Error

This repository demonstrates a common error encountered when working with JSON request bodies in Express.js applications.  The problem arises when the request body is either empty or contains invalid JSON data. This leads to the `req.body` object being undefined or incorrectly parsed.

## Bug Description
The provided Express.js server attempts to handle POST requests to the `/data` endpoint, expecting a JSON payload. If the client sends an empty request body or a request body that is not valid JSON, the server fails to parse the body correctly. This can lead to unexpected behavior or errors.  The server logs `undefined` when the body is invalid.

## Solution
The solution involves adding error handling to gracefully handle cases where the request body is empty or contains invalid JSON.  This is achieved by checking if `req.body` is empty before attempting to access its properties, or using a try-catch block to handle JSON parsing errors.