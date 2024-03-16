# Add Tax

This endpoint allows for the creation of a new product tax.

## Add a New Tax

To add a new tax, send a `POST` request to the `/api/taxes` endpoint with the tax name and slug.

### HTTP Request

`POST /api/taxes`

#### Authorization

Bearer token required.

#### Parameters

| Name | Type   | Description                |
|------|--------|----------------------------|
| name | string | The name of the tax.  |
| rate | string | The rate for the tax. |
| type | string | The type for the tax. |

#### Responses

- `201 Created`

```json
{
    "message": "tax created successfully",
    "tax": {
        "name": "Product Tax",
        "rate": "30",
        "type": "include in price",
        "shop_id": 1,
        "updated_at": "2024-03-16T13:10:28.000000Z",
        "created_at": "2024-03-16T13:10:28.000000Z",
        "id": 3
    }
}
```

[< Previous: List Taxes](/taxes-management/list-taxes.md) | [Next: Update Tax >](/taxes-management/update-tax.md)