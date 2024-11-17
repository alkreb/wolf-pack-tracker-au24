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

```JSON

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
| `id`	|number	|The unique record ID|
| `habitat_id` | number | The ID of the wolf habitat|
| `location` | string | Geographical region of the wolf habitat|
| `climate` | string | The habitat's climate|
| `prey_population` | array | Lists the prey in the habitat|

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../tutorials/tutorials.md)
* [Wolves resource](wolves.md)
    * [Get all wolves](wolves-get-all.md)
* [Packs resource](packs.md)
    * [Get all packs](packs-get-all.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
