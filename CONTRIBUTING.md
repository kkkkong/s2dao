# Contributing to S2Dao

Thanks for your interest in contributing to S2Dao! We welcome bug reports, documentation improvements, tests, and code contributions. This document explains the preferred process for contributing so your work can be merged quickly.

## Table of contents

- How can I contribute?
- Reporting bugs
- Suggesting enhancements
- Your first code contribution
- Development setup
- Building and running tests
- Coding style
- Commit messages
- Pull request process
- Code of Conduct

## How can I contribute?

Pick from one of the following:

- Open an issue to report a bug or request a feature.
- Send a pull request (PR) with a small, focused change and tests.
- Improve documentation or add examples.

## Reporting bugs

When filing an issue, please include:

- A short, descriptive title.
- Steps to reproduce the problem.
- Expected and actual behavior.
- Environment details (OS, JDK version).
- A minimal code sample or stack trace if available.

Label the issue appropriately (bug, enhancement, question) if you can.

## Suggesting enhancements

Describe the enhancement and the motivation. Explain the use case and provide examples where appropriate. If you have a design or API proposal, include a short discussion of alternatives and why your suggestion is better.

## Your first code contribution

We recommend starting with a small change: fix a typo, improve a test, or tidy up documentation. If you want to work on a bigger feature, open an issue first to discuss the approach.

## Development setup

1. Fork the repository on GitHub.
2. Clone your fork:

```bash
git clone https://github.com/<your-username>/s2dao.git
cd s2dao
```

3. Add the upstream remote to keep your fork up-to-date:

```bash
git remote add upstream https://github.com/kkkkong/s2dao.git
```

4. Create a topic branch for your work:

```bash
git checkout -b feat/short-description
```

Note: This project is Java-based. It may use Maven or Gradle as a build tool — check the repository root for `pom.xml` (Maven) or `build.gradle` / `settings.gradle` / `gradlew` (Gradle).

## Building and running tests

If the project uses Maven:

```bash
# run all tests
mvn test

# build package
mvn clean package
```

If the project uses Gradle (wrapper recommended):

```bash
# run tests
./gradlew test

# build
./gradlew build
```

Run a single test class with Maven:

```bash
mvn -Dtest=YourTestClass test
```

Or with Gradle:

```bash
./gradlew test --tests "com.example.YourTestClass"
```

## Coding style

- Follow standard Java conventions: package naming, camelCase for methods/variables, PascalCase for types.
- Keep methods small and focused.
- Write JUnit tests for bug fixes and new features.
- Document public APIs with Javadoc comments.

Optional tools you can use locally:

- google-java-format or another formatter to keep consistent formatting.
- Checkstyle/SpotBugs if present in the project configuration.

## Commit messages

Write clear, concise commit messages. A recommended format:

```
Short (50 chars or less) summary

More detailed explanatory text, if necessary. Wrap at 72 characters.
```

Reference issues in commits/PRs when appropriate: "Fixes #123" or "Relates to #456".

## Pull request process

1. Fork, create a branch, commit changes, push to your fork.
2. Open a pull request against the `main` (or default) branch of `kkkkong/s2dao`.
3. In the PR description include:
   - What the change does and why.
   - Any related issues.
   - How to run tests and verify the change.
4. Keep PRs small and focused. If requested, make updates to address review feedback.

Automated checks (CI) may run — ensure all tests pass before requesting review.

## Code of Conduct

Be respectful and constructive. By participating in this project you agree to follow a basic code of conduct: be kind, helpful, and avoid harassment. If the project has a `CODE_OF_CONDUCT.md`, follow it; otherwise follow common community norms.

---

Thanks again for contributing! If you're unsure where to start, check the open issues or open a discussion/issue describing what you'd like to work on.
