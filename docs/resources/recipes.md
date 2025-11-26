# `recipe` resource

Contains information about the `recipes` in the `RecipeBuddy` API service.

## Base Endpoint

```bash
{server_url}/recipes
```

## Sample `recipe` Resource

```json
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
```

## `recipe` Properties

| Field | Type | Description |
|:-|:-|:-|
| `id` | Integer | Unique recipe ID |
| `title` | String | Recipe title |
| `ingredients` | Array | List of required ingredients |
| `cookingTime` | Integer | Time (in minutes) required for cooking |
| `difficulty` | String | Difficulty level (Easy / Medium / Hard) |
| `authorId` | Integer | References the recipe creator in `/users` |

## Read Operations

- [Get recipes with ingredients](../tasks/get-recipes-with-ingredients.md)
