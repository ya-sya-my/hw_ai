# Mock API Server

A simple local mock API server that generates responses from an OpenAPI 3 specification, demonstrating API behavior without a real backend or database.

## Installation

Ensure you have Node.js 14+ installed, then install dependencies:

```bash
npm install
```

## Running the Mock Server

Start the mock server on localhost:3000:

```bash
npm start
```

The server will listen on `http://127.0.0.1:3000` and generate responses based on the `openapi.yaml` specification.

## API Endpoints

### POST /login

Authenticate a user and receive a token.

**Request:**
```bash
curl -X POST http://localhost:3000/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "user@example.com",
    "password": "password123"
  }'
```

**Example Response (200 OK):**
```json
{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9",
  "user": {
    "id": 1,
    "email": "user@example.com",
    "name": "John Doe"
  }
}
```

### GET /users/{id}

Retrieve a user's details by their ID.

**Request:**
```bash
curl http://localhost:3000/users/1
```

**Example Response (200 OK):**
```json
{
  "id": 1,
  "email": "user@example.com",
  "name": "John Doe",
  "created_at": "2026-01-01T00:00:00Z"
}
```

## Project Structure

```
.
├── package.json       # Project configuration and dependencies
├── openapi.yaml       # OpenAPI 3.0 specification for the mock API
└── README.md          # This file
```

## How It Works

This project uses **Prism**, a lightweight mock server that automatically generates responses from the OpenAPI specification. No backend code or database is required—responses are generated directly from the schema definitions in `openapi.yaml`.

## Development

For development with dynamic response generation, use:

```bash
npm run dev
```

This enables additional Prism features like dynamic examples.
