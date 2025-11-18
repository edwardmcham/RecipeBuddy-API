# `/user` resource

Contains information about the `users` in the `RecipeBuddy` API service.

## Base Endpoint

```bash
{server_url}/users
```

## Sample `user` Resource

```json
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
```

## `user` Properties

| Field | Type | Description |
|:-|:-|:-|
| `id` | Integer | Unique user ID |
| `name` | String | User’s full name |
| `email` | String | Contact email address |
| `favoriteCuisines` | Array | Preferred cuisines |
| `ownedIngredients` | Array | Ingredients currently available in the user’s kitchen |

## Read Operations

- [Get recipes with ingredients](../tasks/get-recipes-with-ingredients.md)

---

[^ top ^](#user-resource)
