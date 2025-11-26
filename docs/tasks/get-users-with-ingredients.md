# Get users with ingredients

Returns a filtered list of users who have the requested ingredient.

**NOTE**: This resource only supports filtering by a single `ownedIngredient`.

## Request

### Postman

```bash
GET {base_url}/users?ownedIngredients_like=Cheese"
```

### cURL

```bash
curl "http://{base_url}/users?ownedIngredients_like=Cheese"

```

### JavaScript

```javascript
fetch('/users?ownedIngredients_like=Cheese')
  .then(response => response.json())
  .then(data => console.log(data));
```

## Response

```json
[
  {
    "id": 1,
    "name": "Drashti Bhatt",
    "email": "drashti@example.com",
    "favoriteCuisines": [
      "Indian",
      "Italian"
    ],
    "ownedIngredients": [
      "Rice",
      "Tomatoes",
      "Garlic",
      "Cheese",
      "Spinach"
    ]
  }
]
```
