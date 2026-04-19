# User API Spec

### Register User

Endpoint: POST /api/users
Request Body:

```json
{
  "username": "mejimaru",
  "password": "123321",
  "name": "Meiji Maruao"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "mejimaru",
    "name": "Meiji Maruao"
  }
}
```

Respone Body (Failed):

```json
{
  "errors": "Username must not blank, ..."
}
```

### Login User

Endpoint: POST /api/users/login
Request Body:

```json
{
  "username": "mejimaru",
  "password": "123321"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "mejimaru",
    "name": "Meiji Maruao",
    "token": "uuid"
  }
}
```

Respone Body (Failed):

```json
{
  "errors": "Username or password wrong, ..."
}
```

### Get User

Endpoint: GET /api/users/current

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": {
    "username": "mejimaru",
    "name": "Meiji Maruao"
  }
}
```

Respone Body (Failed):

```json
{
  "errors": "Unauthorized, ..."
}
```

### Update User

Endpoint: PATCH /api/users/current

Request Header:

- X-API-TOKEN: token

Request Body:

```json
{
  "password": "123321", // tidak wajib
  "name": "Meiji Maruao" // tidak wajib
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "mejimaru",
    "name": "Meiji Maruao"
  }
}
```

Respone Body (Failed):

```json
{
  "errors": "Unauthorized, ..."
}
```

### Logout User

Endpoint: DELETE /api/users/current

Request Header:

- X-API-TOKEN: token

Response Body (Success):

```json
{
  "data": "OK"
}
```

Respone Body (Failed):

```json
{
  "errors": "Unauthorized, ..."
}
```
