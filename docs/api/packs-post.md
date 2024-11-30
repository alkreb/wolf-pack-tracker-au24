---
layout: page
---

# POST a pack

Add a pack to the wolf pack tracker service.

## URL

```shell

curl --location 'http://localhost:3000/packs/'
```

## Parameters

### Path parameters

None

### Query parameters

None


## Request headers

Content-Type: application/json

## Request body

### Request body parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|
|`pack_id` | number | The ID of the pack|
|`pack_name` | string | The packs's name|
|`members` | array | Wolves in the pack|
|`territory` | string | Geographical region of the wolf pack's territory|
|`migration_pattern` | array | The date, latitude, and longitude of the packs's migration habits|

### Example JSON request body

```JSON

{
    "id": "7",
    "pack_id": "P007",
    "pack_name": "Northern packs",
    "members": [
        "W006",
        "W007"
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
|`pack_id` | number | The ID of the pack|
|`pack_name` | string | The packs's name|
|`members` | array | Wolves in the pack|
|`territory` | string | Geographical region of the wolf pack's territory|
|`migration_pattern` | array | The date, latitude, and longitude of the packs's migration habits|

### Example JSON return body

```JSON

{
    "id": "7",
    "pack_id": "P007",
    "pack_name": "Northern packs",
    "members": [
        "W006",
        "W007"
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
| 200 | Success | Requested data returned successfully. |
| 400 | Error | Invalid request. Check request format. |
| Insert failed, duplicate id | Error | Pack is already tracked. Add a new pack|
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
    * [Update a  pack](packs-put.md)
    * [Delete a pack](packs-delete.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)
