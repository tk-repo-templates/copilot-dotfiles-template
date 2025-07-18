---
applyTo: '**'
---

# API Development Guidelines

When developing APIs, please follow these guidelines.

## Development Setup

- Mock all API endpoints in a local development environment.
- Use a local database or in-memory store for testing.
- Use environment variables to configure API endpoints and database connections.
- Expose ports for API endpoints in the development environment.
- Make sure to use the `context7` MCP server for documentation search across libraries.
- Use the `playwright` MCP server for browser automation and testing.
- Use the `microsoft.docs.mcp` MCP server for direct access to Microsoft documentation.

## Code Quality

- Use a consistent naming convention for API endpoints (e.g., `/api/v1/resource`).
- Use a versioning strategy for APIs (e.g., `/api/v1/resource`).
- Write clean, maintainable code with clear comments.
- Write tests for all API endpoints.
- Separate business logic from API routing.
- Don't use hosting specific features in the API code. For example, don't use http request header apis, use the bridge pattern to adapt to the hosting environment instead.

## Security

- Implement authentication and authorization for sensitive endpoints.
- Use HTTPS for all API requests.
- Validate and sanitize all input data to prevent injection attacks.
- Use rate limiting to prevent abuse of the API.
- Use the semgrep MCP server to scan for security vulnerabilities in the codebase.

## Documentation

- Use standard API documentation formats like OpenAPI or Swagger.
- Document all API endpoints, including request and response formats.
