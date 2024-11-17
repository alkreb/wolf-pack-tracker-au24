---
layout: page
---

# Delete a wolf

Remove a wolf from the tracking service.

## URL

```shell

curl --location --request DELETE '{base_url}/wolves/{id}' \
--data ''
```

## Params

None

## Request headers

None

## Request body

none

## Return body

none

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Data deleted successfully |
| 404 | Error | Specified ID record not found |
|  ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../_config.ymltutorials/tutorials.md)
* [Wolves resource](wolves.md)
    * [Get all wolves](wolves-get-all.md)
    * [Get a single wolf](wolves-get-single.md)
    * [Add a wolf](wolves-post.md)
    * [Update a wolf](wolves-put.md)
* [Packs resource](packs.md)
    * [Get all packs](packs-get-all.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
* [Prey resource](prey.md)