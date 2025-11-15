# Recipe Buddy API
*A smart kitchen companion for discovering and managing recipes.*

## Overview
**Recipe Buddy API** is a RESTful web service designed for home cooks and food enthusiasts. It allows users to discover, save, and share recipes — and even suggests dishes based on ingredients already in their kitchen. The goal is to make home cooking simpler, reduce food waste, and save time searching for meal ideas.  
This repository is part of the **SME/TW collaboration** for the Technical Writing Portfolio project.  
- **SME:** Drashti Bhatt  
- **TW:** Eddie McHam  
- **Service:** Recipe Buddy API  

## Key features
- Ingredient-based search — find recipes using what’s already in your pantry.  
- Recipe storage — save and organize personal or favorite recipes.  
- Culinary insights — filter by cuisine, difficulty, or cook time.  
- Favorites tracking — keep a record of preferred cuisines and dishes.  
- Shareable content — export recipes or send to other users.

## API resources
### `/recipes`
| Field | Type | Description |
|--------|------|-------------|
| `id` | Integer | Unique recipe ID |
| `title` | String | Recipe title |
| `ingredients` | Array | List of required ingredients |
| `cookingTime` | Integer | Time (in minutes) required for cooking |
| `difficulty` | String | Difficulty level (Easy / Medium / Hard) |
| `authorId` | Integer | References the recipe creator in `/users` |

### `/users`
| Field | Type | Description |
|--------|------|-------------|
| `id` | Integer | Unique user ID |
| `name` | String | User’s full name |
| `email` | String | Contact email address |
| `favoriteCuisines` | Array | Preferred cuisines |
| `ownedIngredients` | Array | Ingredients currently available in the user’s kitchen |

## Example database file
The main database file for this service is:
```
api/recipe-buddy-db-source.json
```
It contains mock data used for API examples — including recipes and users. This file models how data would be stored and fetched by a backend service.

## Example query
**Request**
```
GET /recipes?ingredients=spinach,cheese
```
**Response**
```json
[
  {
    "id": 1,
    "title": "Spinach Cheese Omelet",
    "ingredients": ["Eggs", "Spinach", "Cheese", "Salt", "Pepper"],
    "cookingTime": 10,
    "difficulty": "Easy",
    "authorId": 1
  }
]
```

## Quick start (Example Integration)
### Using cURL
```bash
curl https://example.com/api/recipes?ingredients=tomato,cheese
```
### Using JavaScript (fetch)
```javascript
fetch('/api/recipes?ingredients=tomato,cheese')
  .then(response => response.json())
  .then(data => console.log(data));
```
These calls return a filtered list of recipes that match the provided ingredients.

## Project structure
```
RecipeBuddy-API/
├── README.md
└── api/
    └── recipe-buddy-db-source.json
```

## Use case example
A user named **Drashti** opens Recipe Buddy, enters “potatoes, spinach, and cheese” as available ingredients. The API instantly returns dishes like *Spinach Cheese Omelet* or *Aloo Palak*, which can be made immediately without extra shopping. This reduces food waste and simplifies decision-making in the kitchen.


This project is part of an academic documentation portfolio and may be used for educational purposes only.  

