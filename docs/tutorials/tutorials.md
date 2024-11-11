---
layout: page
---

# Tutorial


Learn how to add a wolf. 

The Wolf Pack Tracker lets lets you add wolves to track including their name, location, pack, migration history and health information. 

You need about 20  minutes to complete this tutorial.

## Step 1: Set up your environment

Review the  [getting started page](../getting-started.md) to get your environment set up.

## Step 2: Add your first wolf

To add a wolf run the following command.

```
curl --location 'http://localhost:3000/wolves' \
--header 'Content-Type: application/json' \
--data-raw '{
    "wolf_id": "W006",
    "name": "Anubis",
    "location": {
      "latitude": 45.000,
      "longitude": -112.000
    },
    "pack_id": "P002",
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
  }'
```

## Step 3: Verify the response

The response is returned.  Make note of the user's id; it may be different in your response.

```
{
 "last_name": "Smith",
 "first_name": "Apple",
 "email": "apple.smith@example.com",
 "id": 8
}
```

## Step 3: Retrieve the user
To validate the user was added, run the following command. Change the id to match the one returned for your user.

```
curl --location --request GET 'http://localhost:3000/users/8'
```

Now that you have added a user to the To-do service, you can [add a new task for the user](../tutorials/add-a-new-task.md).


## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)
