# Update Product

This endpoint allows for updating the details of an existing product.

## Update an Existing Product

To update a product, send a `PUT` request to the `/api/products/{product}` endpoint with the updated product details in the JSON body.

### HTTP Request

`PUT /api/products/{product}`

#### Authorization

Bearer token required.

#### Update Body JSON

```json
{
  "name": "Updated Product Name",
  "slug": "updated-product-slug",
  "image_url": "https://example.com/updated-image.jpg",
  "category_id": 2,
  "is_visible": true,
  "track_stock": true,
  "price": 24.99,
  "stock_quantity": 75,
  "description": "This is an updated product description.",
  "SKU": "XYZ789",
  "Barcode": "987654321",
  "shop_id": 1
}
```

#### Parameters

No parameters are needed in the query string as the product ID and updated details are provided in the URL and body respectively.

#### Responses

- `200 OK`

```json
{
  "message": "Product updated successfully",
  "product": {
    "id": 7,
    "name": "Updated Product Name",
    "slug": "updated-product-slug",
    "image_url": "https://example.com/updated-image.jpg",
    "category_id": 2,
    "price": 24.99,
    "stock_quantity": 75,
    "is_visible": true,
    "track_stock": true,
    "description": "This is an updated product description.",
    "SKU": "XYZ789",
    "Barcode": "987654321",
    "shop_id": 1,
    "created_at": "2024-02-08T04:32:56.000000Z",
    "updated_at": "2024-02-08T04:32:56.000000Z"
  }
}
```

[< Previous: Add Product](/products-management/add-product.md) | [Next: Delete Product >](/products-management/delete-product.md)