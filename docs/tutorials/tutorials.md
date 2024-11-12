---
layout: page
---

# Add a wolf to the tracker

The Wolf Pack Tracker lets lets you add wolves to track including their name, location, pack, migration history and health information. 

You need about 20  minutes to complete this tutorial.

## Step 1: Set up your environment

Review the  [getting started page](../getting-started.md) to get your environment set up.

## Step 2: Add your first wolf

To add a wolf run the following command.

```shell
curl --location 'http://localhost:3000/wolves' \
--header 'Content-Type: application/json' \
--data '{
    "wolf_id": "W003",
    "name": "Anubis",
    "location": {
        "latitude": 45.000,
        "longitude": -112.000
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
    "health_status": "injured"
}'
```

## Step 3: Verify the response

The response is returned.  Make note of the id; it may be different in your response.

```shell
{
 {
    "wolf_id": "W003",
    "name": "Anubis",
    "location": {
        "latitude": 45,
        "longitude": -112
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
    "health_status": "injured",
    "id": 3
}
}
```

## Step 3: Retrieve the wolf

To validate the user was added, run the following command. Change the id to match the one returned for the wolf.

```shell
curl --location --request GET 'http://localhost:3000/wolves/3'
```



## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolves resource](../api/wolves.md)
    * [Get all wolves](../api/wolves-get-all.md)
* [Packs resource](../api/packs.md)
    * [Get all packs](../api/packs-get-all.md)
* [Habitats resource](../api/habitats.md)
* [Migration Events resource](../api/migration-events.md)
* [Prey resource](../api/prey.md)
