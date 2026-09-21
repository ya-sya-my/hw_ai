# Project Requirements

## Goal

Create a small local mock API server based on an OpenAPI specification.

The project must demonstrate that API responses can be generated locally from an OpenAPI/Swagger specification without a real backend or database.

## Requirements

1. Create an OpenAPI 3 specification in `openapi.yaml`.

2. The OpenAPI specification must contain at least two endpoints:
   - `POST /login`
   - `GET /users/{id}`

3. Define simple and realistic request and response schemas for these endpoints.

4. Use a local mock server that can generate API responses from the OpenAPI specification.

5. The mock server must generate responses based on `openapi.yaml`.

6. Do not create a real backend.

7. Do not use a database.

8. Keep the project small and simple. Do not add unnecessary frameworks, services, features, or dependencies.

9. Add a simple `README.md` with:
    - installation instructions
    - how to start the mock server
    - example requests for both endpoints

10. Verify that:
    - the mock server starts successfully;
    - `POST /login` responds;
    - `GET /users/{id}` responds.

## Technical Requirements

- Node.js
- OpenAPI 3
- Use a local mock server that can generate API responses from the OpenAPI specification.
- Choose the simplest suitable tool or library for the local mock server.
- Do not add unnecessary dependencies or architecture.

## Simplicity

- Keep the project small and easy to understand.
- Choose the simplest implementation that satisfies the requirements.
- Do not create a real backend or database.
- Do not add authentication, Docker, CI/CD, frontend, or other features unless explicitly required.
- Avoid unnecessary files, dependencies, and abstractions.

## Restrictions

- Do not implement authentication logic.
- Do not create a real database.
- Do not connect to external APIs.
- Do not create a real backend.
- Do not add functionality that is not required for this task.

## Expected Project Structure

The final project should remain small and should contain approximately:
- `package.json`
- `openapi.yaml`
- `README.md`
- necessary configuration files only