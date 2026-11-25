# Codebase Exploration

I want you to help me understand this codebase before making any modifications.

Task context:
[INSERT TASK]

Please:

1. Identify and follow relevant repository instructions, including AGENTS.md, CLAUDE.md and other project-specific guidelines.
2. Identify the primary application architecture and technology stack.
3. Explain the main directories and their responsibilities.
4. Identify the application entry points.
5. Trace the relevant request, data or execution flow.
6. Identify relevant database models and their relationships.
7. Identify existing components, services, utilities and patterns that could be reused.
8. Identify existing testing conventions, development tooling and validation commands.
9. Highlight architectural patterns, conventions and constraints I should preserve.

Prioritize exploration relevant to the task rather than exhaustively analyzing the entire repository.

Distinguish verified findings from assumptions and identify any important gaps in understanding.

Do not modify any files.

Present your findings in a structured and concise manner. Reference the relevant files and functions.


# Problem Investigation

Investigate the task described below:

[INSERT TASK]

- Identify the expected behaviour, current behaviour, requirements and constraints.
- Trace the relevant execution and data flows.
- Identify relevant existing functionality, dependencies and affected components.
- Establish the baseline behaviour and identify existing failures where practical.
- Identify gaps between the current implementation and the desired behaviour.

For bugs or unexpected behaviour, identify potential root causes. For each potential cause:

- Explain the underlying mechanism.
- Identify the relevant files and functions.
- Explain the conditions under which it could occur.
- Reproduce or verify it where practical, or explain how it could be verified.

For new features or improvements, identify integration points, existing functionality that can be reused, implementation constraints and potential impacts on the existing system.

Prioritize evidence from the existing implementation over assumptions.

Distinguish confirmed findings from hypotheses and identify uncertainties requiring clarification.

Do not modify any files. Use non-destructive investigation methods and isolated, non-production environments where applicable.


# Solution Design

Based on our investigation, propose the simplest reliable solution that satisfies the requirements.

- Identify the requirements, constraints, assumptions and system invariants.
- Define explicit, testable acceptance criteria.
- Evaluate viable approaches and their trade-offs.
- Identify applicable engineering principles, design patterns and domain-specific best practices.
- Consider the following where relevant:
  - Data integrity, consistency, database transactions, atomicity and isolation.
  - Concurrency, race conditions, locking and deadlocks.
  - Idempotency, deduplication, retries and timeouts.
  - Financial correctness, double-entry accounting, ledger integrity, reconciliation and precise monetary representations instead of binary floating-point arithmetic.
  - Database indexing, constraints, query optimization and performance.
  - Security, authentication, authorization and input validation.
  - Scalability, caching and resource contention.
  - Distributed system behaviour, partial failures and recovery.
  - Fault tolerance, observability and auditability.
  - Backward compatibility and migration implications.
- Proactively identify additional considerations specific to the problem.
- Analyze relevant edge cases, failure scenarios and potential regressions.
- Recommend a pragmatic solution and justify the design decisions.
- Identify affected files, components and data models.
- Outline the implementation and testing strategy.

Preserve existing architectural conventions. Avoid unnecessary complexity and do not introduce mechanisms merely because they are mentioned above.

Distinguish verified facts from assumptions, mandatory requirements from optional improvements, and confirmed risks from speculative concerns.

Identify residual risks, limitations and decisions requiring my input.

Keep the analysis proportional to the complexity and risk of the task.

Do not modify any files. Wait for my approval.


# Design Implementation

Implement the approved solution.

Requirements:

1. Follow the approved design, acceptance criteria and existing architectural conventions.
2. Keep the implementation focused and avoid unnecessary refactoring.
3. Reuse existing components, services and utilities where appropriate.
4. Preserve relevant system invariants and handle identified edge cases and failure scenarios.
5. Add or update meaningful tests covering the expected behaviour and relevant acceptance criteria.
6. Do not introduce unnecessary dependencies.
7. Preserve existing functionality and unrelated changes.
8. Do not weaken assertions, disable tests or bypass validation merely to achieve passing results.
9. Seek my approval before making material deviations from the approved design or expanding the scope.

