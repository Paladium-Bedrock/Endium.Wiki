---
sidebar_position: 6
title: Furnace Recipe
---

# Recipe Documentation - Furnace Recipe

Represents a recipe that is to be used with a furnace. Input items will burn and transform into items specified in
output.

## Parameters

| Name       | Type            | Default   | Description                                                                  |
|------------|-----------------|-----------|------------------------------------------------------------------------------|
| input      | Item descriptor | *not set* | Item that is to be transformed in the furnace.                               |
| output     | Item descriptor | *not set* | Item that is produced as output when the input item is burned.               |
| tags       | String array    | *not set* | Item that can create the furnace recipe, such as "furnace".                  |
| experience | Float           | 0.0       | Amount of experience to be given to the player when the recipe is completed. |

## Furnace Recipe Example

```json
{
  "format_version": "1.0.0",
  "minecraft:recipe_furnace": {
    "description": {
      "identifier": "minecraft:furnace_beef"
    },
    "tags": [
      "furnace",
      "smoker",
      "campfire",
      "soul_campfire"
    ],
    "experience": 0.15,
    "input": {
      "item": "minecraft:beef"
    },
    "output": {
      "item": "minecraft:cooked_beef"
    }
  }
}
```