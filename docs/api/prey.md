---
layout: page
---

# `habitats` resource

Base endpoint:

```shell

{base_url}/habitats
```

Wolf habitat information.

## Resource properties

Sample`habitats` resource

```js

{
    "user_id": 1,
    "title": "Grocery shopping",
    "description": "eggs, bacon, gummy bears",
    "due_date": "2024-02-20T17:00",
    "warning": "-10",
    "id": 1
}
```

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `user_id` | number | The ID of the user resource to which this task is assigned |
| `title` | string | The title or short description of the task |
| `description` | string | The long description of the task|
| `due_date` | string | The [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format of the date and time the task is due |
| `warning` | number | The number of minutes relative to the `due_date` to alert the user of the task. This is normally a negative number to alert the user before the `due_date`.|
| `id` | number | The task's unique record ID |

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolf Pack Tracker API setup](getting-started.md)
* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md)
* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
