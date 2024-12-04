---
layout: page
---

# Add a wolf to a pack

This tutorial adds a wolf to a wolf pack.

You need about 15 minutes to complete this tutorial.

## Step 1: Set up your environment and start the service

Review the [getting started page](../getting-started.md) to get your system set up and the start the service.

## Step 2: Retrieve the packs

Run this command to get a list of packs and their current information. 

```shell

{base_url}/packs
```

A list of packs is returned in the response.  

```json
[
    {
        "id": 1,
        "pack_id": "P001",
        "pack_name": "Northern Wolves",
        "members": [
            "W001",
            "W002"
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
    },
    {
        "id": 2,
        "pack_id": "P002",
        "pack_name": "Eastern Wolves",
        "members": [
            "W003",
            "W004"
        ],
        "territory": "Eastern Mountains",
        "migration_pattern": [
            {
                "date": "2024-03-01",
                "latitude": 48,
                "longitude": -115
            },
            {
                "date": "2024-04-01",
                "latitude": 49,
                "longitude": -116
            }
        ]
    }
]
```

Make note of the members of pack_id P001. This is a list of the wolf_ids for the wolves in the pack. 
In the next step you will add a member to the pack. For this tutorial, you can add a made up wolf_id. If you were actually using the API you would first add the wolf to the [Wolf resource](../api/wolves.md).

## Step 2: Update a pack's information

To update pack P001 to add a wolf (for example, W003), run the following command with your wolf added to the members array. 

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

## Step 3: Verify the response

The response is returned. You can see that your wolf is now a member of the pack. 

```json

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

## What's next?

If you have not practiced adding a wolf to the service yet, try [adding a wolf](add-wolf-tutorial.md).


## More information

* [Wolf Pack Tracker API overview](../index.md)
* [Wolf Pack Tracker API setup](../getting-started.md)
* [Wolves resource](../api/wolves.md)
    * [Get all wolves](../api/wolves-get-all.md)
    * [Get a single wolf](../api/wolves-get-single.md)
    * [Add a wolf](../api/wolves-post.md)
    * [Update a wolf](../api/wolves-put.md)
    * [Delete a wolf](../api/wolves-delete.md)
* [Packs resource](../api/packs.md)
    * [Get all packs](../api/packs-get-all.md)
    * [Get a single pack](../api/packs-get-single.md)
    * [Add a pack](../api/packs-post.md)
    * [Update a  pack](../api/packs-put.md)
    * [Delete a pack](../api/packs-delete.md)
* [Habitats resource](../api/habitats.md)
* [Migration Events resource](../api/migration-events.md)
* [Prey resource](../api/prey.md)
