# Update Tax

This endpoint is used to update the details of an existing tax.

## Update an Existing Tax

To update an existing tax, send a `PUT` request to the `/api/taxes/{tax}` endpoint with the new tax name, rate and type in the request body.

### HTTP Request

`PUT /api/taxes/{tax}`

#### Authorization

Bearer token required.

#### Parameters

| Name | Type   | Description                |
|------|--------|----------------------------|
| name | string | The name of the tax.  |
| rate | string | The rate for the tax. |
| type | string | The type for the tax. |

#### Responses

- `200 OK`

```json
{
    "message": "Tax updated successfully",
    "tax": {
        "id": 2,
        "shop_id": 1,
        "name": "Transport Tax",
        "rate": "2.5",
        "type": "include in price",
        "created_at": "2024-03-16T09:38:42.000000Z",
        "updated_at": "2024-03-16T13:44:43.000000Z"
    }
}
```

[< Previous: Add Tax](/taxes-management/add-taxes.md) | [Next: Delete Tax >](/taxes-management/delete-taxes.md)