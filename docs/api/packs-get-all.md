---
layout: page
---

# Get all packs

Get information for all packs tracked by the service.

## URL

```shell

{base_url}/packs
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
    ...
]
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../tutorials/tutorials.md)
* [Get all wolves](wolves-get-all.md)
    * [Get all wolves](wolves-get-all.md)
* [Packs resource](packs.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
