# Project Service

The Project Service owns projects and project membership.

At a high level, it is responsible for:

- Creating and managing projects.
- Recording project ownership.
- Adding and removing project members.
- Controlling access based on ownership and membership.
- Returning projects visible to the current user.

It may reference users, but it does not own user accounts, credentials, or user
authentication data.

The implementation, API contracts, persistence model, authorization approach,
and communication with the User Service are left to the candidate.
