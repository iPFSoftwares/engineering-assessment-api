# Engineering Assessment API

## Objective

Build the backend for a simple project management application.

The system should allow users to register, authenticate, create and manage
projects, and collaborate with other registered users.

This assessment is intended to demonstrate your ability to turn requirements
into a working backend solution. You are expected to make and explain the
technical decisions that are not explicitly prescribed.

## Functional Requirements

The system should support:

- User registration.
- User authentication.
- Retrieving relevant user information.
- Creating projects.
- Viewing projects accessible to the authenticated user.
- Viewing an individual project.
- Updating and deleting projects.
- Adding registered users to a project.
- Removing users from a project.
- Distinguishing between project owners and project members.
- Restricting operations based on authentication, ownership, and membership.
- Returning meaningful responses when operations cannot be completed.

The exact API endpoints, request formats, response formats, and data models are
left to you.

## Repository Structure

The backend should be organized as independently runnable services:

```text
services/
├── user-service/
│   └── README.md
└── project-service/
    └── README.md
```

Each service directory contains a short description of its high-level boundary.

You may organize the implementation inside each service as you consider
appropriate.

## Service Boundaries

### User Service

See [`services/user-service/README.md`](services/user-service/README.md).

The User Service owns user identity and access-related capabilities.

It should not own projects or project membership.

### Project Service

See [`services/project-service/README.md`](services/project-service/README.md).

The Project Service owns projects, project ownership, and project membership.

It may reference users but should not own user accounts, credentials, or
authentication data.

## Technical Constraints

- Use Java and Spring Boot.
- Use JPA/Hibernate for persistence.
- Use a relational database.
- Implement the services under the `services/` directory.
- Each service should be independently runnable.
- Include meaningful automated tests.
- Do not commit credentials or environment-specific secrets.

You may choose any additional libraries, tools, and infrastructure you consider
appropriate.

## Technical Decisions

You are responsible for deciding:

- The internal structure of each service.
- API endpoints and contracts.
- Data models and relationships.
- Database organization and ownership.
- Authentication and authorization design.
- How services communicate.
- How service failures are handled.
- Validation and error-response design.
- Transaction boundaries.
- Testing strategy.
- Configuration and local development setup.

Document important decisions and trade-offs in this README.

There is no requirement to introduce infrastructure or patterns that the
solution does not need.

## API Consumers

The services should expose APIs that can be consumed by external clients.

A separate client application may consume these APIs, but its implementation,
framework, interface, and state-management requirements are outside the scope
of this repository.

Document the information an API consumer needs, including:

- How to authenticate.
- Available operations.
- Required request data.
- Important response formats.
- Relevant error behaviour.

API documentation may be provided in any clear and usable form.

## Quality Expectations

We will consider:

- Correctness of the implemented behaviour.
- Clarity and maintainability of the code.
- Appropriate separation of responsibilities.
- Security and access-control enforcement.
- Persistence and data-integrity decisions.
- Handling of invalid input and failure cases.
- Quality and relevance of automated tests.
- Ease of running and reviewing the application.
- Ability to explain the submitted solution.

A smaller, complete solution is preferred over unnecessary complexity.

## Deliverables

Your submission should include:

- Runnable source code for both services.
- Database setup or migrations.
- Automated tests covering important behaviour.
- Instructions for configuring and running the application.
- Instructions for running the tests.
- API documentation or usage examples.
- A short explanation of your architecture and major decisions.
- Known limitations or incomplete work.

The repository should not depend on undocumented local configuration.

## Timebox

Spend approximately eight focused hours on the assessment.

If you do not complete everything within the timebox, submit the working
solution and document:

- What remains incomplete.
- What you would implement next.
- Any decisions you would reconsider with more time.

Prioritization and reasoning are part of the assessment.

## Review Discussion

Be prepared to:

- Demonstrate the working application.
- Explain the service boundaries.
- Explain how authentication and authorization work.
- Discuss data ownership and service communication.
- Describe how the system behaves when one service is unavailable.
- Explain the most important tests.
- Discuss what you would change before using the system in production.
- Make a small change to the application during the review.
