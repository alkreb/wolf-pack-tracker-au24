---
layout: page
---

# `migration_events` resource

Base endpoint:

```shell

{base_url}/migration_events
```

Wolf migration event information.

## Resource properties

Sample `migration_events` resource

```json

{
        "event_id": "ME001",
        "event_name": "Winter Migration",
        "start_date": "2024-01-01",
        "end_date": "2024-02-28",
        "packs_involved": [
            "P001"
        ],
        "wolves_involved": [
            "W001",
            "W002"
        ],
        "location_path": [
            {
                "date": "2024-01-05",
                "latitude": 45.123,
                "longitude": -112.456
            },
            {
                "date": "2024-01-20",
                "latitude": 46.789,
                "longitude": -113.987
            }
        ]
},
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|
| `event_id` | number | The ID of the migration event|
| `event_name` | string | The name of the event
| `start_date` | string | Date the event starts|
| `end_date` | string | Date the event ends|
| `packs_involved` | array | IDs of the packs involved in the event.|
| `wolves_involved` | array| IDs of the wolves involved in the event |
| `location_path` | array| Date, latitude and longitude of the migration event|


## More Information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Add a wolf tutorial](../tutorials/add-wolf-tutorial.md)
* [Add a wolf to a pack tutorial](../tutorials/update-pack-tutorial.md)
* [Wolves resource](wolves.md)
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
* [Prey resource](prey.md)
