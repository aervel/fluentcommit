# Commit Type Guide

This guide outlines how to craft clear and effective commit messages, ensuring each message accurately reflects the
changes made to the project. Each type of commit message serves a specific purpose, making the commit history organized
and comprehensible.

## `Docs`

The `docs` type is used for changes related to documentation files or comments. This includes updates to README files,
code comments, or any other documentation relevant to the project.

#### Purpose

To keep all documentation up-to-date and ensure it accurately reflects the current state of the codebase and project
setup.

#### Motivation

Well-maintained documentation helps contributors and users understand the project and its usage.

| Advantage                  | Description                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **Improved** Documentation | Keeps documentation up-to-date with the latest changes in the codebase, ensuring it remains relevant and accurate. |
| **Enhanced** Clarity       | Helps new contributors and users understand the project setup, usage, and changes more clearly.                    |
| Error **Correction**       | Corrects typos and errors in documentation, reducing confusion and improving the quality of project resources.     |

## `Feature`

The `feature` type is used for commits that introduce new features or functionalities to the project.

#### Purpose

To track the development of new capabilities and ensure they are clearly documented.

#### Motivation

Adding new features enhances the project's functionality and provides visibility into its evolution.

| Advantage                          | Description                                                                                                                |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| **Clear Tracking** of New Features | Clearly distinguishes new features from other types of changes, making it easier to track the addition of functionalities. |
| **Better Planning** and Review     | Facilitates planning and review processes by making new features easily identifiable.                                      |
| Feature **Visibility**             | Enhances visibility into the evolution of the project by highlighting new capabilities.                                    |

## `Patch`

The `patch` type is used for minor fixes or bug resolutions in existing code.

#### Purpose

To address issues affecting current functionality without introducing new features.

#### Motivation

Maintaining stability by fixing bugs and minor issues ensures a smoother user experience.

| Advantage                      | Description                                                                                                                                   |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| **Focus** on Bug Fixes         | Clearly separates bug fixes from other types of changes, ensuring that minor issues are addressed without mixing them with feature additions. |
| **Stability** Maintenance      | Helps maintain stability by ensuring that bug fixes are documented and tracked separately.                                                    |
| **Simplified** Troubleshooting | Makes it easier to identify and address issues in the codebase by isolating them from other changes.                                          |

## `Build`

The `build` type is used for changes related to build processes and configurations.

#### Purpose

To manage modifications that affect how the project is built and deployed.

#### Motivation

Keeping build and deployment configurations up-to-date ensures that the project is properly built and deployed.

| Advantage                    | Description                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| **Configuration** Management | Keeps track of changes related to build processes, configurations, and deployment setups.                                      |
| **Improved** Build Process   | Ensures that updates to build tools or CI configurations are documented, facilitating smoother build and deployment processes. |
| **Clear Build** Changes      | Helps in managing and understanding changes in build scripts, making it easier to troubleshoot build issues.                   |

## `Test`

The `test` type is used for adding or modifying tests within the project.

#### Purpose

To maintain or improve test coverage and ensure that code changes are properly tested.

#### Motivation

Effective testing helps maintain code quality and functionality by identifying issues early.

| Advantage                    | Description                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------|
| **Maintained** Test Coverage | Ensures that changes are accompanied by appropriate tests, maintaining or improving test coverage.               |
| **Enhanced** Code Quality    | Helps in identifying and fixing issues early by keeping tests updated and relevant.                              |
| **Clear** Testing Efforts    | Makes it easier to track and review testing efforts, ensuring that new features and changes are properly tested. |

## `Refactor`

The `refactor` type is used for code restructuring or cleanup without changing functionality.

#### Purpose

To improve code readability, maintainability, or performance without affecting existing behavior.

#### Motivation

Refactoring enhances the organization and clarity of the codebase, making it easier to maintain.

| Advantage                              | Description                                                                                             |
|----------------------------------------|---------------------------------------------------------------------------------------------------------|
| **Improved** Code Quality              | Focuses on improving code readability, maintainability, and performance without changing functionality. |
| **Easier** Code Maintenance            | Makes the codebase easier to understand and maintain by organizing and cleaning up code.                |
| **Separation** from Functional Changes | Clearly differentiates between changes that affect functionality and those that improve code structure. |

## `Upgrade`

The `upgrade` type is used for improving existing code or updating dependencies.

#### Purpose

To enhance performance, efficiency, or update libraries/frameworks.

#### Motivation

Keeping the project optimized and up-to-date with the latest versions of dependencies.

| Advantage                              | Description                                                                                                             |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| **Enhanced Performance** and Stability | Keeps the project up-to-date with the latest versions of libraries and frameworks, enhancing performance and stability. |
| **Improved Efficiency**                | Helps in optimizing existing code and dependencies, leading to better performance.                                      |
| **Clear Update** Tracking              | Clearly tracks upgrades and improvements, making it easier to manage and review dependency changes.                     |

## Usage Guide

This table summarizes the appropriate commit types for various scenarios. With this table you can exercise your mind to
learn **Fluent Commit**.

| Scenario                      | docs | feature | patch | build | test | refactor | upgrade |
|-------------------------------|------|---------|-------|-------|------|----------|---------|
| Adding new functionalities    |      | ✓       |       |       |      |          |         |
| Adding new tests              |      |         |       |       | ✓    |          |         |
| Creating API endpoints        |      | ✓       |       |       |      |          |         |
| Creating CI/CD pipelines      |      |         |       | ✓     |      |          |         |
| Creating deployment scripts   |      |         |       | ✓     |      |          |         |
| Creating documentation        | ✓    |         |       |       |      |          |         |
| Enhancing performance         |      |         |       |       |      |          | ✓       |
| Fixing bugs                   |      |         | ✓     |       |      |          |         |
| Implementing authentication   |      | ✓       |       |       |      |          |         |
| Improving UI/UX               |      |         |       |       |      | ✓        |         |
| Increasing performance        |      |         |       |       |      |          | ✓       |
| Integrating third-party APIs  |      | ✓       |       |       |      |          |         |
| Migrating database            |      |         |       | ✓     |      |          |         |
| Monitoring application health |      |         |       | ✓     |      |          |         |
| Optimizing database queries   |      |         |       |       |      | ✓        | ✓       |
| Refactoring code              |      |         |       |       |      | ✓        |         |
| Resolving security issues     |      |         | ✓     |       |      |          |         |
| Setting up monitoring tools   |      |         |       | ✓     |      |          |         |
| Setting up project structure  |      | ✓       |       |       |      |          |         |
| Updating build scripts        |      |         |       | ✓     |      |          |         |
| Updating configuration files  | ✓    |         |       |       |      |          |         |
| Updating markdown files       | ✓    |         |       |       |      |          |         |
| Updating txt files            |      |         |       |       |      |          | ✓       |
| Updating json files           |      |         |       | ✓     |      |          | ✓       |
| Upgrading dependencies        |      |         |       | ✓     |      |          | ✓       |
| Writing unit tests            |      |         |       |       | ✓    |          |         |