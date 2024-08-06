# Fluent Commit Specification

**Fluent Commit** provides a standardized approach for writing commit messages. The goal is to enhance clarity,
consistency, and collaboration across development teams by structuring commit messages in a predictable format.

## Structure

The [Fluent Commit message](#fluent-commit-message) is divided into three primary sections: Header, Body, and Footer.
Each section plays a crucial
role in conveying the purpose and details of the commit.

```
<header>

<body>

<footer>
```

### Header

The Header is the first and most critical part of the commit message. It provides a quick overview of the change. The
header has the following format:

```
<type>(<scope>): <description>
```

#### Type

Defines the category of the change. Use one of the predefined types to classify the commit:

| Type           | Description                                                                                                                                                                                      |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```docs```     | Commits that involve changes to documentation files or comments. This can include README updates, changes to code comments, or any other form of documentation relevant to the project.          |
| ```feature```  | Commits that introduce new features or functionality to the project. These are additions that enhance the capabilities of the software.                                                          |
| ```patch```    | Commits that fix bugs or resolve issues in existing code. These are usually minor fixes that address problems affecting the current functionality.                                               |
| ```build```    | Commits related to changes in the build or configuration process. This includes modifications to build scripts, package dependencies, or other configuration files.                              |
| ```test```     | Commits that add or modify tests in the project. This includes writing new unit tests, integration tests, or adjusting existing tests to ensure code quality and functionality.                  |
| ```refactor``` | Commits that involve code restructuring or cleanup without changing the functionality. This is focused on improving code readability, maintainability, or performance.                           |
| ```upgrade```  | Commits that involve upgrading or improving existing code for better performance or usability. This includes optimizations, enhancements, or refactoring aimed at improving the overall quality. |

[Learn More](COMMIT_TYPE_GUIDE)

#### Scope

Describes the part of the project affected by the change. A scope is **optional**, but **recommended**.

`auth` `api` `UI`

#### Description

A brief, imperative description of the change. Use lowercase and avoid punctuation at the end.

`add user login functionality`

```
feature(auth): Add JWT authentication
```

<blockquote>
<p>
When writing a <strong>Pull Request</strong>, the title of that Pull Request must follow the <strong>same structure and 
rulers</strong> of a commit header
</p>
<p>The header is used as the title. Must contain all elements of a header: <i>type, scope (if applicable) and description</i></p>
</blockquote>

## Body

The Body of the commit message provides a more detailed explanation of the change. It is separated from the Header by a
blank line.

```
<description of the change>

<motivation>

<details of the change>

<impact or side effects>
```

<blockquote>
In a <strong>Pull Request</strong>, the body and footer of a commit message are used as the <strong>description</strong>
of the Pull Request. It must contain all elements of a body as described above.
</blockquote>

#### Description of the Change

Briefly summarize what was done.

`Implement user authentication using JWT. Added login and registration endpoints.`

<blockquote>
In a <strong>Pull Request</strong>, is called <strong>Description</strong>
</blockquote>

#### Motivation

Explain why the change was necessary.

`To enhance security and support scalable user authentication.`

#### Details of the Change

Provide specific information about what was altered.

`Created JWT tokens for authentication and added middleware for token validation.`

<blockquote>
In a <strong>Pull Request</strong>, receives the name in plural of type in header. For example, if the type is 
<strong>feature</strong>, the name of this section is <strong>Features</strong>
</blockquote>

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

<blockquote>
In a <strong>Pull Request</strong>, is called <strong>Impact</strong>
</blockquote>

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

<blockquote>
In a <strong>Pull Request</strong> the footer is used to reference. Can be used to reference issues, pull requests,
related discussions, reviewers, Co-Authors, etc.
</blockquote>

## Commit Checklist

1. **Header**

- [ ] Choose the correct type (`docs`, `feature`, `patch`, `...`)
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

___

###### Fluent Commit Message

A Fluent Commit Message, is a structured commit or pull request message that follows the Fluent Commit Specification.
Normally, it consists of a header, body, and footer. That [structure](#structure) is the same used in the Fluent Commit
Specification.