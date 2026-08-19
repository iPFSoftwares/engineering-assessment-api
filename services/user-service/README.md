# User Service

The User Service owns user identity and access-related capabilities.

At a high level, it is responsible for:

- Registering users.
- Authenticating users.
- Managing user information.
- Representing whether a user is allowed to access the system.
- Providing other services with the user information they legitimately need.

It does not own projects or project membership.

The implementation, API contracts, persistence model, security approach, and
integration method are left to the candidate.
