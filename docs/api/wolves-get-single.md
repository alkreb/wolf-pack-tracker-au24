---
layout: page
---

# Get all wolves

Get information for a wolf tracked by the service.

## URL

```shell

{base_url}/wolves?wolf_id={wolf_id}
```

## Params

None

## Request headers

None

## Request body

None

## Return body

```JSON
[
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
    }.   
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified wolf_id record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../_config.ymltutorials/tutorials.md)
* [Wolves resource](wolves.md)
    * [Get all wolves](wolves-get-all.md)
    * [Add a wolf](wolves-post.md)
    * [Update a wolf](wolves-put.md)
    * [Delete a wolf](wolves-delete.md)
* [Packs resource](packs.md)
    * [Get all packs](packs-get-all.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
