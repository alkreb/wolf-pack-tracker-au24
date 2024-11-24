---
layout: page
---

# Put pack data

Update information for a pack tracked by the service.

## URL

```shell

curl --location --request PUT 'http://localhost:3000/packs/1' \
--header 'Content-Type: application/json' \
--data ' {
        "id": 2,
        "pack_id": "P002",
        "pack_name": "Northern Wolves",
        "members": [
            "W001",
            "W002",
            "W003"  
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
    }'
```

## Params

None

## Request headers

None

## Request body

```JSON
{
    "id": 2,
    "pack_id": "P002",
    "pack_name": "Northern Wolves",
    "members": [
        "W001",
        "W002",
        "W003"
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
}
```
## Return body

```JSON
{
    "id": 1,
    "pack_id": "P002",
    "pack_name": "Northern Wolves",
    "members": [
        "W001",
        "W002",
        "W003"
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
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified ID record not found. Use a valid ID. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

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
    * [Delete a pack](packs-delete.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
