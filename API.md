# API Documentation

This document describes all available API endpoints in the yaya99 project.

## Base URL

```
http://localhost:3000
```

## Endpoints

### 1. Welcome Endpoint

**Endpoint:** `GET /`

**Description:** Returns welcome message and app information.

**Response:**
```json
{
  "message": "Welcome to yaya99",
  "version": "1.0.0",
  "timestamp": "2026-05-20T22:00:00.000Z"
}
```

**Status Code:** `200 OK`

**Example:**
```bash
curl -X GET http://localhost:3000/
```

---

### 2. Health Check Endpoint

**Endpoint:** `GET /health`

**Description:** Returns the health status of the server.

**Response:**
```json
{
  "status": "ok"
}
```

**Status Code:** `200 OK`

**Example:**
```bash
curl -X GET http://localhost:3000/health
```

---

## Error Handling

The API returns standard HTTP status codes and error messages.

### 404 Not Found

When requesting an undefined endpoint:

```json
{
  "error": "Not Found"
}
```

**Status Code:** `404 Not Found`

### 500 Internal Server Error

When an unexpected error occurs:

```json
{
  "error": "Internal Server Error",
  "message": "Error details (only in development mode)"
}
```

**Status Code:** `500 Internal Server Error`

---

## Request/Response Format

- **Content-Type:** `application/json`
- All responses are in JSON format
- All timestamps are in ISO 8601 format

---

## Rate Limiting

Currently, there are no rate limits. This may change in future versions.

---

## Authentication

Currently, no authentication is required. Future endpoints may require API keys or tokens.

---

## Versioning

The API version is included in the welcome response. Breaking changes will be announced with version updates.

Current version: **1.0.0**

---

## Future Endpoints

The following endpoints are planned for future releases:

- `POST /api/users` - Create a new user
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

---

## Support

For API issues or feature requests, please open an issue on the [GitHub repository](https://github.com/yacoubkaba77-png/yaya99/issues).
