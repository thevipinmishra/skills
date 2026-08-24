---
name: implementation-spec
description: Analyze a user-requested feature or fix, explore the existing codebase, gather the necessary context, and produce an implementation plan that follows the project's established architecture, patterns, and conventions.
---

# Implementation Specification

Use this skill when the user asks for a feature, bug fix, enhancement, or other implementation work that requires understanding the existing codebase.

## Core Principle

The goal is to understand the existing system before proposing changes.

The implementation must fit the project's existing architecture, patterns, conventions, and methodologies. Do not introduce new abstractions, patterns, methodologies, dependencies, or architectural changes unless they are genuinely required and explicitly approved by the user.

## Codebase Exploration

Before creating the implementation plan:

1. Explore the relevant parts of the codebase.
2. Identify existing implementations of similar or related functionality.
3. Understand the project's:
   - Architecture
   - Folder and module structure
   - Coding conventions
   - Existing abstractions
   - State management patterns
   - API/data-fetching patterns
   - Error-handling patterns
   - Testing approach
   - Existing dependencies and utilities
4. Identify the files and components that are likely to be affected.
5. Reuse existing patterns and utilities wherever possible.
6. Avoid proposing changes based on assumptions when the codebase can provide the answer.

Do not design the solution in isolation from the existing implementation.

## Implementation Approach

Prefer completing the implementation in a single pass when the scope is reasonably contained.

If the work is too large to safely complete in one session:

- Break it into logical phases.
- Make each phase independently understandable and implementable.
- Clearly state what remains for subsequent phases.
- Preserve enough context between phases to avoid re-exploring the same work unnecessarily.

Do not artificially split a small task into multiple phases.

## Design Constraints

- Follow established project patterns.
- Prefer existing abstractions over creating new ones.
- Do not introduce a new dependency if an existing dependency or project utility can solve the problem.
- Do not introduce a new architectural pattern unless required.
- Do not refactor unrelated code.
- Keep the implementation focused on the requested feature or fix.
- If multiple valid approaches exist, recommend the approach that best fits the existing codebase.
- Briefly mention viable alternatives when they could materially affect the implementation.
- If an architectural change, new dependency, or significant refactoring is required, explicitly call it out for user approval before implementation.

## Plan Template

The final plan must follow this structure:

### <Feature/Fix Name>

Briefly describe the feature or problem and the proposed solution.

### Implementation Steps

Provide the concrete steps required to implement the feature or fix.

For each step:

- Explain what needs to change.
- Reference the existing pattern or implementation being followed where relevant.
- Mention important implementation considerations.

If multiple approaches are viable:

- Recommend one approach.
- Briefly explain why it fits the existing codebase.
- List the alternatives and their trade-offs.

### Files & Changes

List:

- Files to modify
- Files to create, if any
- Existing utilities/components to reuse
- New dependencies, if any
- Refactoring required, if any
- Relevant conventions or patterns that must be followed

Clearly distinguish between existing files and new files.

### Verification

Describe how the implementation should be verified after the changes are made.

Include relevant checks such as:

- Unit/integration tests
- Existing test suites
- Type checking
- Linting
- Build verification
- Relevant manual verification

Do not start the local development server unless explicitly requested.

## Important

The plan should be specific enough that another developer or coding agent can implement it without having to rediscover the codebase context.

Do not produce generic implementation advice. The plan must be grounded in the actual project structure and existing implementation patterns.
