# Add Category

This endpoint allows for the creation of a new product category.

## Add a New Category

To add a new category, send a `POST` request to the `/api/categories` endpoint with the category name and slug.

### HTTP Request

`POST /api/categories`

#### Authorization

Bearer token required.

#### Parameters

| Name | Type   | Description                |
|------|--------|----------------------------|
| name | string | The name of the category.  |
| slug | string | The slug for the category. |

#### Responses

- `201 Created`

```json
{
  "message": "Category created successfully",
  "category": {
    "name": "grocery",
    "slug": "grocery",
    "shop_id": 1,
    "created_at": "2024-02-08T07:43:00.000000Z",
    "updated_at": "2024-02-08T07:43:00.000000Z",
    "id": 12
  }
}
```

[< Previous: List Categories](/category-management/list-categories.md) | [Next: Update Category >](/category-management/update-category.md)