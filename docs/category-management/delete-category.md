# Delete Category

This endpoint is used to delete an existing category.

## Delete an Existing Category

To delete a category, send a `DELETE` request to the `/api/categories/{category}` endpoint.

### HTTP Request

`DELETE /api/categories/{category}`

#### Authorization

Bearer token required.

#### Parameters

No parameters are required as the category ID will be specified in the URL.

#### Responses

- `200 OK`

```json
{
  "message": "Category deleted successfully"
}
```

[< Previous: Update Category](/category-management/update-category.md) | [Next: List Products >](/products-management/list-products.md)