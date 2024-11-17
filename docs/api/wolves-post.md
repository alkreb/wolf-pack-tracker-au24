---
layout: page
---

# POST a wolf

Add a wolf to the wolf tracker service.

## URL

```shell

curl --location '{base_url}/wolves/' \
--header 'Content-Type: application/json' \
--data '{
    "id": 7,
    "wolf_id": "W007",
    "name": "Belle",
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
    "health_status": "pregnant"
}'
```

## Params

None

## Request headers

None

## Request body
```JSON
{
    "id": 7,
    "wolf_id": "W007",
    "name": "Belle",
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
    "health_status": "pregnant"
}
```

## Return body

```JSON

    "id": 7,
    "wolf_id": "W007",
    "name": "Belle",
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
    "health_status": "pregnant"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| Insert failed, duplicate id | Error | Wolf is already tracked. Add a new wolf|
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../_config.ymltutorials/tutorials.md)
* [Wolves resource](wolves.md)
    * [Get all wolves](wolves-get-all.md)
    * [Get a single wolf](wolves-get-single.md)
    * [Update a wolf](wolves-put.md)
    * [Delete a wolf](wolves-delete.md)
* [Packs resource](packs.md)
    * [Get all packs](packs-get-all.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
