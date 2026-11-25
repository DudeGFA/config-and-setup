
# Agent Directives & Execution Protocol

## 1. Pre-Implementation Discovery (Mandatory)

- Utilize reusable components and functions.
- Never write custom styling for buttons, inputs, modals, cards, or typography if an existing shared component can fulfill the requirement.
- Inspect surrounding sibling views to match token usage: spacing, colors, border radii, font scales, and icon libraries.

## 2. Dynamic Data & State Handling

- When converting a static/mock UI to dynamic data:
  - Implement complete lifecycle states for every async operation:
    1. Loading (skeletons or spinners matching design patterns).
    2. Empty state (helpful user copy, call-to-action if applicable).
    3. Error state (retry action, clean visual feedback).
    4. Populated state.
  - Delete all mock arrays, dummy objects, and hardcoded placeholder text entirely.

## 3. UI/UX Constraints

- **Strictly forbid native alerts:** Never call `window.alert()`, `window.confirm()`, or native OS alert dialogs.
- Maintain absolute visual consistency: do not invent new hex colors or arbitrary pixel margins. Use defined design system tokens/utility classes.

## 4. Code Quality & Bug Prevention

- Always follow established engineering best practices.
- Implement changes in a way that prevents bugs in both the current implementation and other existing implementations.
- Clean up side effects: ensure every event listener, timer, or socket subscription has an appropriate teardown/cleanup mechanism.
- Do not leave dead or missing imports, commented-out dead code, or unnecessary `console.log` statements in the final diff.
- Ensure the implementation works correctly.

## 5. AI-Assisted Development

- Treat AI-generated code and recommendations as proposals that must be reviewed and validated.
- Understand the relevant implementation before making significant changes.
- When investigating bugs, identify and verify the root cause before implementing a fix.
- Base technical decisions on evidence from the codebase rather than unsupported assumptions.
- Prioritize correctness, reliability, simplicity, security, and maintainability over unnecessary complexity.
- Do not make broad or unrelated modifications without a clear justification.
- Preserve existing architecture and conventions unless there is a justified reason to change them.
- Use independent review when it would materially improve confidence in the solution.
- Explain important assumptions, technical decisions, trade-offs, and limitations.
- Communicate uncertainties and blockers rather than making unsupported claims.

## 6. Testing and Validation (Mandatory)

### Pre-Implementation

- Inspect the existing test structure, testing framework, configuration, and project test commands.
- Follow the testing conventions and patterns already established in the codebase.
- Identify the tests relevant to the affected functionality.
- Where practical, run relevant existing tests before implementation to establish a baseline and identify pre-existing failures.

### Test Implementation

- For bug fixes, add or update a regression test that reproduces the reported issue where practical.
- Where possible, confirm that the regression test fails before the fix and passes afterward.
- For new functionality, add tests covering expected behavior, relevant edge cases, and failure scenarios.
- Consider invalid inputs, empty states, boundary conditions, authorization, concurrency, and external dependency failures where applicable.
- Keep test changes focused on the behavior being implemented or corrected.
- Ensure tests validate actual expected behavior rather than merely reflecting the implementation.
- Do not introduce unnecessary testing dependencies.

### Test Execution

- Run tests using the project's documented commands or package scripts. Do not assume a particular test framework or command.
- Run focused tests during development, followed by related test suites.
- Run the full test suite before completing the task where practical.
- Run applicable linting, type-checking, and build checks.
- Perform manual or integration verification when automated tests cannot adequately validate the affected behavior.
- Use isolated test environments and test databases. Never execute destructive tests against production systems.

### Failure Handling

- If a test fails, investigate the underlying cause before changing the implementation or test.
- Distinguish between implementation defects, incorrect test assumptions, pre-existing failures, and environment limitations.
- Do not modify, delete, skip, or weaken existing tests merely to make the test suite pass.
- Do not suppress errors or introduce workarounds that conceal underlying problems.

### Final Validation

- Inspect the final diff for unintended changes, unnecessary complexity, and potential regressions.
- Verify that the implementation satisfies the original requirements.
- Do not claim that tests pass unless they have actually been executed and their results verified.
- If tests cannot be run due to missing dependencies, environment limitations, or other constraints, explain the reason and identify what remains unverified.
- Provide a concise validation summary containing:
  - Tests added or modified.
  - Commands executed.
  - Test results.
  - Pre-existing failures, if any.
  - Remaining risks or unverified behavior.


## 7. Post-Implementation

- Complete all applicable testing and validation.
- Inspect `git status` and `git diff` for unintended changes.
- Create database migrations only when required.
- Do not push commits, deploy applications, or modify remote resources without explicit authorization.
- Provide a concise implementation summary containing:
  - Changes made.
  - Root cause identified, where applicable.
  - Technical decisions and trade-offs.
  - Files modified.
  - Tests and validation results.
  - Remaining limitations, risks, or recommended follow-up actions.
