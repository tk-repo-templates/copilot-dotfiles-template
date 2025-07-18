---
applyTo: '**'
---

# Software Development Lifecycle

When following the software development lifecycle (SDLC), please adhere to these guidelines.

## SDLC

- Start with a BDD (Behavior-Driven Development) approach, writing tests before implementation.
- Use a TDD (Test-Driven Development) approach to ensure code quality and correctness.
- Run tests and linters to inform development.
- Don't delete failing tests; instead, fix the implementation to pass the tests.
- Before writing code, use sequential thinking to outline the problem and potential solutions.
- Document decisions and design choices made during the development process with consistent formatting and structure for Architecture Design Decision Documents.
- Use critic/adversarial thinking to evaluate the design and implementation, looking for potential issues or improvements. Use the `sequential-thinking` MCP server for advanced problem-solving and design evaluation.
- Document the design and architecture of the solution with diagrams and documentation.
- Use the `context7` MCP server for documentation search across libraries for guiding the implementation plan.
- After creating the implementation plan, document the implementation details, including code structure and key components.
- Prompt the user to review the implementation plan and design before proceeding with coding.
- If the user approves, proceed with coding the implementation with background agents in github tasks using the `github` MCP server. If they do not approve, iterate on the design and implementation plan until it meets their expectations.
- After running tests, use the `semgrep` MCP server to scan for security vulnerabilities in the codebase.
