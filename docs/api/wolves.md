---
layout: page
---

# `wolves` resource

Base endpoint:

```shell

{base_url}/wolves
```

Location, migration and health information for wolves tracked by the service. 

## Resource properties

Sample `wolves` resource

```js

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
|`wolf_id` | number | The ID of the wolf|
|`name` | string | The wolf's name|
|`location` | array | The latitude and longitude of the wolf's location|
|`pack_id` | number | The wolf's pack id number|
|`migration_history` | array | The date, latitude, and longitude of the wolf's past migrations. 
|`health_status` |string| Status of the wolf's health|

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolf Pack Tracker API setup](getting-started.md)
* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md)
* [Get all wolves](api/wolves-get-all.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)
