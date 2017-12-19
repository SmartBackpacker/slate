# Health Information

Where you can find out information about mandatory, recommended and optional vaccines, in addition to health travel alerts provided by [CDC (Centers for Disease Control and Prevention)](https://www.cdc.gov/).

> Json response for AR (Argentina):

```json
{
	"vaccinations": {
		"mandatory": [],
		"recommendations": [{
				"disease": "Hepatitis A",
				"description": "CDC recommends this vaccine because you can get hepatitis A through contaminated food or water in Argentina, regardless of where you are eating or staying.",
				"diseaseCategories": [
					"GetVaccinated",
					"EatAndDrinkSafely"
				],
			},
			{
				"disease": "Typhoid",
				"description": "You can get typhoid through contaminated food or water in Argentina. CDC recommends this vaccine for most travelers, especially if you are staying with friends or relatives, visiting smaller cities or rural areas, or if you are an adventurous eater.",
				"diseaseCategories": [
					"GetVaccinated",
					"EatAndDrinkSafely"
				],
			}
		],
		"optional": [{
				"disease": "Hepatitis B",
				"description": "You can get hepatitis B through sexual contact, contaminated needles, and blood products, so CDC recommends this vaccine if you might have sex with a new partner, get a tattoo or piercing, or have any medical procedures.",
				"diseaseCategories": [
					"GetVaccinated",
					"AvoidSharingBodyFluids",
					"AvoidNonSterileEquipment"
				],
			},
			{
				"disease": "Rabies",
				"description": "Although rabies can be found in dogs, bats, and other mammals in Argentina, it is not a major risk to most travelers. CDC recommends this vaccine only for these groups: Travelers involved in outdoor and other activities in remote areas that put them at risk for animal bites (such as adventure travel and caving). People who will be working with or around animals (such as veterinarians, wildlife professionals, and researchers). People who are taking long trips or moving to remote areas in Argentina Children, because they tend to play with animals, might not report bites, and are more likely to have animal bites on their head and neck.",
				"diseaseCategories": [
					"GetVaccinated",
					"KeepAwayFromAnimals"
				],
			},
			{
				"disease": "Yellow Fever",
				"description": "Yellow fever is a risk in certain parts of Argentina, so CDC recommends the yellow fever vaccine for travelers 9 months of age or older to these areas. For more information on this recommendation, see yellow fever recommendations and requirements for Argentina.Your doctor can help you decide if this vaccine is right for you based on your travel plans.",
				"diseaseCategories": [
					"GetVaccinated",
					"PreventBugBites"
				],
			}
		],
	},
	"notices": {
		"alertLevel": "LevelTwo",
		"alerts": [{
			"title": "Zika Virus in Argentina",
			"link": "",
			"description": "Zika virus (or Zika) has been reported. Public health officials have reported that mosquitoes are infected with Zika and spreading it to people."
		}],
	}
}
```

### HTTP Request

`GET /v1/health/{country_code}`

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

* **vaccinations**:
  - **mandatory**: a list of the required vaccines to travel to the destination country
  - **recommendations**: a list of the recommended vaccines
  - **optional**: a list of the optional vaccines depending on the situation of the traveler
* **notices**: 
  - **alertLevel**: either NoAlert, LevelOne or LevelTwo. Level 1 indicates `Practice Usual Precautions` (green warning) and Level 2 `Practice Enhanced Precautions` (yellow warning).
  - **alerts**: a list of alerts
     - **title**: title of the alert
     - **link**: website link of the alert
     - **description**: the description

* **vaccine** format:
  - **disease**: the disease name
  - **description**: the description
  - **diseaseCategories**: any of the disease categories

### Disease Category

* AvoidNonSterileEquipment
* TakeAntimalarialMeds
* GetVaccinated
* AvoidSharingBodyFluids
* ReduceExposureToGerms 
* PreventBugBites 
* EatAndDrinkSafely 
* KeepAwayFromAnimals 
* UnknownDiseaseCategory