Before finishing:

- Inspect the resulting changes.
- Run the relevant tests and applicable validation checks using the project's established tooling.
- Report the files modified.
- Explain the implementation and significant technical decisions.
- Identify any assumptions, deviations or limitations.
- Report the commands executed and their actual results, including failed or skipped checks.
- Distinguish pre-existing failures from implementation-related failures where evidence permits.

Use isolated, non-production environments for testing.

Do not claim that something works unless it has been verified.


# Independent AI Review

Act as an independent senior software engineer reviewing this implementation.

Original requirements:
[INSERT REQUIREMENTS]

Approved design and acceptance criteria:
[INSERT APPROVED DESIGN AND ACCEPTANCE CRITERIA]

Review the current changes against the original requirements, approved design, system invariants and existing codebase conventions.

Inspect relevant surrounding code, dependencies, tests and affected execution paths rather than reviewing the diff in isolation.

Review for:

1. Missing requirements, logical errors and incorrect assumptions.
2. Unhandled edge cases and failure scenarios.
3. Race conditions, concurrency and transaction management issues.
4. Data integrity, consistency and domain-specific correctness issues.
5. Security vulnerabilities.
6. Performance and scalability concerns.
7. Unnecessary complexity or architectural inconsistencies.
8. Missing, inadequate or misleading tests.
9. Potential regressions and backward compatibility issues.
10. Unintended changes or deviations from the approved design.

Proactively identify additional risks specific to the problem.

For each finding, provide:

- Severity.
- Relevant file and line references.
- Description of the issue.
- Conditions under which it occurs.
- Potential impact.
- Recommended corrective action.

Prioritize actionable findings. Distinguish confirmed issues from speculative concerns, and mandatory corrections from optional improvements.

Do not manufacture findings for the sake of criticism. Explicitly state when no significant issues are identified.

Do not modify any files.


# Review Findings Resolution

An independent code review has produced the following findings:

[INSERT CODE REVIEW FINDINGS]

Evaluate each finding against the original requirements, approved design and actual implementation.

For each finding:

- Determine whether it is valid, partially valid, invalid or requires further investigation.
- Explain your assessment using evidence from the codebase.
- Identify the severity and potential impact.
- Recommend the simplest appropriate corrective action where necessary.
- Identify any trade-offs or potential regressions introduced by the correction.

Distinguish mandatory corrections from optional improvements.

Do not blindly accept or dismiss review findings.

Do not modify any files. Wait for my approval before implementing corrective changes.


# Validation

Perform final validation of the implementation against the original requirements, approved design and acceptance criteria.

- Independently evaluate the acceptance criteria against the original requirements.
- Verify that all mandatory requirements and relevant system invariants are satisfied.
- Inspect all task-related changes, including staged, unstaged and relevant untracked files, for unintended changes, defects and unnecessary complexity.
- Verify that confirmed code review findings have been addressed.
- Evaluate test quality, coverage and meaningfulness, not merely whether tests pass.
- Identify missing tests for relevant edge cases, failure scenarios, concurrency, idempotency, data integrity, security and regressions.
- Proactively identify domain-specific validation requirements.
- Execute relevant tests, linting, type checks, builds and targeted runtime checks using the project's established tooling.
- Perform additional validation for high-risk behaviour where applicable.
- Compare results against the established baseline where available.
- Distinguish pre-existing failures from regressions introduced by the implementation.

Report:

1. Acceptance criteria, verification status and supporting evidence.
2. Commands executed and actual results, including failed or skipped checks.
3. Confirmed defects and missing coverage.
4. Unverified behaviour, limitations and residual risks.
5. Recommended corrective actions.
6. Final readiness assessment: Ready, Ready with limitations, or Not ready.

Keep validation proportional to the complexity and risk of the task. Use isolated, non-production environments.

Do not perform destructive operations or expose sensitive information.

Do not claim success without sufficient evidence. Do not modify implementation files or tests without my approval.
