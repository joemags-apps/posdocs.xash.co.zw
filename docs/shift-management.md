# Shift Management

Manage cashier shifts including starting and ending them.

## Start Shift

To start a shift, send a `POST` request to the `/api/shift/start` endpoint.

### HTTP Request

`POST /api/shift/start`

#### Authorization

Bearer token required.

#### Sample JSON Request

```json
{
  "cashier_id": 18
}
```

#### Request Parameters

| Name        | Type | Description                |
|-------------|------|----------------------------|
| cashier_id  | int  | ID of the cashier starting the shift. |

#### Response

- `200 OK`

```json
{
  "message": "Shift started successfully",
  "shift": {
    "cashier_id": 18,
    "start_time": "2024-02-14T09:35:26.000000Z",
    "created_at": "2024-02-14T09:35:26.000000Z",
    "updated_at": "2024-02-14T09:35:26.000000Z",
    "id": 3
  }
}
```

## End Shift

To end a shift, send a `POST` request to the `/api/shift/end` endpoint.

### HTTP Request

`POST /api/shift/end`

#### Authorization

Bearer token required.

#### Sample JSON Request

```json
{
  "shift_id": 3 // Current shift id
}
```

#### Request Parameters

| Name     | Type | Description                  |
|----------|------|------------------------------|
| shift_id | int  | ID of the shift being ended. |

#### Response

- `200 OK`

```json
{
  "message": "Shift ended successfully",
  "shift": {
    "id": 3,
    "cashier_id": 18,
    "start_time": "2024-02-14T09:35:26.000000Z",
    "end_time": "2024-02-14T09:36:43.000000Z",
    "created_at": "2024-02-14T09:35:26.000000Z",
    "updated_at": "2024-02-14T09:36:43.000000Z",
    "orders": [
      {
        "id": 10,
        "number": "XASH-POS-864395779",
        "shop_id": 15,
        "cashier_id": 18,
        "created_at": "2024-02-14T09:36:10.000000Z",
        "updated_at": "2024-02-14T09:36:10.000000Z"
      }
      // ... additional orders ...
    ]
  }
}
```

[< Previous: Delete Order](/orders-management/delete-order.md)