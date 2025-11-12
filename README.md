# 🍳 Recipe Buddy API
*A smart kitchen companion for discovering and managing recipes.*

---

## 📖 Overview
**Recipe Buddy API** is a RESTful service that helps home cooks discover, store, and share recipes.  
It suggests dishes based on the ingredients users already have — reducing food waste and simplifying meal planning.

This project is part of the **SME / TW collaboration** for the Technical Writing Portfolio.  
- **SME:** Drashti Bhatt  
- **TW:** Eddie McHam  
- **Service:** Recipe Buddy API  
- **Repo purpose:** SME-managed database and API specification source.

---

## 💡 Key Features
- Discover recipes by ingredients you already have.  
- Save favorite recipes and track preferred cuisines.  
- Share recipes with other users.  
- View step-by-step cooking instructions.  
- RESTful endpoints for `recipes` and `users`.

---

## 📂 API Resources

### `/recipes`
| Field | Type | Description |
|--------|------|-------------|
| `id` | Integer | Unique recipe ID |
| `title` | String | Recipe title |
| `ingredients` | Array | List of ingredients |
| `cookingTime` | Integer | Minutes required |
| `difficulty` | String | Difficulty level (Easy / Medium / Hard) |
| `authorId` | Integer | References the recipe creator |

### `/users`
| Field | Type | Description |
|--------|------|-------------|
| `id` | Integer | Unique user ID |
| `name` | String | Full name |
| `email` | String | Contact email |
| `favoriteCuisines` | Array | Preferred cuisines |
| `ownedIngredients` | Array | Pantry items currently available |

---

## 🧾 Example Query
**GET** `/recipes?ingredients=spinach,cheese`

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
