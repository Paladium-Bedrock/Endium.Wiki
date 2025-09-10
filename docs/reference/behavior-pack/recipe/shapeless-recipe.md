---
sidebar_position: 6
title: Shapeless Recipe
---

# Recipe Documentation - Shapeless Recipe

Represents a shapeless crafting recipe.

:::note

Unlike a [Shaped Recipe](shaped-recipe), `pattern` and `key` are not used when defining a Shapeless Recipe.

:::

## Parameters

| Name        | Type                  | Default   | Description                                                                       |
|-------------|-----------------------|-----------|-----------------------------------------------------------------------------------|
| ingredients | Item descriptor array | *not set* | Items used as input (without a shape) for the recipe.                             |
| priority    | Integer               | *not set* | Sets the priority order of the recipe. Lower numbers represent a higher priority. |
| result      | Item descriptor       | *not set* | When input items match the recipe, this item will be produced as output.          |
| tags        | String array          | *not set* | Item that can create the shapeless recipe, such as "crafting_table".              |

## Shapeless Recipe Example

```json
{
  "format_version": "1.0.0",
  "minecraft:recipe_shapeless": {
    "description": {
      "identifier": "minecraft:blaze_powder"
    },
    "tags": [ "crafting_table" ],
    "ingredients": [
      {
        "item": "minecraft:blaze_rod"
      }
    ],
    "result": {
      "item": "minecraft:blaze_powder",
      "count": 2
    }
  }
}
```