# Delete Product

This endpoint is used to delete an existing product.

## Delete an Existing Product

To delete a product, send a `DELETE` request to the `/api/products/{product}` endpoint.

### HTTP Request

`DELETE /api/products/{product}`

#### Authorization

Bearer token required.

#### Parameters

No parameters are needed in the query string as the product ID to be deleted is specified in the URL.

#### Responses

- `200 OK`

```json
{
  "message": "Product deleted successfully"
}
```

[< Previous: Update Product](/products-management/update-product.md) | [Next: List Orders >](/orders-management/list-orders.md)