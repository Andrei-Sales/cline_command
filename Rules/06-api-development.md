# API Development Rules

Design APIs consistently with the existing application.

## REST

Prefer predictable resource-oriented endpoints.

Examples:

GET    /users
GET    /users/{id}
POST   /users
PUT    /users/{id}
PATCH  /users/{id}
DELETE /users/{id}

## HTTP Status Codes

Use appropriate status codes.

200 OK
201 Created
204 No Content
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
409 Conflict
422 Unprocessable Entity
429 Too Many Requests
500 Internal Server Error
503 Service Unavailable

## Validation

Validate requests at the API boundary.

Return structured errors.

Example:

{
  "code": "VALIDATION_ERROR",
  "message": "Invalid request",
  "details": [...]
}

## API Security

Check:

- authentication
- authorization
- rate limiting where required
- input validation
- output filtering
- sensitive information exposure

## Backward Compatibility

Before changing an existing API:

- search for consumers
- inspect frontend usage
- inspect other services
- check tests
- consider versioning

Do not casually rename or remove API fields.