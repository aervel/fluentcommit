# Fluent Commit Specification

**Fluent Commit** provides a standardized approach for writing commit messages. The goal is to enhance clarity,
consistency, and collaboration across development teams by structuring commit messages in a predictable format.

---

## Structure

The Fluent Commit message is divided into three primary sections: Header, Body, and Footer. Each section plays a crucial
role in conveying the purpose and details of the commit.

```
<header>

<body>

<footer>
```

---

### Header

The Header is the first and most critical part of the commit message. It provides a quick overview of the change. The
header has the following format:

```
<type>(<scope>): <description>
```

#### Type

Defines the category of the change. Use one of the predefined types to classify the commit:

<details>
<summary>Docs</summary>

### Description

Commits that involve changes to documentation files or comments. This can include README updates,
changes to code comments, or any other form of documentation relevant to the project.

### Purpose

To ensure that documentation stays accurate and up-to-date, reflecting any changes in the code or project setup.

### Common Changes

- Updating the README with new installation instructions.
- Correcting typos in documentation.
- Adding or modifying code comments.

```
docs: Update README with setup instructions for new contributors
docs(api): Fix typo in API documentation
```

**docs**

- [ ] Identify documentation files or comments that need updating.
- [ ] Make sure changes are clearly explained and accurate.

</details>

---

<details>
<summary>Feature</summary>

### Description

Commits that introduce new features or functionality to the project. These are additions that enhance
the capabilities of the software.

### Purpose

To track the introduction of new capabilities and track their development separately from other types of
changes.

### Common Changes

- Implementing a new user authentication mechanism.
- Adding a new module or service to the application.
- Introducing a new user interface component.

```
feature(auth): Implement OAuth2 authentication flow
feature(ui): Add new dashboard widget for analytics
```

**feature**

- [ ] Define the new feature being introduced.
- [ ] Ensure that the feature is fully implemented and tested.

</details>

---

<details>
<summary>Patch</summary>

### Description

Commits that fix bugs or resolve issues in existing code. These are usually minor fixes that address
problems affecting the current functionality.

### Purpose

To address issues that need to be resolved without introducing new features or making major changes.

### Common Changes

- Fixing a bug in a function or method.
- Correcting errors in existing logic.
- Resolving problems with existing features.

```
patch(api): Fix incorrect response handling in user endpoint
patch(ui): Correct display issue with user profile images
```

**patch**

- [ ] Identify the bug or issue being fixed.
- [ ] Confirm that the fix resolves the issue without introducing new problems.

</details>

---

<details>
<summary>Build</summary>

### Description

Commits related to changes in the build or configuration process. This includes modifications to
build scripts, package dependencies, or other configuration files.

### Purpose

To manage changes that affect the build and deployment processes, ensuring that the project is configured
correctly.

### Common Changes

- Adding or updating Docker configurations.
- Modifying build scripts or continuous integration pipelines.
- Changing package dependencies or version constraints.

```
build: Add configuration for Webpack to handle new asset types
build(ci): Update Travis CI configuration for deployment
```

**build**

- [ ] Check changes to build or configuration files.
- [ ] Ensure that the build and deployment processes are correctly updated.

</details>

---

<details>
<summary>Test</summary>

### Description

Commits that add or modify tests in the project. This includes writing new unit tests, integration
tests, or adjusting existing tests to ensure code quality and functionality.

### Purpose

To maintain or improve test coverage and ensure that new or existing features are thoroughly tested.

### Common Changes

- Adding new unit tests for a specific function.
- Updating test cases to cover new features.
- Fixing broken tests or improving test reliability.

```
test: Add unit tests for new authentication service methods
test(api): Update API tests to handle new error responses
```

**test**

- [ ] Add or update tests to cover new or existing functionality.
- [ ] Verify that tests run correctly and cover the necessary code paths.

</details>

---

<details>
<summary>Refactor</summary>

### Description

