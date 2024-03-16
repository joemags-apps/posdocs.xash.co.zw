# Assign Category to Products

Assign Category to the products using this endpoint.

## Assign Category

To assign Category on a product, send a `POST` request to the `/api/assign-category` endpoint.

### HTTP Request

`POST /api/assign-category`

#### Authorization

Bearer token required.

#### Sample JSON Request

```json
{
  "product_id": 1,
  "category_id": 2
}
```

#### Request Parameters

| Name        | Type | Description                |
|-------------|------|----------------------------|
| product_id  | int  | ID of the product to be assigned category. |
| category_id  | int  | ID of the category. |

#### Response

- `200 OK`

```json
{
    "message": "Category assigned to product successfully"
}
```



[< Previous: Add Category](/category-management/add-category.md) | [Next: Delete Category >](/category-management/delete-category.md)