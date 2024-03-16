# List Taxes

This endpoint retrieves a list of product taxes.

## Get List of Taxes

To get the list of taxes available, send a `GET` request to the `/api/taxes` endpoint.

### HTTP Request

`GET /api/taxes`

#### Authorization

Bearer token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
    "Taxes": [
        {
            "id": 1,
            "shop_id": 1,
            "name": "Product Tax",
            "rate": "30",
            "type": "include in price",
            "created_at": "2024-03-16T09:38:20.000000Z",
            "updated_at": "2024-03-16T09:38:20.000000Z"
        },
        {
            "id": 2,
            "shop_id": 1,
            "name": "Duty Tax",
            "rate": "25",
            "type": "added to the price",
            "created_at": "2024-03-16T09:38:42.000000Z",
            "updated_at": "2024-03-16T09:38:42.000000Z"
        }
    ]
}
```

[< Previous: Shop](/shop.md) | [Next: Add Tax >](/taxes-management/add-tax.md)