---
sidebar_position: 6
title: Block Description
---

# Block Documentation - Block Description

The block `"description"` lives inside the `"minecraft:block"` section of a custom block's behavior pack JSON file, and
contains a list of block characteristics that are applicable to all permutations of the block.
The description MUST contain an identifier to identify the block by; the other fields are optional.

## Parameters

| Name       | Type        | Default   | Description                                                                                                                                                                      |
|------------|-------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| identifier | String      | *not set* | The identifier for this block. The name must include a namespace and must not use the Minecraft namespace unless overriding a Vanilla block.                                     |
| states     | JSON Object | *not set* | Map of key/value pairs that maps the state name (key) to an array of all possible values for that state (value). Learn how to use block states in Block States and Permutations. |
| traits     | JSON Object | *not set* |                                                                                                                                                                                  |

## Example

```json
{
  "format_version": "1.0.0",
  "minecraft:block": {
    "description": {
      "identifier": "paladium:paladium_block"
    },
    "components": {
      "minecraft:material_instances": {
        "materials": {
          "*": {
            "texture": "paladium_block"
          }
        }
      },
      "minecraft:destructible_by_mining": {
        "hardness": 5,
        "tool_type": 3,
        "tool_tier": 4
      }
    }
  }
}
```