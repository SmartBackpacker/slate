# Baggage Policy

Where you can find Airline's Baggage Policy information.

> Json response for the Airline `Air France`:

```bash
curl "https://api.smartbackpackerapp.com/v1/airlines?name=Air France"
```

```json
{
  "name": "Air France",
  "baggagePolicy": {
    "allowance": [
      {
        "baggageType": "CabinBag",
        "kgs": null,
        "size": {
          "height": 55,
          "width": 35,
          "depth": 25
        }
      },
      {
        "baggageType": "SmallBag",
        "kgs": null,
        "size": {
          "height": 40,
          "width": 30,
          "depth": 15
        }
      }
   ],
   "extra": "The combined weight of your hand baggage item and accessory must not exceed 12 kg or 18 kg, depending on your travel cabin. You can take 1 or 2 hand baggage items depending on your flight cabin, as well as 1 accessory.",
   "website": "https://www.airfrance.fr/FR/en/common/guidevoyageur/pratique/bagages-cabine-airfrance.htm"
  }
}
```

### HTTP Request

`GET /v1/airlines`

### Query Parameters

Parameter | Description
--------- | ------- | -----------
name | The exact name of the airline, case sensitive.

### HTTP Response

Code | Description
---- | ----------
200 | Success
404 | Airline not found
500 | Internal Server Error
503 | Service Unavailable

### Response

* **name**: The airline's name
* **baggagePolicy**
  - **allowance**: a list of baggage allowance
    - **baggageType**: any of `SmallBag`, `CabinBag` or `CheckedBag`
    - **kgs**: an integer number
    - **size**: 
      - **height**: an integer number
      - **width**: an integer number
      - **depth**: an integer number

<aside class="warning">The field <b>kgs</b> could be null.</aside>

