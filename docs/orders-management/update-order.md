# Update Order

This endpoint is used for updating the details of an existing order.

## Update an Existing Order

To update an existing order, send a `PUT` request to the `/api/orders/{order}` endpoint with the updated order details in the JSON body.

### HTTP Request

`PUT /api/orders/{order}`

#### Authorization

Bearer token required.

#### Update Body JSON

```json
{
  "cashier_id": 2,
  "order_items": [
    {
      "product_id": 1,
      "quantity": 15,
    },
    {
      "product_id": 3,
      "quantity": 20,
    }
  ]
}
```

#### Parameters

The JSON body should contain the following parameters:

| Name         | Type  | Description                           |
|--------------|-------|---------------------------------------|
| cashier_id   | int   | ID of the cashier creating the order. |
| order_items  | array | Array of order item objects.          |

Each object in the `order_items` array should contain:

| Name        | Type   | Description                               |
|-------------|--------|-------------------------------------------|
| product_id  | int    | ID of the product being ordered.          |
| quantity    | int    | Quantity of the product being ordered.    |

#### Responses

- `200 OK`

```json
{
  "message": "Order updated successfully",
  "order": {
    "id": 7,
    "number": "XASH-POS-502507786",
    // return total
    "shop_id": 1,
    "cashier_id": 2,
    "updated_at": "2024-02-08T04:37:57.000000Z"
  }
}
```

[< Previous: Add Order](/orders-management/add-order.md) | [Next: Delete Order >](/orders-management/delete-order.md)