# List Orders

This endpoint retrieves a list of all orders.

## Retrieve a List of Orders

To get the list of orders, send a `GET` request to the `/api/orders` endpoint.

### HTTP Request

`GET /api/orders`

#### Authorization

Bearer token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
  "orders": [
    {
      "id": 6,
      "number": "XASH-POS-66664070",
      "shop_id": 1,
      "cashier_id": 2,
      "cashier": {
        "id": 2,
        "name": "Cashier1",
        "email": "cashier1@email.com",
        "email_verified_at": null,
        "role": "cashier",
        "shop_id": 1
      },
      "items": [
        {
          "id": 18,
          "order_id": 6,
          "product_id": 1,
          "quantity": 15,
          "unit_price": "10.99",
          "created_at": "2024-02-07T05:28:00.000000Z",
          "updated_at": "2024-02-07T05:28:00.000000Z"
        }
        // ... additional items ...
      ]
    }
    // ... additional orders ...
  ]
}
```

[< Previous: Delete Product](/products-management/delete-product.md) | [Next: Add Order >](/orders-management/add-order.md)