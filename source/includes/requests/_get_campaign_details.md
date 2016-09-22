## Get campaign details

> Example of campaign details call:

```shell
curl -X GET
-H "Authorization: <ACCESS_TOKEN>"
https://api.worldcoo.com/v3/ngos/2454de2c-cb31-44e5-83bd/campaigns/a9fb530d-6270-0cc7-e8a8
```

> Example of add donation response:

```json
{
  "id": "a9fb530d-6270-0cc7-e8a8",
  "alias": "Demo capaign",
  "ngo_id": "2454de2c-cb31-44e5-83bd",
  "status": "opened",
  "location": [
    {
      "country": "ESP",
      "name": "Spain"
    }
  ],
  "category": "children",
  "currency": "EUR",
  "budget": {
    "funding": 100000,
    "others": 10000,
    "transport": 50000,
    "materials": 10000,
    "providers": 35000,
    "team": 5000,
    "initial_funding": 4000,
    "other_donations": 200,
    "donations_in_ecommerce": 3000,
    "amount_in_ecommerce": 56
  },
  "beneficiaries": {
    "direct": 400,
    "indirect": 1000
  },
  "starting_date": 1464277166,
  "ending_date": null,
  "media": [
      {
        "location": "http://cdn.worldcoo.com/campaigns/8720fdd5-1b10-a4c8-a614/logos/logoexamplengo1.png",
        "type": "image/png"
      }
  ],
  "counters": {
    "donors": 467,
    "donated": 5035
  },
  "texts": {
    "name": "NGO Campaign 1",
    "name_short": "Cmpgn 1",
    "resume": "This is an example of campaign description.",
    "activities": "",
    "objectives": "",
    "benefits": "",
    "call_to_action": "",
    "worldcoo_url": ""
  }
}
```

`GET https://api.worldcoo.com/v3/ngos/{{ngo_id}}/campaigns/{{campaign_id}}`

### Request

#### HTTP Headers

Header name | Required | default | Description
---------- | ------- | ------- | -------
Authorization | yes | NA | Authorization token provided by WorldCoo
[Accept-Language](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.4) | No | en | iso 639-2/b language code.

### Response

`200 Ok`

##### Response body

- **id** *string*
- **alias** *string*
- **location** *value map*
  - **country_code** *[CountryCode](#country-standar)*
  - **city_name** *string*
- **[category](#campaign-categories)** *string*
- **ngo_id** *string*
- **[status](#campaign-statuses)** *string*
- **languages** *[LanguageCode](#language-standar) list*
- **currency** *[CurrencyCode](#currency-standar)*
- **budget** *numbers map* 
  - **funding** *number*
  - **others** *number*
  - **transport** *number*
  - **materials** *number*
  - **providers** *number*
  - **team** *number*
  - **initial_funding** *number*
  - **other_donations** *number*
  - **donations_in_ecommerce** *number*
  - **amount_in_ecommerce** *number*
- **beneficiaries** *numbers map*
  - **direct** *number*
  - **indirect** *number*
- **starting_date** *[Date](#date-standar) | null*
- **ending_date** *[Date](#date-standar) | null*
- **media** *list* Linked media resources
  - **type** *string* MIME Type of the linked resource.
  - **location** *string* URI of the linked resource.
- **counters** *numbers map* Campaign current funding.
  - **donors** *number*
  - **donated** *number*
- **texts** *strings map* These are localized texts.
  - **name** *string*
  - **name_short** *string*
  - **resume** *string*
  - **activities** *string*
  - **objectives** *string*
  - **benefits** *string*
  - **call_to_action** *string*
  - **worldcoo_url** *string*
