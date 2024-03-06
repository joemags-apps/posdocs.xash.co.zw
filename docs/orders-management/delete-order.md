# Delete Order

This endpoint is used to delete an existing order along with any associated items.

## Delete an Existing Order

To delete an order, send a `DELETE` request to the `/api/orders/{order}` endpoint.

### HTTP Request

`DELETE /api/orders/{order}`

#### Authorization

Bearer token required.

#### Parameters

No parameters are required as the ID of the order to be deleted will be specified in the endpoint's URL.

#### Responses

- `200 OK`

```json
{
  "message": "Order and associated items deleted successfully"
}
```

[< Previous: Update Order](/orders-management/update-order.md) | [Next: Shift Management >](/shift-management.md)