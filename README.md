This repository contains automated tests for Enyata Assessment using Postman.
It includes API tests
## Prerequisites
**Postman & Newman** (if applicable) → Installed via `npm install -g newman`
Environment Setup
Import the Postman collection and environment file into Postman.
Ensure you have valid API credentials before running tests.
## run Test with Newman
newman run Enyata_Postman_Collection.json -e Enyata_Environment.json --reporters cli,html --reporter-html-export report.html
## Observation & Blockers
❌ Failing Endpoints
The following endpoints are currently failing during execution:

DELETE User Endpoint

Issue: The API is returning a 500 Internal Server Error.
Expected Behavior: The user should be deleted successfully.
Steps to Reproduce:
Send a DELETE request to /api/users/{user_id}.
Observe the response status and message.
GET User Endpoint

Issue: The API is returning a 404 Not Found, even when the user exists.
Expected Behavior: The user details should be returned correctly.
Steps to Reproduce:
Send a GET request to /api/users/{user_id}.
Observe that the user is not found.

