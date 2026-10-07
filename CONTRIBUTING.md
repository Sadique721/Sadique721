# Contributing to @Sadique721 Projects

Thank you for your interest in contributing! All development in this ecosystem follows **Spec-Driven Development (SDD)** powered by **[GitHub Spec-Kit (github/spec-kit)](https://github.com/github/spec-kit)**.

## How to Contribute

1. **Constitution First**: Review [.specify/memory/constitution.md](.specify/memory/constitution.md) for non-negotiable architectural invariants (test gates, zero hardcoded secrets, clean layering).
2. **Open a Feature Spec**: Submit a GitHub Issue using the `🌱 Feature Specification (SDD)` template before writing code.
3. **Follow the SDD Lifecycle**:
   - Define **WHAT & WHY** in `.specify/specs/`.
   - Architect the technical plan in `.specify/plans/`.
   - Break down atomic tasks in `.specify/tasks/`.
4. **Pull Requests**:
   - Ensure all automated unit and integration tests pass (`mvn test` / `pytest` / `npm test`).
   - Use our Pull Request Template and complete the SDD Convergence Checklist.
   - PR diffs must be minimal, scoped, and strictly additive.
