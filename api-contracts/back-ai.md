## Backend → AI Backend

### Endpoint 1
```
POST /api/process
```

**Body:**
```json
{
  "input": "string",
  "model": "string"
}
```

**Response (200):**
```json
{
  "status": "success",
  "output": "string"
}
```

**Response (error):**
```json
{
  "status": "error",
  "message": "Error message"
}
```
