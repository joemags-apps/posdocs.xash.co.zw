# List Products

This endpoint retrieves a list of all products.

## Get List of Products

To retrieve a list of all products, send a `GET` request to the `/api/products` endpoint.

### HTTP Request

`GET /api/products`

#### Authorization

Bearer token required.

#### Parameters

No parameters.

#### Responses

- `200 OK`

```json
{
  "Products": [
    {
      "id": 1,
      "name": "Laptop HP",
      "image_url": "QmHNZ08W365CEEAPCO6D6EY574.jpg",
      "category_id": 2,
      "price": "1200.00",
      "stock_quantity": "20",
      "is_visible": 1,
      "track_stock": 0,
      "shop_id": 1,
      "created_at": "2024-02-06T10:21:21.000000Z",
      "updated_at": "2024-02-06T10:21:21.000000Z",
      "slug": null,
      "description": "Laptop HP",
      "sold_by": "each",
      "SKU": null,
      "Barcode": null
    }
    // ... other products ...
  ]
}
```

[< Previous: Delete Category](/category-management/delete-category.md) | [Next: Add Product >](/products-management/add-product.md)