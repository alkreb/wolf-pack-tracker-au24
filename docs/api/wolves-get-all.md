---
layout: page
---

# Get all wolves

Get information for all wolves tracked by the service.

## URL

```shell

{base_url}/wolves
```

## Parameters

### Path parameters

None

### Query parameters

None

## Request headers

Content-Type: application/json

## Request body

None

## Return body

### Return body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|
|`wolf_id` | number | The ID of the wolf|
|`name` | string | The wolf's name|
|`location` | array | The latitude and longitude of the wolf's location|
|`pack_id` | number | The wolf's pack id number|
|`migration_history` | array | The date, latitude, and longitude of the wolf's past migrations. 
|`health_status` |string| Status of the wolf's health|


### Example JSON return body

```json
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
| 400 | Error | Invalid request. Check request format. |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Add a wolf tutorial](../tutorials/add-wolf-tutorial.md)
* [Add a wolf to a pack tutorial](../tutorials/update-pack-tutorial.md)
* [Wolves resource](wolves.md)
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
