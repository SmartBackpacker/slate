# Visa Requirements

Where you can find out Visa Requirements and Currency Exchange information given a country code `from` and a country code `to`.

> Json response for traveling from AR (Argentina) to AU (Australia):

```bash
curl "https://api.smartbackpackerapp.com/v1/traveling/AR/to/AU?baseCurrency=EUR"
```

```json
{
  "countryName": "Australia",
  "countryCode": "AU",
  "visaRequirements": {
    "visaCategory": "VisaRequired",
    "description": "May apply online (Online Visitor e600 visa). Transit visa is not required."
  },
  "exchangeRate": {
    "baseCurrency": "EUR",
    "foreignCurrency": "AUD",
    "rate": 1.5055
  }
}
```

<aside class="notice">
Country code follows the <b>Alpha-2 code</b> form specified by <a href="https://en.wikipedia.org/wiki/ISO_3166-1" target="_blank">ISO 3166-1</a>.
</aside>

### HTTP Request

`GET /v1/traveling/{from}/to/{to}`

### Query Parameters

Parameter | Description
--------- | -----------
baseCurrency | Currency code to get information about currency exchange

<aside class="notice">
Currency code should be as defined by <a href="https://en.wikipedia.org/wiki/ISO_4217" target="_blank">ISO 4217</a>.
</aside>

### HTTP Response

Code | Description
---- | ----------
200 | Success
400 | Whenever `to` and `from` are the same country
404 | Country not found
500 | Internal Server Error
503 | Service Unavailable

### Response

* **countryName**: the name of the `to` country
* **countryCode**: the ISO country code of the `to` country
* **visaRequirements**:
  - **visaCategory**: any of the categories defined below
  - **description**: a string value
* **exchangeRate**:
  - **baseCurrency**: the currency set in the request (ISO 4217)
  - **foreignCurrency**: the currency of the `to` country
  - **rate**: a floating point number indicating the exchange rate

### Visa Category

* VisaNotRequired
* VisaWaiverProgram
* AdmissionRefused
* TravelBanned
* VisaRequired
* VisaDeFactoRequired
* ElectronicVisa
* ElectronicVisitor
* ElectronicTravelAuthority
* FreeVisaOnArrival
* VisaOnArrival
* ElectronicVisaPlusVisaOnArrival
* OnlineReciprocityFee
* MainlandTravelPermit
* HomeReturnPermitOnly
* UnknownVisaCategory

