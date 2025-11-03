## Frontend → Backend

### Endpoint 1
```
GET /api/example
```

**Parameters:**
```json
{
  "param1": "string"
}
```

**Response (200):**
```json
{
  "status": "success",
  "data": {}
}
```

**Response (error):**
```json
{
  "status": "error",
  "message": "Error message"
}
```

### Endpoint 2
```
POST /api/example
```

**Body:**
```json
{
  "param1": "string"
}
```

**Response (201):**
```json
{
  "status": "success",
  "data": {}
}
```
