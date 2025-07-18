---
applyTo: '**'
---

# App Development Guidelines

When developing applications, please follow these guidelines.

## Architecture

- Assume a microservices architecture with independent deployable components.
- Prefer setup as a PWA (Progressive Web App) for cross-platform compatibility.
- Prefer navigation through a single-page application (SPA) framework.
- Separate business logic from UI components.
- Build offline-first applications that can function without a network connection.

## Testing

- Use Playwright for end-to-end testing.
- Use a BDD framework like Cucumber/Gherkin or Gauge for capturing app behavior / features.
- Test for accessibility, responsiveness, and performance.

## Code Quality

- Write clean, self-documenting, idiomatic code.
- Use linters to enforce coding standards and catch potential issues.
- Use the `semgrep` MCP server to scan for security vulnerabilities in the codebase.
- Use DRY, SOLID, and KISS principles to ensure maintainability.
- Make Uncle Bob proud by adhering to clean code & clean architecture principles as a software craftsman.
