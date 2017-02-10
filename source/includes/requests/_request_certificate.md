## Request donor certificate

> Example of certificate request call:

```shell
curl -X PUT
-H "Authorization: <ACCESS_TOKEN>"
-H "Content-Type: application/json"
https://api.worldcoo.com/v3/certificates
--data '{
    "donation_id": "a9fb530d-6270-0cc7-e8a8",
    "donor_name": "John",
    "donor_lastname": "Doe",
    "donor_email": "johndoe@worldcoo.com",
    "donor_documentType": "id",
    "donor_documentNumber": "12345678Z",
    "donor_streetType": "Street",
    "donor_streetName": "Riera de Sant Miquel",
    "donor_streetNumber": "26",
    "donor_phone": "+34698726252",
    "donor_postalCode": "08008",
    "donor_city": "Barcelona",
    "donor_province": "Barcelona",
    "donor_country": "Spain",
    "donor_isCompany": false
    "donor_companyName": "John & Sons"
    }'
```

> Example of certificate request response:

```json
{"request": "success"}
```

`PUT https://api.worldcoo.com/v3/certificates`

### Request

#### HTTP Headers

Header name | Required | default | Description
---------- | ------- | ------- | -------
Authorization | yes | NA | Authorization token provided by WorldCoo
[Accept-Language](https://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.4) | No | en | iso 639-2/b language code.

#### Body

Field name | Required | default | Description
---------- | ------- | ------- | -------
donation_id | yes | NA | WorldCoo donation ID
donor_name | yes | NA | Name of the donor
donor_lastname | yes | NA | Lastname of the donor
donor_email | yes | NA | Email of the donor
donor_documentType | yes | NA | Value map: "id", "taxid", "passport", "others"
donor_documentNumber | yes | NA | Donor document ID number
donor_streetType | yes | NA | Direction type of the direction
donor_streetName | yes | NA | Direction name of the donor
donor_streetNumber | yes | NA | Direction number of the donor
donor_stairs | no | NA | Direction stairs for the donor
donor_floor | no | NA | Direction floor for the donor
donor_door | no | NA | Direction door for the donor
donor_phone | no | NA | Phone of the donor
donor_postalCode | yes | NA | Postal code of the donor
donor_city | yes | NA | City of the donor
donor_province | yes | NA | Province of the donor
donor_country | yes | NA | Country of the donor
donor_isCompany | no | false | If this certificate is expended to a company
donor_companyName | no | NA | If this is a company related certificate, his name



### Response

`201 Created`

`200 Success`

##### Body
- **request** *string* "success" | "missing fields"
