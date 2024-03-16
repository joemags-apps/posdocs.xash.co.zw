# Delete Tax

This endpoint is used to delete an existing tax.

## Delete an Existing Tax

To delete a tax, send a `DELETE` request to the `/api/taxes/{tax}` endpoint.

### HTTP Request

`DELETE /api/taxes/{tax}`

#### Authorization

Bearer token required.

#### Parameters

No parameters are required as the tax ID will be specified in the URL.

#### Responses

- `200 OK`

```json
{
    "message": "Tax deleted successfully"
}
```

[< Previous: Update Tax](/taxes-management/update-tax.md) | [Next: List Products >](/products-management/list-products.md)