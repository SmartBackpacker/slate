# Errors

The Smart Backpacker API uses the following error codes:

> All the errors have the following json form (API v2 only):

```json
{
  "error": 100
  "value": "Country not found: Mars"
}
```

Code | Meaning
---- | -------
100 | Country not found.
101 | Airline not found
666 | Forbidden -- Only authorized requests with the provided API Token.
