# Add Order

This endpoint is used to create a new order.

## Create a New Order

To add a new order, send a `POST` request to the `/api/orders` endpoint with the order details in the JSON body.

### HTTP Request

`POST /api/orders`

#### Authorization

Bearer token required.

#### Sample JSON Body

```json
{
  "cashier_id": 2,
  "order_items": [
    {
      "product_id": 1,
      "quantity": 2,
      "unit_price": 10.99
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
| unit_price  | float  | Unit price of the product being ordered.  |

#### Responses

- `201 Created`

```json
{
  "message": "Order created successfully",
  "order": {
    "shop_id": 1,
    "cashier_id": 2,
    "number": "XASH-POS-502507786",
    "updated_at": "2024-02-08T04:37:57.000000Z",
    "id": 7
  }
}
```

[< Previous: List Orders](/orders-management/list-orders.md) | [Next: Update Order >](/orders-management/update-order.md)