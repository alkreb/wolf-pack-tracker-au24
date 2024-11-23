---
layout: page
---

# `prey` resource

Base endpoint:

```shell

{base_url}/prey
```

Wolf prey information.

## Resource properties

Sample`prey` resource

```JSON

    {
      "id": 1,
      "prey_id": "PR001",
      "species": "deer",
      "habitat_id": "H001",
      "population_estimate": 200
    }
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id`	|number	|The unique record ID|
| `prey_id` | number | The ID of the prey|
| `species` | string | The name of the species|
| `habitat_id` | number | The ID of the prey's habitat|
| `population_estimate` | number | Number of prey in the habitat|

## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolf Pack Tracker API tutorial](../tutorials/tutorials.md)
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
    * [Update a  pack](packs-put.md)
    * [Delete a pack](packs-delete.md)
* [Habitats resource](habitats.md)
* [Migration Events resource](migration-events.md)
