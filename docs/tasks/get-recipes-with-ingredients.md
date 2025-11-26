# Get recipes with ingredients

Returns a filtered list of recipes that match the provided ingredients.

**NOTE**: This resource only supports filtering by a single `ownedIngredient`.

## Request

### Postman

```bash
GET {base_url}/recipes?ingredients_like=spinach
```

### cURL

```bash
curl https://{base_url}/recipes?ingredients_like=spinach
```

### JavaScript

```javascript
fetch('/recipes?ingredients_like=spinach')
  .then(response => response.json())
  .then(data => console.log(data));
```

## Response

```json
[
    {
        "id": 1,
        "title": "Spinach Cheese Omelet",
        "ingredients": [
            "Eggs",
            "Spinach",
            "Cheese",
            "Salt",
            "Pepper"
        ],
        "cookingTime": 10,
        "difficulty": "Easy",
        "authorId": 1
    }
]
```
