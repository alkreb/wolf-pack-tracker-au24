---
layout: page
---

# `wolves` resource

Base endpoint:

```shell

{base_url}/wolves
```

Location, migration, and health information for wolves tracked by the service. 

## Resource properties

Sample `wolves` resource

```json

{
    "wolf_id": "W001",
    "name": "Alpha",
    "location": {
      "latitude": 45.123,
      "longitude": -112.456
    },
    "pack_id": "P001",
    "migration_history": [
      {
        "date": "2024-01-15",
        "latitude": 45.123,
        "longitude": -112.456
      },
      {
        "date": "2024-01-20",
        "latitude": 46.789,
        "longitude": -113.987
      }
    ],
    "health_status": "healthy"
  },

```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|
|`wolf_id` | number | The ID of the wolf|
|`name` | string | The wolf's name|
|`location` | array | The latitude and longitude of the wolf's location|
|`pack_id` | number | The wolf's pack id number|
|`migration_history` | array | The date, latitude, and longitude of the wolf's past migrations. 
|`health_status` |string| Status of the wolf's health|

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Add a wolf tutorial](../tutorials/add-wolf-tutorial.md)
* [Add a wolf to a pack tutorial](../tutorials/update-pack-tutorial.md)
* [Get all wolves](wolves-get-all.md)
* [Get a single wolf](wolves-get-single.md)
* [Add a wolf](wolves-post.md)
* [Update a wolf](wolves-put.md)
* [Delete a wolf](wolves-delete.md)
* [Packs resource](packs.md)
    * [Get all packs](packs-get-all.md)
    * [Get a single pack](packs-get-single.md)
    * [Add a pack](packs-post.md)
    * [Update a  pack](packs-put.md)
    * [Delete a pack](packs-delete.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
