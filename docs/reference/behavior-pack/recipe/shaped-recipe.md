---
sidebar_position: 6
title: Shaped Recipe
---

# Recipe Documentation - Shaped Recipe

Represents a crafting recipe that is to be used with a crafting table. The key used in the pattern may be any single
character except the 'space' character, which is reserved for empty slots in a recipe.

## Parameters

| Name            | Type                        | Default   | Description                                                                       |
|-----------------|-----------------------------|-----------|-----------------------------------------------------------------------------------|
| key             | Array of key and item pairs | *not set* | Pattern key character mapped to item names.                                       |
| pattern         | String array                | *not set* | Characters that represent a pattern to be defined by keys.                        |
| priority        | Integer                     | *not set* | Sets the priority order of the recipe. Lower numbers represent a higher priority. |
| result          | Item descriptor             | *not set* | When input items match the pattern, this item will be produced as output.         |
| tags            | String array                | *not set* | Item that can create the shaped recipe, such as "crafting_table".                 |
| assume_symmetry | Boolean                     | true      | Used to automatically assume a symmetrical recipe should return the same result.  |

### Key and pattern

The `key` used in the pattern may be any single character except the 'space' character, which is reserved for empty slots in a recipe.

## Shaped Recipe Example

```json
{
  "format_version": "1.0.0",
  "minecraft:recipe_shaped": {
    "description": {
      "identifier": "minecraft:stone_axe"
    },
    "tags": [ "crafting_table" ],
    "pattern": [
      "XX",
      "X#",
      " #"
    ],
    "key": {
      "#": [
        {
          "item": "minecraft:stick"
        }
      ],
      "X": [
        {
          "item": "minecraft:cobblestone"
        }
      ]
    },
    "result": {
      "item": "minecraft:stone_axe"
    }
  }
}
```

## Shaped Recipes with assume_symmetry Property Set

`assume_symmetry` is an optional field. If not set, it will default to true. By setting it to false, you can define mirrored versions of a recipe and have different results.

```json
{
  "format_version": "1.0.0",
  "minecraft:recipe_shaped": {
    "description": {
      "identifier": "minecraft:zig"
    },
    "tags": [ "crafting_table" ],
    "assume_symmetry": false,
    "pattern": [
      "## ",
      " ##"
    ],
    "key": {
      "#": [
        {
          "tag": "minecraft:planks"
        }
      ]
    },
    "result": {
      "item": "minecraft:zig"
    }
  }
}
```

```json
{
  "format_version": "1.0.0",
  "minecraft:recipe_shaped": {
    "description": {
      "identifier": "minecraft:zag"
    },
    "tags": [ "crafting_table" ],
    "assume_symmetry": false,
    "pattern": [
      " ##",
      "## "
    ],
    "key": {
      "#": [
        {
          "tag": "minecraft:planks"
        }
      ]
    },
    "result": {
      "item": "minecraft:zag"
    }
  }
}
```