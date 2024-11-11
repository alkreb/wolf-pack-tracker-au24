---
layout: page
---

# `habitats` resource

Base endpoint:

```shell

{base_url}/habitats
```

Wolf habitat information.

## Resource properties

Sample`habitats` resource

```js

{
        "habitat_id": "H001",
        "location": "Northern Forest",
        "climate": "temperate",
        "prey_population": [
            "deer",
            "rabbits"
        ]
},
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `habitat_id` | number | The ID of the wolf habitat|
| `location` | string | Geographical region of the wolf habitat|
| `climate` | string | The habitat's climate|
| `prey_population` | array | Lists the prey in the habitat|

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolf Pack Tracker API setup](getting-started.md)
* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md)
* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)
