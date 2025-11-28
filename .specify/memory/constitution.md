# [PROJECT_NAME] Constitution
<!-- Example: Spec Constitution, TaskFlow Constitution, etc. -->

## Core Principles

### [PRINCIPLE_1_NAME]
<!-- Example: I. Library-First -->
[PRINCIPLE_1_DESCRIPTION]
<!-- Example: Every feature starts as a standalone library; Libraries must be self-contained, independently testable, documented; Clear purpose required - no organizational-only libraries -->

### [PRINCIPLE_2_NAME]
<!-- Example: II. CLI Interface -->
[PRINCIPLE_2_DESCRIPTION]
<!-- Example: Every library exposes functionality via CLI; Text in/out protocol: stdin/args → stdout, errors → stderr; Support JSON + human-readable formats -->

### [PRINCIPLE_3_NAME]
<!-- Example: III. Test-First (NON-NEGOTIABLE) -->
[PRINCIPLE_3_DESCRIPTION]
<!-- Example: TDD mandatory: Tests written → User approved → Tests fail → Then implement; Red-Green-Refactor cycle strictly enforced -->

### [PRINCIPLE_4_NAME]
<!-- Example: IV. Integration Testing -->
[PRINCIPLE_4_DESCRIPTION]
<!-- Example: Focus areas requiring integration tests: New library contract tests, Contract changes, Inter-service communication, Shared schemas -->

### [PRINCIPLE_5_NAME]
<!-- Example: V. Observability, VI. Versioning & Breaking Changes, VII. Simplicity -->
[PRINCIPLE_5_DESCRIPTION]
<!-- Example: Text I/O ensures debuggability; Structured logging required; Or: MAJOR.MINOR.BUILD format; Or: Start simple, YAGNI principles -->

## [SECTION_2_NAME]
<!-- Example: Additional Constraints, Security Requirements, Performance Standards, etc. -->

[SECTION_2_CONTENT]
<!-- Example: Technology stack requirements, compliance standards, deployment policies, etc. -->

## [SECTION_3_NAME]
<!-- Example: Development Workflow, Review Process, Quality Gates, etc. -->

[SECTION_3_CONTENT]
<!-- Example: Code review requirements, testing gates, deployment approval process, etc. -->

## Governance
<!-- Example: Constitution supersedes all other practices; Amendments require documentation, approval, migration plan -->

[GOVERNANCE_RULES]
<!-- Example: All PRs/reviews must verify compliance; Complexity must be justified; Use [GUIDANCE_FILE] for runtime development guidance -->

**Version**: [CONSTITUTION_VERSION] | **Ratified**: [RATIFICATION_DATE] | **Last Amended**: [LAST_AMENDED_DATE]
<!-- Example: Version: 2.1.1 | Ratified: 2025-06-13 | Last Amended: 2025-07-16 -->

# Core guidelines

This document defines the global rules and operating procedures for the Multi-Agent Team. All Agents (Project Lead, PM Lead, Engineering Lead) must strictly adhere to these principles.

## 1. The Golden Rule: Human-in-the-Loop (HITL)
- **Ask, Don't Guess:** If you encounter ambiguity, missing requirements, or conflicting instructions, you MUST pause and ask the user for clarification.
- **Clarification Protocol:** You are authorized to ask clarifying questions to the user OR to other agents.
- **No Hallucinations:** Do not invent business rules or technical constraints.

## 2. Workflow & Data Safety
- **Continuous Save:** Immediately after generating or modifying ANY file, you must **Commit and Push** to the current feature branch. Do not wait for a full phase to complete.
- **Batched Review:**
    - **PM Lead:** Open a Pull Request only when the *entire* Spec Package (Requirements, Research, Functional Spec) is complete.
    - **Engineering Lead:** Open Pull Requests for code implementation. Do not open PRs for planning docs unless requested.

## 3. Folder Structure Discipline
- **Features are for Paperwork:** All Specs, Plans, and Task lists go into `features/<feature-name>/`.
- **Src is for Code:** All implementation code goes into `src/`, organized by architecture (not by feature folder).
- **Agents are Global:** Agent definitions live in `.github/agents/`.

## 4. GitHub Integration
- **Tracking:** Every feature must have a Tracking Issue.
- **Tasks:** Every engineering task must be a GitHub Issue linked to the Tracking Issue.
- **Traceability:** All PRs must reference the Issue they close (e.g., `Closes #123`).

## 5. Language Agnosticism vs. Specificity
- **PM Lead:** Must remain technology-agnostic. Focus on user value and behavior.
- **Engineering Lead:** Must be technology-specific. Adhere strictly to `ARCHITECTURE.md`.