Commits that involve code restructuring or cleanup without changing the functionality. This is

focused on improving code readability, maintainability, or performance.

### Purpose

To improve code quality by restructuring or cleaning up code without introducing new features or fixing
bugs.

### Common Changes

- Renaming variables or functions for clarity.
- Refactoring code to simplify complex logic.
- Reorganizing code into more manageable modules or files.

```
refactor: Rename variables for clarity in authentication module
refactor: Extract common functions into utility module
```

**refactor**

- [ ] Determine what code needs to be cleaned up or reorganized.
- [ ] Ensure that refactoring does not change the existing functionality.

</details>

---

<details>
<summary>Upgrade</summary>

### Description

Commits that involve upgrading or improving existing code for better performance or usability. This
includes optimizations, enhancements, or refactoring aimed at improving the overall quality.

### Purpose

To enhance the performance, efficiency, or user experience of the codebase.

### Common Changes

- Improving query performance or reducing latency.
- Updating libraries or frameworks to newer versions.
- Enhancing existing features for better usability.

```
upgrade: Optimize database queries for better performance
upgrade: Update to latest version of React for improved stability
```

**upgrade**

- [ ] Identify areas for performance improvement or code upgrades.
- [ ] Test the upgraded code to ensure that it meets performance and usability goals.

</details>

---

#### Scope

Describes the part of the project affected by the change. **A scope is optional**.

`auth`, `api`, `UI`

#### Description

A brief, imperative description of the change. Use lowercase and avoid punctuation at the end.

`add user login functionality`

```
feature(auth): Add JWT authentication
```

---

### Body

The Body of the commit message provides a more detailed explanation of the change. It is separated from the Header by a
blank line.

```
<description of the change>

<motivation>

<details of the change>

<impact or side effects>
```

#### Description of the Change

Briefly summarize what was done.

`Implement user authentication using JWT. Added login and registration endpoints.`

#### Motivation

Explain why the change was necessary.

`To enhance security and support scalable user authentication.`

#### Details of the Change

Provide specific information about what was altered.

`Created JWT tokens for authentication and added middleware for token validation.`

#### Impact or Side Effects

Mention any potential impacts or side effects of the change.

`This may affect the login flow and requires updating client applications to handle JWT tokens.`

The following is an example of a body in a commit message:

```
Implement user authentication using JWT. Added login and registration endpoints.

This change enhances security by using JWT tokens for user authentication, which are more scalable than previous methods.

The authentication process now includes token generation and validation middleware. Updated the user service to handle tokens.

May impact the login flow. Ensure client applications are updated to support JWT.
```

---

### Footer

The Footer is used for additional information, such as references to related issues or tickets.

```
<reference to related issues or tickets>
```

#### Issue Closing

Reference issues or tickets that this commit addresses or closes.

`Closes #123`

#### Additional Information

Any other relevant information or notes.

`See also #456 for related discussion`

```
Closes #45
See also #123 for related discussions
```

---

Here’s how a full commit message would look:

```
feature(auth): Add JWT authentication

Implement user authentication using JWT. Added login and registration endpoints.

This change enhances security by using JWT tokens for user authentication, which are more scalable than previous methods.

The authentication process now includes token generation and validation middleware. Updated the user service to handle tokens.

May impact the login flow. Ensure client applications are updated to support JWT.

Closes #45
See also #123 for related discussions
```

---

## Checklist

1. **Header**

- [ ] Choose the correct type (`docs`, `feature`, `patch`, etc.)
- [ ] Define the scope (if applicable)
- [ ] Write a concise, imperative description

2. **Body**

- [ ] Provide a clear description of the change
- [ ] Explain the motivation for the change
- [ ] Detail what was altered
- [ ] Note any potential impacts or side effects

3. **Footer**

- [ ] Reference any related issues or tickets
- [ ] Include additional information if necessary

By following this specification, you ensure that commit messages are informative, consistent, and useful for all team
members.