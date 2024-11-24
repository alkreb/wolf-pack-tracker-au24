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

```JSON

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
| `id`	|number	|The unique record ID|
|`pack_id` | number | The ID of the pack|
|`pack_name` | string | The wolf's name|
|`members` | array | Wolves in the pack|
|`territory` | string | Geographical region of the wolf packs territory|
|`migration_pattern` | array | The date, latitude, and longitude of the wolf's migration habits|

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../_config.ymltutorials/update-pack-tutorial.md)
* [Wolves resource](wolves.md)
    * [Get all wolves](wolves-get-all.md)
    * [Get a single wolf](wolves-get-single.md)
    * [Add a wolf](wolves-post.md)
    * [Update a wolf](wolves-put.md)
    * [Delete a wolf](wolves-delete.md)
* [Get all packs](packs-get-all.md)
* [Get a single pack](packs-get-single.md)
* [Add a pack](packs-post.md)
* [Update a  pack](packs-put.md)
* [Delete a pack](packs-delete.md)
* [Habitats resource](/habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
