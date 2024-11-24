---
layout: page
---

# Put pack data

Update information for a pack tracked by the service.

## URL

```shell

curl --location --request PUT '{base_url}/packs/1' \
--header 'Content-Type: application/json' \
--data '{
    
```

## Params

None

## Request headers

None

## Request body

```JSON
{
   
}
```

## Return body

```JSON
{
   
}
```

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | Specified ID record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../_config.ymltutorials/update-pack-tutorial.md)
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
