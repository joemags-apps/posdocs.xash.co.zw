# Authentication

This section covers the authentication process for the Point of Sale (POS) API including registration, login, and generating signed URLs.

## Register

To register a new user to the system, send a `POST` request to the `auth/register` endpoint with the following JSON payload:

```json
{
    "first_name": "John",
    "last_name": "Doe",
    "dob": "2000-01-01",
    "phone": "263775123456",
   "id_number": "71-123456X55",
    "email": "johndoe@gmail.com"
}


```

### HTTP Request

`POST auth/register`

#### Parameters

No parameters.

#### Responses

- `201 Created`

```json
{
    "success": true,
    "message": "User registered successfully",
    "token": "xxx",
    "data": {
        "success": true,
        "message": "Profile was created successfully. User number sent on WhatsApp",
        "data": {
         "first_name": "John",
       "last_name": "Doe",
    "dob": "2000-01-01",
    "phone": "263775123456",
    "id_number": "71-123456X55"
        }
    }
}
```

<!-- Set Passowrd -->
## Set Password

This endpoint allows users to set their password after registration.

### HTTP Request

`POST auth/set-password`

#### Parameters

| Name       | Type   | Description  |
|------------|--------|--------------|
| `user_number`    | string | The user's unique user number |
| `password` | string | User's password |
| `password_confirmation` | string | The confirmation of the new password |

#### Responses

- `201 Created`

```json
{
    "success": true,
    "accessToken": "39|mIDgu6IDZ0tRPksJ1MiUFbito0486gmNLX3QOOAm0cbdd7ea",
    "tokenType": "Bearer",
    "has_address": false,
    "has_business": false,
    "message": "Password has been set successfully."
}
```
<!-- Login -->
## Login

To log in an existing user, send a `POST` request to `auth/login` with the user's email and password.

### HTTP Request

`POST auth/login`

#### Parameters

| Name       | Type   | Description  |
|------------|--------|--------------|
| `user_number`    | string | The user's unique user number |
| `password` | string | User's password |

#### Responses

- `201 Created`

```json
{
    "success": true,
    "token": "2|Jw63hQgjNjSFrcrbReN2xMD9qXN2LcKuAkn8sSV0e10b4a95"
}
```
<!-- Resend User Number -->
## Resend User Number

This endpoint allows users to request a resend of their user number.

### HTTP Request

`POST /auth/resend-number/{phone`

#### Parameters

| Name       | Type   | Description  | 
|------------|--------|----------------------------|
| `phone`    | string | TThe user's phone number in E.164 format without leading + |

#### Responses

- `201 Created`

```json
{
  "success": true,
  "message": "User number resent successfully."
}
```


<!-- Create a Business -->
## Create Business

This endpoint allows authenticated users to create a business

### HTTP Request

`POST /auth/create-business`

#### Parameters

| Name       | Type   | Description  | Validation |
|------------|--------|--------------|--------------|
| `business_name`    | string | The name of the business | Required, min 2 characters, max 50 characters |
| `business_category`    | string | The category of the business | Required |
| `bp_number`    | string | The business partner number | Optional|
| `address_line_1`    | string | The home address line 1 | Required, min 3 characters, max 256 characters |
| `address_line_2`    | string | The home address line 2 | Optional, min 3 characters, max 256 characters |
| `city`    | string | The home address city | Required, min 3 characters, max 256 characters |
| `business_address_line_1`    | string | The business address line 1 | Required, min 3 characters, max 256 characters |
| `business_address_line_2`    | string | The business address line 2 | Optional, min 3 characters, max 256 characters |
| `business_city`    | string | The business address city | Required, min 3 characters, max 256 characters |


#### Responses

- `201 Created`

```json
{
  "success": true,
  "message": "Business created successfully.",
  "data": {
    "id": 1,
    "business_name": "Xash Technologies",
    "business_category": "IT",
    "bp_number": "BP12345678",
    "home_address": {
      "address_line_1": "123 Main St",
      "address_line_2": null,
      "city": "Mutare"
    },
    "business_address": {
      "business_address_line_1": "456 Business Ave",
      "business_address_line_2": null,
      "business_city": "Mutare"
    }
  }
}
```

<!-- Fetch Profile -->


<!-- Signed URL -->
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