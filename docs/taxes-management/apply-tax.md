# Apply Tax to Products

Apply Tax to the products using this endpoint.

## apply Tax

To apply tax on a product, send a `POST` request to the `/api/apply-tax` endpoint.

### HTTP Request

`POST /api/apply-tax`

#### Authorization

Bearer token required.

#### Sample JSON Request

```json
{
    "product_id": 1,
    "tax_id": 1
}

```

#### Request Parameters

| Name        | Type | Description                |
|-------------|------|----------------------------|
| product_id  | int  | ID of the product to be applied tax. |
| tax_id  | int  | ID of the tax. |

#### Response

- `200 OK`

```json
{
    "message": "Tax associated with product successfully"
}
```



[< Previous: List Taxes](/taxes-management/list-taxes.md) | [Next: Update Tax >](/taxes-management/update-tax.md)