## Get available NGOs

> Example of ngo call:

```shell
curl -X GET
-H "Authorization: <ACCESS_TOKEN>"
https://api.worldcoo.com/v3/ngos
```

> Example of get ngos response:

```json
{
    "items": [
            {
                "id": "8720fdd5-1b10-a4c8-a614",
                "name": "NGO Name Example 1",
                "url": "http://www.examplengo1.com",
                "logo": {
                    "height": 533,
                    "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.original.jpg",
                    "width": 800,
                    "type": "image/jpeg",
                    "versions": {
                        "S": {
                            "height": 50,
                            "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.S.jpg",
                            "width": 75,
                            "type": "image/jpeg"
                        },
                        "L": {
                            "height": 200,
                            "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.L.jpg",
                            "width": 300,
                            "type": "image/jpeg"
                        },
                        "M": {
                            "height": 100,
                            "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.M.jpg",
                            "width": 150,
                            "type": "image/jpeg"
                        }
                    }
                },
                "media": {},
                "description": "This is an example of NGO description."
            },
            {
                "id": "79a3b10a-3c84-a19a-5e07",
                "name": "NGO Name Example 2",
                "url": "http://www.examplengo2.com",
                "logo": {
                    "height": 533,
                    "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.original.jpg",
                    "width": 800,
                    "type": "image/jpeg",
                    "versions": {
                        "S": {
                            "height": 50,
                            "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.S.jpg",
                            "width": 75,
                            "type": "image/jpeg"
                        },
                        "L": {
                            "height": 200,
                            "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.L.jpg",
                            "width": 300,
                            "type": "image/jpeg"
                        },
                        "M": {
                            "height": 100,
                            "location": "https://cdn.worldcoo.com/ngos/ee80cf92-d49b-4b7c-9949-9946750ec451/logo.1479742005411.M.jpg",
                            "width": 150,
                            "type": "image/jpeg"
                        }
                    }
                },
                "media": {},
                "description": "This is an example of NGO description."
            }
    ],
    "total": 53,
    "offset": 0,
    "limit": 20
}
```

`GET https://api.worldcoo.com/v3/ngos`

### Request

#### HTTP Headers

Header name | Required | default | Description
---------- | ------- | ------- | -------
Authorization | yes | NA | Authorization token provided by WorldCoo
[Accept-Language](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.4) | No | ENG | iso 639-2/b language code.

#### Query params

Param name | Required | default | Description
---------- | ------- | ------- | -------
offset | no | 0 | The amount of items to ignore.
limit | no | 20 | The maximum number of items to return.

### Response

`200 Ok`

##### Response body

- **total** *number*
- **offset** *number*
- **limit** *number*
- **items** *list*
  - **id** *string*
  - **name** *string*
  - **url** *string*
  - **logo** *logo map*
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
  - **media** *media map*
  - **description** *string*

### Errors:

[error responses reference](#errors)
