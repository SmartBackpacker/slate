# Errors

The Smart Backpacker API uses the following error codes:

> All the errors have the following json form:

```json
{
  "code": 100
  "error": "Country not found: Mars"
}
```

Code | Meaning
---- | -------
100 | Entity not found (Country, Airline, etc).
101 | Cannot search traveling to the same country.
