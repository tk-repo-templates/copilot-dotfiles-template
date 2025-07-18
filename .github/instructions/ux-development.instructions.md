---
applyTo: '**'
---

# UX Development Guidelines

When developing ux components, please follow these guidelines.

## Architecture

- Build micro-components that can be easily integrated into larger applications.
- Independently deployable components should be versioned and documented.
- Each component should have a clear API for interaction with the parent application, documented with Storybook.

## Accessibility

- Make components accessible and responsive
- Use semantic HTML and ARIA roles where appropriate.
- Use a linter to check for accessibility issues.
- Test components with screen readers and keyboard navigation.
- Ensure color contrast meets WCAG standards.

## Mobile Responsiveness

- Build components that adapt to different screen sizes; Use CSS media queries and flexible layouts.
- Test components on various devices and browsers to ensure consistent behavior using the Playwright MCP server.
- Use relative units (like `em`, `rem`, `%`) for sizing instead of fixed units (like `px`).
- Implement touch-friendly interactions for mobile devices.

## Component Development

- Build components that will be rendered as micro-components delivered through unpkg or esm.sh.
- Each component should be self-contained, self-deployable, and versioned separately.
- Expose events, providers, and hooks for interaction with the parent application as appropriate.
- Test components across different browsers and devices using the Playwright MCP server.
- Document components clearly, including usage examples and props; Build a storybook for visual testing.

## Styling and Theming

- Use CSS-in-JS or CSS modules for styling components to avoid global styles conflicts.
- Ensure consistent styling by adhering to the project's design system.
- Use variables for colors, fonts, and spacing to maintain consistency and ease of updates.
- Implement dark mode support if applicable, using CSS custom properties or media queries.
- Prefer Tailwind CSS unless otherwise specified.
- Choose a design system unless otherwise specified.

