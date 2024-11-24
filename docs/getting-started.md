---
layout: page
---

# Getting started

Follow these steps to get your system set up and make your first request to the **Wolf Pack Tracker** API**.
Once you are set up, you can try out the tutorials and start using the service. 

It will take about 30 minutes to complete the system setup.

## Prerequisites to use the Wolf Pack Tracker API

To follow the tutorials and test the **Wolf Pack Tracker** make sure you have completed the following:  

1. Create a [GitHub account](https://github.com) if you don't have one already. 
1. Make sure your system (PC, Mac, or Linux) is running a current or supported operating system version.
1. Install [Git](https://docs.github.com/en/get-started/quickstart/set-up-git)
1. (Optional) Install [GitHub Desktop](https://desktop.github.com)
1. Fork the  [Wolf Pack Tracker repo](https://github.com/alkreb/wolf-pack-tracker-au24)
1. Install a current or supported version of `node.js`
1. Install a current version of [json-server](https://www.npmjs.com/package/json-server)
1. (Optional) Install the [Postman desktop app](https://www.postman.com/downloads/). **Note:** The **Wolf Pack Tracker** uses `http://localhost` as hostname, which means the web-version of Postman won't work for the tutorials. 

## Test that you can run the **Wolf Pack Tracker** service

To test that you can run the service:

1. Create a test branch from your fork of the Wolf Pack Tracker repo. 

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (The wolf-pack-tracker-au24 directory displays in the list)
    cd wolf-pack-tracker-au24
    git checkout -b tutorial-test
    cd api
    json-server -w wolf-pack-tracker-db.json
    ```

    If everything is correctly installed, the service starts and displays the URL of the service: `http://localhost:3000`.

2. Send a test request to the service.

    ```shell
    curl 'http://localhost:3000/wolves'
    ```

3. If the service is running correctly, a list of wolves is returned.

    ```js
     [
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
        ...
    ```

If a list of wolves is returned from the service, you can now try the tutorials: 

* [Add a wolf tutorial](tutorials/update-pack-tutorial.md).
* [Update a pack tutorial]()

### Troubleshooting the first request

If a list of wolves is not returned, check the following:

1. Did you type the commands correctly?
2. Are you in the /api directory?
3. Verify that you installed the required software correctly.
4. Verify that you are running the most current or a supported version of the required software.

## What's next

Now that you have the service up and running, you can practice [adding a wolf](tutorials/add-wolf-tutorial.md).

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Add a wolf tutorial](tutorials/add-wolf-tutorial.md)
* [Add a wolf to a pack tutorial](tutorials/update-pack-tutorial.md)
* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
    * [Get a single wolf](api/wolves-get-single.md)
    * [Add a wolf](api/wolves-post.md)
    * [Update a wolf](api/wolves-put.md)
    * [Delete a wolf](api/wolves-delete.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
    * [Get a single pack](api/packs-get-single.md)
    * [Add a pack](api/packs-post.md)
    * [Update a  pack](api/packs-put.md)
    * [Delete a pack](api/packs-delete.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)

