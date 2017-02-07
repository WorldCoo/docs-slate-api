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
  "status": "active",
  "location": {
    "country_code": "ESP",
    "city_name": "Barcelona"
  },
  "category": "water_and_energy",
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
  "media": {
          "eaba63b5-d7be-4de8-a53e-283c9104a9a6": {
              "versions": {
                  "S": {
                      "height": 200,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/eaba63b5-d7be-4de8-a53e-283c9104a9a6.1479739685956.S.jpg",
                      "width": 150,
                      "type": "image/jpeg"
                  },
                  "L": {
                      "height": 800,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/eaba63b5-d7be-4de8-a53e-283c9104a9a6.1479739685956.L.jpg",
                      "width": 600,
                      "type": "image/jpeg"
                  },
                  "M": {
                      "height": 400,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/eaba63b5-d7be-4de8-a53e-283c9104a9a6.1479739685956.M.jpg",
                      "width": 300,
                      "type": "image/jpeg"
                  },
                  "XL": {
                      "height": 1599,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/eaba63b5-d7be-4de8-a53e-283c9104a9a6.1479739685956.XL.jpg",
                      "width": 1200,
                      "type": "image/jpeg"
                  }
              },
              "height": 1354,
              "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/eaba63b5-d7be-4de8-a53e-283c9104a9a6.1479739685956.original.jpg",
              "width": 1016,
              "type": "image/jpeg"
          },
          "89bfea45-5704-4e4b-9aab-b80c3ac1fa9c": {
              "versions": {
                  "S": {
                      "height": 107,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/89bfea45-5704-4e4b-9aab-b80c3ac1fa9c.1479739676674.S.jpg",
                      "width": 150,
                      "type": "image/jpeg"
                  },
                  "L": {
                      "height": 426,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/89bfea45-5704-4e4b-9aab-b80c3ac1fa9c.1479739676674.L.jpg",
                      "width": 600,
                      "type": "image/jpeg"
                  },
                  "M": {
                      "height": 213,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/89bfea45-5704-4e4b-9aab-b80c3ac1fa9c.1479739676674.M.jpg",
                      "width": 300,
                      "type": "image/jpeg"
                  },
                  "XL": {
                      "height": 852,
                      "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/89bfea45-5704-4e4b-9aab-b80c3ac1fa9c.1479739676674.XL.jpg",
                      "width": 1200,
                      "type": "image/jpeg"
                  }
              },
              "height": 852,
              "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/campaigns/f6425839-1e6f-4dd2-8d4d-593d61f5437f/media/89bfea45-5704-4e4b-9aab-b80c3ac1fa9c.1479739676674.original.jpg",
              "width": 1200,
              "type": "image/jpeg"
          }
      },
  "counters": {
    "donors": 467,
    "donated": 5035
  },
  "texts": {
    "name": "NGO Campaign 1",
    "name_short": "Cmpgn 1",
    "resume": "This is an example of campaign description.",
    "resume_short": "campaign description",
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
[Accept-Language](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.4) | No | ENG | iso 639-2/b language code.

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
- **media** *media map* Linked media resources
      - **media_id** *string*
          - **type** *string*
          - **location** *string*
          - **width** *number*
          - **height** *number*
          - **versions** *versions map*
            - **version_key** *string*
                - **type** *string*
                - **location** *string*
                - **width** *number*
                - **height** *number*
- **counters** *numbers map* Campaign current funding.
  - **donors** *number*
  - **donated** *number*
- **texts** *strings map* These are localized texts.
  - **name** *string*
  - **name_short** *string*
  - **resume** *string*,
  - **resume_short** *string*
  - **activities** *string*
  - **objectives** *string*
  - **benefits** *string*
  - **call_to_action** *string*
  - **worldcoo_url** *string*
