# Authentication

This section covers the authentication process for the Point of Sale (POS) API including registration, login, and generating signed URLs.

## Register

To register a new user to the system, send a `POST` request to the `/api/register` endpoint with the following JSON payload:

```json
{
  "name": "API Doe",
  "email": "sabukku@xash.com",
  "password": "secretPassword",
  "shop_name": "Example Shop",
  "city": "Mutare"
}
```

### HTTP Request

`POST /api/register`

#### Parameters

No parameters.

#### Responses

- `201 Created`

```json
{
  "message": "User registered successfully",
  "token": "ABCD1234"
}
```

## Login

To log in an existing user, send a `POST` request to `/api/login` with the user's email and password.

### HTTP Request

`POST /api/login`

#### Parameters

| Name       | Type   | Description  |
|------------|--------|--------------|
| `email`    | string | User's email |
| `password` | string | User's password |

#### Responses

- `201 Created`

```json
{
  "user": {
    "id": 1,
    "name": "ShopOwner1",
    "email": "shopowner1@gmail.com",
    "role": "shop_owner",
    "shop_id": 1,
    "created_at": "

```json
    "created_at": "2024-02-06T08:05:43.000000Z",
    "updated_at": "2024-02-06T08:53:24.000000Z"
  },
  "token": "EFGH5678"
}
```

## Signed URL

To access certain resources, a signed URL may be required. The signed URL can be obtained by sending a `GET` request to `/api/owner-dashboard-url`.

### HTTP Request

`GET /api/owner-dashboard-url`

#### Authorization

Bearer Token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
  "url": "<HOST>/login?expires=1786746656&signature=123456"
}
```

[< Previous: Point of Sale (POS) API Documentation](/)   |   [Next: Shop >](/shop.md)