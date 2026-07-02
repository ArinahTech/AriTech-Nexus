# Contributing to AriTech NEXUS

Thank you for your interest in contributing to AriTech NEXUS.

This document outlines the development workflow, coding standards, and contribution guidelines used throughout the project.

---

# Project Vision

AriTech NEXUS is an enterprise-grade ISP and Hotspot Management Platform focused on providing a scalable, secure, and maintainable solution for Internet Service Providers and wireless network operators.

Every contribution should align with the project's goals of:

- Reliability
- Security
- Scalability
- Maintainability
- Performance
- Clean Architecture

---

# Development Workflow

Development follows a structured workflow.

1. Update your local repository.
2. Create or switch to the appropriate branch.
3. Implement the required feature or fix.
4. Test your changes.
5. Commit using clear commit messages.
6. Push your branch.
7. Open a Pull Request for review.

---

# Branch Naming Convention

Use descriptive branch names.

Examples:

```
feature/authentication

feature/customer-module

feature/billing

feature/dashboard

bugfix/login-validation

bugfix/payment-calculation

docs/api-design

refactor/database
```

---

# Commit Message Guidelines

Write concise and meaningful commit messages.

Examples:

```
Initialize Next.js frontend

Implement JWT authentication

Add customer management module

Implement billing service

Create voucher generation API

Add MikroTik integration

Update project documentation

Fix invoice calculation bug
```

Avoid generic messages such as:

```
Update

Fix

Changes

Test
```

---

# Coding Standards

## General

- Write clean and readable code.
- Keep functions focused on a single responsibility.
- Avoid duplicated logic.
- Use meaningful variable names.
- Remove unused code before committing.

---

## TypeScript

- Prefer interfaces where appropriate.
- Enable strict typing.
- Avoid using `any`.
- Use descriptive type names.

---

## NestJS

- Organize code by feature modules.
- Keep controllers lightweight.
- Place business logic in services.
- Validate incoming requests using DTOs.
- Use dependency injection throughout the application.

---

## Next.js

- Use reusable components.
- Keep pages focused on presentation.
- Fetch data through API services.
- Separate UI from business logic.
- Follow the App Router conventions.

---

## Database

- Use Prisma ORM.
- Follow naming conventions consistently.
- Use foreign keys where appropriate.
- Avoid redundant data.
- Keep database migrations under version control.

---

# Documentation

Whenever a major feature is introduced, update the relevant documentation.

Examples include:

- Architecture
- API Design
- Database Design
- SRS
- Development Roadmap
- README
- CHANGELOG

Documentation should evolve together with the codebase.

---

# Testing

Before submitting changes:

- Ensure the project builds successfully.
- Verify existing functionality is unaffected.
- Test new functionality thoroughly.
- Resolve all known errors before committing.

Future versions will include automated testing using:

- Jest
- Supertest
- Playwright

---

# Pull Requests

Each Pull Request should include:

- A clear description.
- Related issue (if applicable).
- Summary of changes.
- Testing performed.
- Screenshots for UI changes.

Pull Requests should remain focused on a single feature or fix.

---

# Issue Reporting

When reporting issues, include:

- Expected behavior
- Actual behavior
- Steps to reproduce
- Screenshots (if applicable)
- Browser or operating system information

---

# Code Review

Every contribution should be reviewed for:

- Code quality
- Performance
- Security
- Maintainability
- Documentation updates

Constructive feedback is encouraged throughout the review process.

---

# Security

Do not commit:

- Passwords
- API keys
- Database credentials
- JWT secrets
- Environment files
- Private certificates

Sensitive information must always be stored using environment variables.

---

# License

By contributing to AriTech NEXUS, you agree that your contributions will be licensed under the project's MIT License.

---

# Thank You

Thank you for helping improve AriTech NEXUS.

Every contribution—whether code, documentation, testing, or feedback—helps build a more reliable and scalable platform for Internet Service Providers and hotspot businesses.