---
sidebar_position: 5
title: Pack Manifest JSON
---

# manifest.json for Behavior Packs

The manifest file contains all the basic information about the pack that Endium needs to identify it. The tables below
contain all the components of the manifest, their individual properties, and what they mean.

## Properties

| Name     | Description                                                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------|
| header   | Section containing information regarding the name of the pack, description, and other features that are public facing. |
| modules  | Section containing information regarding the type of content that is being brought in.                                 |
| metadata | Section containing the metadata about the file such as authors and licensing information.                              |

### header

| Name        | Type   | Description                                                                          |
|-------------|--------|--------------------------------------------------------------------------------------|
| name        | String | The name of the pack. This is what will be displayed in the game.                    |
| description | String | This is a short description of the pack. We recommend keeping it to 1-2 lines.       |
| version     | String | The version of the pack. This should be in the format `x.x.x` where `x` is a number. |

### metadata

| Name           | Type         | Description                                                                                                                                                                                                                                              |
|----------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| authors        | String array | Name of the author(s) of the pack.                                                                                                                                                                                                                       |
| license        | String       | The license of the pack.                                                                                                                                                                                                                                 |
| url            | String       | The home website of your pack..                                                                                                                                                                                                                          |
| generated_with | String       | This is used to identify tools used to generate a manifest.json file. The tool names are strings that must be [a-zA-Z0-9_-] and 32 characters maximum. The tool version number are semver strings for each version that modified the manifest.json file. |

## Example

```json
{
  "header": {
    "name": "Behavior Pack",
    "version": "1.0.0",
    "description": "Example behavior pack"
  },
  "metadata": {
    "authors": [
      "exampleAuthor"
    ],
    "license": "MIT",
    "url": "https://paladium-pvp.fr/"
  }
}
```