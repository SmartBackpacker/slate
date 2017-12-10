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

`GET https://api.smartbackpacker.com/v1/ranking/{country_code}`

### Response

* rank: passport ranking
* count: amount of countries allowes to enter
* sharing: if the ranking position is shared with other countries, then here's how many of them, otherwise just zero
