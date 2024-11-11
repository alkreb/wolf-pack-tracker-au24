---
layout: page
---

# Get all wolves

Get information for all wolves tracked by the service.

## URL

```shell

{base_url}/wolves
```

## Params

None

## Request headers

None

## Request body

None

## Return body

```js
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
    },
    {
        "wolf_id": "W002",
        "name": "Beta",
        "location": {
            "latitude": 46.123,
            "longitude": -111.456
        },
        "pack_id": "P001",
        "migration_history": [
            {
                "date": "2024-01-15",
                "latitude": 46.123,
                "longitude": -111.456
            },
            {
                "date": "2024-02-01",
                "latitude": 47.789,
                "longitude": -114.987
            }
        ],
        "health_status": "injured"
    }
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolf Pack Tracker API setup](getting-started.md)
* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md)
* [Wolves resource](api/wolves.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)
