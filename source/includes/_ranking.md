# Visa Restrictions Index

Where you can find out the passport ranking based on the [Henley & Partners Visa Restrictions Index 2017](https://en.wikipedia.org/wiki/Henley_%26_Partners_Visa_Restrictions_Index).

> Json response for AR (Argentina):

```json
{
  "rank": 20,
  "count": 154,
  "sharing": 2
}
```

### HTTP Request

`GET /v1/ranking/{country_code}`

<aside class="notice">
Country code follows the <b>Alpha-2 code</b> form specified by <a href="https://en.wikipedia.org/wiki/ISO_3166-1" target="_blank">ISO 3166-1</a>.
</aside>

### HTTP Response

Code | Description
---- | ----------
200 | Success
404 | Country not found
500 | Internal Server Error
503 | Service Unavailable

### Response

* **rank**: passport ranking
* **count**: number of countries allowed to enter
* **sharing**: number of countries that share the same ranking position
