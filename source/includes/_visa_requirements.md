# Visa Requirements

Where you can find out Visa Requirements and Currency Exchange information given a country code `from` and a country code `to`.

Country code follows the `Alpha-2 code` form specified by [ISO 3166-1](https://en.wikipedia.org/wiki/ISO_3166-1).

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

<aside class="success">
Remember — it should be an authenticated request using your API Key!
</aside>

### HTTP Request

`GET https://api.smartbackpacker.com/v1/traveling/{from}/to/{to}`

### Query Parameters

Parameter | Description
--------- | ------- | -----------
baseCurrency | The base currency to get information about currency exchange. Must follow the [ISO 4217](https://en.wikipedia.org/wiki/ISO_4217) form.

### Response

* countryName: the name of the `to` country
* countryCode: the ISO country code of the `to` country
* visaRequirements
  - visaCategory: any of the categories defined below
  - description: a string value
* exchangeRate:
  - baseCurrency: the currency set in the request
  - foreignCurrency: the currency of the `to` country
  - rate: a floating point number indicating the exchaange rate

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

