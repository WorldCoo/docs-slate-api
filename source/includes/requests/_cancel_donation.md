## Cancel donation

> Example of cancel donation call:

```shell
curl -X DELETE
-H "Authorization: <ACCESS_TOKEN>"
https://api.worldcoo.com/v3/donations/{{donation_id}}
```

> Example of cancel donation response:

```json
{
    "id": "17a10455-120d-e767-0206",
    "amount": 5,
    "currency": "EUR",
    "order_code": "9638467",
    "relations": {
        "campaign": {
            "id": "37257fed-37ba-44eb-9cde"
        }
    },
    "campaign_counters": {
        "total_donated": 1,
        "target": 48
    }
}
```

`DELETE https://api.worldcoo.com/v3/donations/{{donation_id}}`

### Response

`200 Ok`

##### Response body

- **id** *string*
- **amount** *number*
- **currency** *[CurrencyCode](#currency-standar)*
- **order_code** *string*
- **relations**
    - **campaign**
        - **id** *string*
- **campaign_counters**
    - **total_donated** *number*. Amount received expressed in EUR.
    - **target** *number*. Target amount expressed in EUR.

### Errors

[error responses reference](#errors-response-reference)

HTTP Code | type | message
--------- | ---- | -------
404 | **donationNotFound** | *donation with id '{id}' doesn't exists*
500 | **system** | *An error occurred while processing your request*
