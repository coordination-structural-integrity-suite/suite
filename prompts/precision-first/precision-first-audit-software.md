# Software Specification Precision Audit
Copy everything below the line, paste it into any AI chat, and attach or paste the specification (API contract, requirements document, technical design document, schema definition, or similar).
---
You are auditing the attached software specification for precision deficits using the Precision-First Design Standard (CC BY 4.0, Regis Lloyd Chapman). A precision deficit is any requirement, definition, or interface that cannot be evaluated by an independent tester using only the specification and observable system behavior.

Check for these seven common precision failures in software specifications:

1. Untestable acceptance criteria: requirements that depend on the original author's intent rather than observable behavior (e.g., "the system should handle errors gracefully," "provide a good user experience," "respond in a timely manner"). For each one found, propose a criterion an independent tester can evaluate without access to the author.
2. Loosely typed definitions: places where a string type is used where a typed enum is possible, where an "other" or "miscellaneous" category exists without an overflow procedure, or where a data format is described in prose rather than in a schema. For each one found, propose the precise type.
3. Unclassified error handling: error responses that use generic categories ("unexpected error," "internal server error," "something went wrong") without distinguishing error classes by structural signature, detectability, and recovery procedure. For each one found, propose a classification.
4. Ambiguous state boundaries: places where the specification does not clearly distinguish between states that the system treats differently (e.g., "active" vs. "enabled," "pending" vs. "processing," "failed" vs. "error"). For each one found, propose operational definitions that make the boundary falsifiable.
5. Interface contracts with implicit assumptions: API endpoints, event schemas, or data contracts that assume context the consumer may not have, or that leave behavior unspecified for valid inputs (e.g., "returns a list of results" without specifying ordering, pagination, empty-set behavior, or maximum size). For each one found, list the unspecified behaviors and propose defaults.
6. Inaction invisibility: detection mechanisms, alerting systems, or error reporting pipelines that produce outputs but provide no way for an independent observer to determine whether those outputs were acted on, without the cooperation of the responsible party. For each one found, propose a specification that makes inaction visible without requiring actor cooperation.
7. Single-mechanism critical properties: critical system properties (e.g., authentication, data integrity, access control, rate limiting) that depend on a single protective mechanism with no structurally independent backup. For each one found, identify the critical property, name the single mechanism protecting it, and propose at least one structurally distinct backup mechanism whose failure would be detectable independently.

Output the results as a precision deficit map organized by failure type, with the deficits most likely to cause bugs, disputes, or integration failures first.

Full standard: https://github.com/durgadasji/standards
