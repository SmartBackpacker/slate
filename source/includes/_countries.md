# Countries

List of all the countries in the world including `Country Code`, `Name` and `Currency`. You can also filter by `Schengen` countries.

> Json response for all the countries (200):

```bash
curl "https://api.smartbackpackerapp.com/v1/countries"
```

```json
[
  {
    "code": "AR",
    "name": "Argentina",
    "currency": "ARS"
  },
  {
    "code": "IE",
    "name": "Ireland",
    "currency": "EUR"
  }
]
```

> Json response for the Schengen countries (26):

```bash
curl "https://api.smartbackpackerapp.com/v1/countries?query=schengen"
```

```json
[
  {
    "code": "AT",
    "name": "Austria",
    "currency": "EUR"
  }
]
```

### HTTP Request

`GET /v1/countries`

### Optional Query Parameters

Parameter | Value | Description
--------- | ------| -----------
query | schengen | Retrieves only the countries that belong to the Schengen Area

### HTTP Response

Code | Description
---- | ----------
200 | Success
500 | Internal Server Error
503 | Service Unavailable

### Response

* **code**: Alpha-2 Country Code [ISO 3166-1Alpha](https://en.wikipedia.org/wiki/ISO_3166-1)
* **name**: Country Name
* **currency**: Country Currency [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217)
