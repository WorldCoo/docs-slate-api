## Add donation

> Example of add donation call:

```shell
curl -X POST
-H "Authorization: <ACCESS_TOKEN>"
-H "Content-Type: application/json"
https://api.worldcoo.com/v3/donations
--data '{"campaign_id": "a9fb530d-6270-0cc7-e8a8", "amount": 5, "currency": "EUR", "order_code": "9638467"}'
```

> Example of add donation response:

```json
{
    "id": "17a10455-120d-e767-0206",
    "amount": 5,
    "currency": "EUR",
    "order_code": "9638467",
    "campaign_counters": {
        "total_donated": 60,
        "target": 50000
    }
}
```

`POST https://api.worldcoo.com/v3/donations`

### Request

#### HTTP Headers

Header name | Required | default | Description
---------- | ------- | ------- | -------
Authorization | yes | NA | Authorization token provided by WorldCoo
[Accept-Language](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.4) | No | en | iso 639-2/b language code.

#### Body

- **campaign_id** *string*: Required campaign idenfifier
- **amount** *number*
- **currency** *[CurrencyCode](#currency-standar)*
- **order_code** *string*: Internal client reference regarding this donation

### Response

`201 Created`

##### Body
- **id** *string*
- **amount** *number*
- **currency** *[CurrencyCode](#currency-standar)*
- **order_code** *string*
- **campaign_counters**
    - **total_donated** *number*. Amount received expressed in EUR.
    - **target** *number*. Target amount expressed in EUR.
    
### Errors:
- **401 unauthorizedCampaign**: You have not access to that campaign
- **404 campaignNotFound**: campaign with id '${entityId}' doesn't exists
- **422 campaignNotStarted**: The campaign you are attempting to access is not started
- **422 campaignFunded**: The campaign you are attempting to access is funded
- **422 campaignDisabled**: The campaign you are attempting to access is disabled
