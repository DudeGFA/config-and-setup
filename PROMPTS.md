# Codebase Exploration

I want you to help me understand this codebase before making any modifications.

Please:
1. Identify the primary application architecture and technology stack.
2. Explain the main directories and their responsibilities.
3. Identify the application entry points.
4. Trace the relevant request or execution flow.
5. Identify the database models and their relationships where relevant.
6. Identify existing testing conventions.
7. Highlight any architectural patterns or conventions I should preserve.

Do not modify any files.

Present your findings in a structured and concise manner. Reference the relevant files and functions.


# Problem Investigation

Investigate the issue described below:

[INSERT PROBLEM]

Trace the relevant execution path and identify potential root causes.

For each potential cause:
- Explain the underlying mechanism.
- Identify the relevant files and functions.
- Explain the conditions under which it could occur.
- Suggest how we could reproduce or verify it.

Do not modify any files yet.

Prioritize evidence from the existing implementation over assumptions.


# Solution Design

Based on our investigation, propose the simplest reliable solution that satisfies the requirements.

- Identify the requirements, constraints, assumptions and system invariants.
- Evaluate viable approaches and their trade-offs.
- Identify applicable engineering principles, design patterns and domain-specific best practices.
- Consider data integrity, transactions, concurrency, locking, idempotency, financial correctness, database performance, security, scalability, distributed system behaviour, fault tolerance and observability where relevant.
- Proactively identify additional considerations specific to the problem.
- Analyze relevant edge cases, failure scenarios and potential regressions.
- Recommend a pragmatic solution and justify the design decisions.
- Outline the implementation and testing strategy.

Preserve existing architectural conventions. Avoid unnecessary complexity and do not introduce mechanisms merely because they are mentioned above.

Distinguish verified facts from assumptions, mandatory requirements from optional improvements, and confirmed risks from speculative concerns.

Keep the analysis proportional to the complexity and risk of the task.

Do not modify any files. Wait for my approval.


# Design Implementation

Implement the solution we have discussed.

Requirements:
1. Follow the existing architectural conventions.
2. Keep the implementation focused and avoid unnecessary refactoring.
3. Handle relevant edge cases and failure scenarios.
4. Add or update tests covering the expected behaviour.
5. Do not introduce unnecessary dependencies.
6. Preserve existing functionality.

Before finishing:
- Run the relevant tests.
- Report the files modified.
- Explain the implementation.
- Identify any assumptions or limitations.
- Report any tests that failed and why.

Do not claim that something works unless it has been verified.


# AI Review

Act as an independent senior engineer reviewing this implementation.

Original requirement:
[INSERT REQUIREMENT]

Review the current changes for:

1. Logical errors and incorrect assumptions.
2. Edge cases that are not handled.
3. Race conditions and concurrency issues, where relevant.
4. Security vulnerabilities.
5. Performance concerns.
6. Unnecessary complexity.
7. Missing or inadequate tests.
8. Potential regressions.

Do not modify any files.

Prioritize actionable findings and reference the relevant files and code sections. Distinguish confirmed issues from speculative concerns.



# Validation

Perform final validation of the implementation against the original requirements and approved design.

- Establish acceptance criteria independently of the implementation.
- Verify that all mandatory requirements and relevant system invariants are satisfied.
- Inspect the complete Git diff for unintended changes, defects and unnecessary complexity.
- Verify that confirmed code review findings have been addressed.
- Evaluate test quality, coverage and meaningfulness, not merely whether tests pass.
- Identify missing tests for relevant edge cases, failure scenarios, concurrency, idempotency, data integrity, security and regressions.
- Proactively identify domain-specific validation requirements.
- Execute relevant tests, linting, type checks, builds and targeted runtime checks using the project's established tooling.
- Perform additional validation for high-risk behaviour where applicable.

Report:
1. Acceptance criteria and verification status.
2. Commands executed and actual results.
3. Confirmed defects and missing coverage.
4. Unverified behaviour, limitations and residual risks.
5. Recommended corrective actions.
6. Final readiness assessment.

Keep validation proportional to the complexity and risk of the task. Use isolated, non-production environments.

Do not claim success without evidence. Do not modify any files without my approval.
