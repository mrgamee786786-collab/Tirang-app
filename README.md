{
  "info": {
    "name": "Colour Trading API",
    "_postman_id": "12345678-abcd-efgh-ijkl-1234567890ab",
    "description": "Postman collection for Colour Trading prototype backend (with variables)",
    "schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json"
  },
  "item": [
    {
      "name": "Signup",
      "request": {
        "method": "POST",
        "header": [
          { "key": "Content-Type", "value": "application/json" }
        ],
        "url": { "raw": "{{baseUrl}}/api/signup", "host": ["{{baseUrl}}"], "path": ["api", "signup"] },
        "body": {
          "mode": "raw",
          "raw": "{\n  \"name\": \"Test User\",\n  \"email\": \"test@example.com\",\n  \"password\": \"123456\"\n}"
        }
      }
    },
    {
      "name": "Login",
      "request": {
        "method": "POST",
        "header": [
          { "key": "Content-Type", "value": "application/json" }
        ],
        "url": { "raw": "{{baseUrl}}/api/login", "host": ["{{baseUrl}}"], "path": ["api", "login"] },
        "body": {
          "mode": "raw",
          "raw": "{\n  \"email\": \"test@example.com\",\n  \"password\": \"123456\"\n}"
        }
      }
    },
    {
      "name": "Get Profile (/me)",
      "request": {
        "method": "GET",
        "header": [
          { "key": "Authorization", "value": "Bearer {{token}}" }
        ],
        "url": { "raw": "{{baseUrl}}/api/me", "host": ["{{baseUrl}}"], "path": ["api", "me"] }
      }
    },
    {
      "name": "Place Bet",
      "request": {
        "method": "POST",
        "header": [
          { "key": "Content-Type", "value": "application/json" },
          { "key": "Authorization", "value": "Bearer {{token}}" }
        ],
        "url": { "raw": "{{baseUrl}}/api/bet", "host": ["{{baseUrl}}"], "path": ["api", "bet"] },
        "body": {
          "mode": "raw",
          "raw": "{\n  \"color\": \"red\",\n  \"amount\": 10\n}"
        }
      }
    },
    {
      "name": "Bet History",
      "request": {
        "method": "GET",
        "header": [
          { "key": "Authorization", "value": "Bearer {{token}}" }
        ],
        "url": { "raw": "{{baseUrl}}/api/history", "host": ["{{baseUrl}}"], "path": ["api", "history"] }
      }
    }
  ],
  "variable": [
    { "key": "token", "value": "" }
  ]
}
