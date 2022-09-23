## Add batch donation

> Example of add a donation batch call :

```shell
curl -X POST
-H "Authorization: <ACCESS_TOKEN>"
-H "Content-Type: application/json"
https://api.worldcoo.com/v3/donations/batch
--data '{"items":[ {"id":"cffffdbb-9a0f-4c90-9763-dc3a7e4f9feb","campaign_id": "a9fb530d-6270-0cc7-e8a8", "channelId": "channelOne", "extRef": "0004507", "transaction": {"amount":"100", "currency":"EUR"}, "merchantId":"b3965494-1961-4d6f-828b-6e038da00c23"] } }'
```

> Example of add a donation batch response:

```json
{
  "success": "true" 
}
```

`POST https://api.worldcoo.com/v3/donations/batch`

### Request

#### HTTP Headers

Header name | Required | default | Description
---------- | ------- | ------- | -------
Authorization | yes | NA | Authorization token provided by WorldCoo


#### Body
- **items** *[donations](#donations) list*
  - **id** *string*: Required id identifier
  - **campaign_id** *string*: Required campaign identifier
  - **channelId** *string*
  - **extRef** *string*: Internal client reference (order_code) regarding this donation
  - **transaction** *Object*: {**amount** *number*, **currency** *[CurrencyCode](#currency-standar)* }
  - **order_code** *string*: Internal client reference regarding this donation

### Response

`200 Created`

##### Body
- **success** *boolean*
    
### Errors:

[error responses reference](#errors-response-reference)

HTTP Code | type                     | message
--------- |--------------------------| -------
400 | **TooManyDonations**     | *The maximum of donations allowed is 1000 *
500 | **system**               | *An error occurred while processing your request*
