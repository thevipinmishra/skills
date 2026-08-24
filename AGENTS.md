Follow these instructions unless they are explicitly overridden by a specific prompt.

## Git

- NEVER commit or push changes without explicitly asking for and receiving confirmation from the user.
- Do not create commits as part of routine development or testing.

## Code

- Follow the existing code patterns, conventions, architecture, and naming used in the codebase.
- Prefer co-located, modular, and testable code.
- Avoid unnecessary refactoring or introducing new patterns unless required by the task.
- Keep changes focused on the requested scope.
- NEVER add code comments unless they are genuinely necessary.
- When comments are required, keep them minimal and explain only non-obvious behavior or intent.

## Testing & Development Server

- NEVER start or run the local development server unless explicitly asked.
- Assume the local development server is already running when testing or debugging.
- Prefer existing test suites, type checks, linters, and build commands where applicable.

## Documentation & APIs

- NEVER rely on training data for API usage, library behavior, configuration, or version-specific implementation details.
- Always refer to the official documentation for the exact version of the library, framework, or API used in the project.
- When official documentation is unavailable or ambiguous, state the uncertainty rather than guessing.

## General

- Before making changes, inspect the existing implementation and understand the surrounding code.
- Reuse existing utilities, components, abstractions, and dependencies where appropriate.
- Do not introduce a dependency when the existing codebase already provides a suitable solution.
- Keep implementations simple, maintainable, and consistent with the project's existing architecture.
