# Add Product

This endpoint is used to create a new product in the system.

## Create a New Product

To create a new product, send a `POST` request to the `/api/products` endpoint with the required details in the JSON body.

### HTTP Request

`POST /api/products`

#### Authorization

Bearer token required.

#### Sample JSON Body

```json
{
  "name": "Create New Product",
  "slug": "example-test",
  "image_url": "https://example.com/image.jpg",
  "category_id": 1,
  "is_visible": true,
  "track_stock": true,
  "price": 19.99,
  "stock_quantity": 100,
  "description": "This is an example product description.",
  "sold_by": "each",
  "SKU": "ABC123",
  "Barcode": "123456789"
}
```

#### Parameters

| Name             | Type    | Description                        |
|------------------|---------|------------------------------------|
| name             | string  | The name of the product.           |
| slug             | string  | The slug for the product.          |
| image_url        | string  | The URL of the product image.      |
| category_id      | integer | The ID of the product's category.  |
| is_visible       | boolean | Whether the product is visible.    |
| track_stock      | boolean | Whether to track stock for the product. |
| price            | float   | The price of the product.          |
| stock_quantity   | integer | The quantity of stock.             |
| description      | string  | The description of the product.    |
| SKU              | string  | The stock keeping unit.            |
| Barcode          | string  | The barcode of the product.        |

#### Responses

- `201 Created`

```json
{
  "message": "Product/Item created successfully",
  "category": {
    "name": "Create New Product",
    "slug": "example-test",
    "image_url": "https://example.com/image.jpg",
    "category_id": 1,
    "is_visible": true,
    "track_stock": true,
    "price": 19.99,
    "stock_quantity": 100,
    "description": "This is an example product description.",
    "sold_by": "each",
    "SKU": "ABC123",
    "Barcode": "123456789",
    "shop_id": 1,
    "created_at": "2024-02-08T14:58:00.000000Z",
    "id": 10
  }
}
```

[< Previous: List Products](/products-management/list-products.md) | [Next: Update Product >](/products-management/update-product.md)