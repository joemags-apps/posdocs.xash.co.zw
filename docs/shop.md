# Shop

This section details how to get shop information using the POS API.

## Get Shop Information

To retrieve information about the shop, send a `GET` request to the `/api/shops` endpoint.

### HTTP Request

`GET /api/shops`

#### Authorization

Bearer token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
  "shop": {
    "id": 1,
    "name": "OK MART",
    "city": "Mutare",
    "state": "Manicaland",
    "address": "Hobhouse III, Mutare",
    "phone_number": "0712 345 6789",
    "country": "Zimbabwe",
    "created_at": "2024-02-06T08:53:24.000000Z",
    "updated_at": "2024-02-06T08:53:24.000000Z"
  }
}
```

[< Previous: Authentication](/authentication) | [Next: Category Management >](/category-management/list-categories)
