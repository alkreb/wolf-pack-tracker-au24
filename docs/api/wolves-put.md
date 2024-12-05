---
layout: page
---

# Put wolf data

Update information for a wolf tracked by the service.

## URL

```shell

url --location --request PUT '{base_url}/packs/{id}'
```

## Parameters

### Path parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|

### Query parameters

None
 

## Request headers

Content-Type: application/json

## Request body

### Request body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|
|`wolf_id` | number | The ID of the wolf|
|`name` | string | The wolf's name|
|`location` | array | The latitude and longitude of the wolf's location|
|`pack_id` | number | The wolf's pack id number|
|`migration_history` | array | The date, latitude, and longitude of the wolf's past migrations. 
|`health_status` |string| Status of the wolf's health|


### Example JSON request body

```json
{
    "id": 1,
    "pack_id": "P001",
    "pack_name": "Northern Wolves",
    "members": [
        "W001",
        "W002",
        "W003",
        "W004"
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
{
    "id": 1,
    "wolf_id": "W001",
    "name": "Alpha",
    "location": {
        "latitude": 45.123,
        "longitude": -112.456
    },
    "pack_id": "P004",
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
    "health_status": "Sick"
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 400 | Error | Invalid request. Check request format. |
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
