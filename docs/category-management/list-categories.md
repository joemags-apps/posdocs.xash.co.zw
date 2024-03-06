# List Categories

This endpoint retrieves a list of product categories.

## Get List of Categories

To get the list of categories available, send a `GET` request to the `/api/categories` endpoint.

### HTTP Request

`GET /api/categories`

#### Authorization

Bearer token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
  "Categories": [
    {
      "id": 1,
      "name": "Clothing Updated",
      "slug": "clothing-updated",
      "created_at": "2024-02-07T09:24:35.000000Z",
      "updated_at": "2024-02-07T22:33.000000Z",
      "shop_id": 1
    },
    {
      "id": 2,
      "name": "Electronics",
      "slug": "electronics",
      "created_at": "2024-02-06T09:24:52.000000Z",
      "updated_at": "2024-02-06T09:24:52.000000Z",
      "shop_id": 1
    },
    // ... other categories ...
  ]
}
```

[< Previous: Shop](/shop.md) | [Next: Add Category >](/category-management/add-category.md)