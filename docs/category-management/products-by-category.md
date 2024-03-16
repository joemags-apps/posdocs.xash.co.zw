# List products by Categories

This endpoint retrieves a list of product categories.

## Get List of products by Categories

To get the list of products by categories available, send a `GET` request to the `/api/products-by-category/{category}` endpoint.

### HTTP Request

`GET /api/products-by-category/{category}`

#### Authorization

Bearer token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
    "products": [
        {
            "id": 1,
            "name": "Cooking oil",
            "image_url": "01HS3TFJN4S9QR151FJAGFPJJ4.jpg",
            "category_id": 2,
            "price": "1.99",
            "sold_by": "each",
            "stock_quantity": null,
            "is_visible": 1,
            "track_stock": 0,
            "shop_id": 1,
            "slug": "cooking-oil",
            "description": "Cooking oil",
            "SKU": null,
            "Barcode": null,
            "created_at": "2024-03-16T14:26:02.000000Z",
            "updated_at": "2024-03-16T14:51:25.000000Z"
        }
    ]
}
```

[< Previous: Shop](/shop.md) | [Next: Add Category >](/category-management/add-category.md)