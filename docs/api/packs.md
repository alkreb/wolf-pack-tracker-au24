---
layout: page
---

# `packs` resource

Base endpoint:

```shell

{base_url}/packs
```
Location, migration and health information for packs tracked by the service. 

## Resource properties

Sample `packs` resource

```js

{
        "pack_id": "P001",
        "pack_name": "Northern Wolves",
        "members": [
            "W001",
            "W002"
        ],
        "territory": "Northern Forest",
        "migration_pattern": [
            {
                "date": "2024-01-01",
                "latitude": 45,
                "longitude": -112
            },
            {
                "date": "2024-02-01",
                "latitude": 47,
                "longitude": -114
            }
        ]
 },
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
|`pack_id` | number | The ID of the pack|
|`pack_name` | string | The wolf's name|
|`members` | array | Wolves in the pack|
|`territory` | string | Geographical region of the wolf packs territory|
|`migration_pattern` | array | The date, latitude, and longitude of the wolf's migration habits|

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolf Pack Tracker API setup](getting-started.md)
* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md)
* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
* [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)
