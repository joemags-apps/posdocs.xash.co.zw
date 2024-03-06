# Update Category

This endpoint is used to update the details of an existing category.

## Update an Existing Category

To update an existing category, send a `PUT` request to the `/api/categories/{category}` endpoint with the new category name and slug in the request body.

### HTTP Request

`PUT /api/categories/{category}`

#### Authorization

Bearer token required.

#### Parameters

| Name | Type   | Description                |
|------|--------|----------------------------|
| name | string | The new name of the category.  |
| slug | string | The new slug for the category. |

#### Responses

- `200 OK`

```json
{
  "message": "Category updated successfully",
  "category": {
    "id": 1,
    "name": "electronics",
    "slug": "electronics",
    "created_at": "2024-02-06T09:24:35.000000Z",
    "updated_at": "2024-02-08T10:37:00.000000Z",
    "shop_id": 1
  }
}
```

[< Previous: Add Category](/category-management/add-category.md) | [Next: Delete Category >](/category-management/delete-category.md)