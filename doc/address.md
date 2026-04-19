## Address API Spec

### Create Address

Endpoint: POST /api/contacts/:idContact/addresses

Request Header:

- X-API-TOKEN: token

Request Body:

```json
{
  "street": "Jl.Bakti",
  "city": "Jakarta Selatan",
  "country": "Indonesia",
  "province": "DKI Jakarta",
  "postal_code": "112345"
}
```

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jl.Bakti",
    "city": "Jakarta Selatan",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "112345"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "postal_code is required"
}
```

### Get Address

Endpoint: GET /api/contacts/:idContact/addresses/:idAddress

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jl.Bakti",
    "city": "Jakarta Selatan",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "112345"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "addrees is not found"
}
```

### Update Address

Endpoint: PUT /api/contacts/:idContact/addresses/:idAddress

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": {
    "id": 1,
    "street": "Jl.Bakti",
    "city": "Jakarta Selatan",
    "province": "DKI Jakarta",
    "country": "Indonesia",
    "postal_code": "112345"
  }
}
```

Response Body (Failed):

```json
{
  "errors": "addrees is not found"
}
```

### Remove Address

### List Address
