# API Documentation

Welcome to the API documentation. This guide covers authentication, endpoints, and best practices.

## Overview

Our REST API allows you to programmatically interact with our platform. All API requests should be made to:

```
https://api.example.com/v1/
```

## Authentication

### API Keys

Generate an API key from your account settings:

1. Navigate to Settings > API Keys
2. Click **Generate New Key**
3. Name your key (e.g., "Production Server")
4. Copy the key immediately (it won't be shown again)
5. Store securely

### Using Your API Key

Include your API key in the request header:

```bash
curl -H "Authorization: Bearer YOUR_API_KEY" \
  https://api.example.com/v1/projects
```

## Rate Limits

**Free Tier:**
- 1,000 requests per hour
- 10,000 requests per day

**Pro Tier:**
- 5,000 requests per hour
- 100,000 requests per day

**Enterprise:**
- Custom limits available

Rate limit headers are included in every response:

```
X-RateLimit-Limit: 5000
X-RateLimit-Remaining: 4999
X-RateLimit-Reset: 1640995200
```

## Common Endpoints

### Get Projects

```http
GET /v1/projects
```

**Response:**

```json
{
  "projects": [
    {
      "id": "proj_123",
      "name": "My Project",
      "created_at": "2026-04-01T12:00:00Z"
    }
  ]
}
```

### Create Project

```http
POST /v1/projects
```

**Request Body:**

```json
{
  "name": "New Project",
  "description": "Project description",
  "private": true
}
```

## Error Handling

The API uses standard HTTP status codes:

- `200 OK` - Request succeeded
- `201 Created` - Resource created
- `400 Bad Request` - Invalid request
- `401 Unauthorized` - Invalid API key
- `404 Not Found` - Resource not found
- `429 Too Many Requests` - Rate limit exceeded
- `500 Internal Server Error` - Server error

**Error Response Format:**

```json
{
  "error": {
    "code": "invalid_request",
    "message": "Project name is required"
  }
}
```

## Best Practices

1. **Cache responses** when appropriate
2. **Handle rate limits** gracefully with exponential backoff
3. **Use webhooks** instead of polling when possible
4. **Keep API keys secure** - never commit them to version control
5. **Use HTTPS** for all requests

## Support

For API support, contact api-support@example.com or visit our developer forum.

## Changelog

See [API Changelog](./api-changelog.md) for version history and updates.
