---
layout: page
---

# Getting started

These are the steps you must do before you can run
the tutorial for the **Wolf Pack Tracker**.

Expect this preparation to take about 20 minutes to complete.

## Preparing to use the Wolf Pack Tracker API

To use the API, you need the following.
You might want to open the links in separate browser tabs before you start installing the software.

* A [GitHub account](https://github.com)
* A development system (PC, Mac, or Linux) running a current or
long-term support (LTS version of the operating system).
* The following software on your development system:
    * [Git](https://docs.github.com/en/get-started/quickstart/set-up-git) (for the command line)
    * [GitHub Desktop](https://desktop.github.com) (optional)
    * A fork of the [Wolf Pack Tracker repo](https://github.com/alkreb/wolf-pack-tracker-au24)
    * A current/LTS version of `node.js`
    * A current version of [json-server](https://www.npmjs.com/package/json-server)
    * A current copy of the database file. You can get this by syncing your fork.
    * **TIP**: If you're using a fork of the repo, create a working branch in which to do your tutorials. Create a new branch for each tutorial to prevent a mistake in one from affecting your work in another.
    * The [Postman desktop app](https://www.postman.com/downloads/). Because you run the **Wolf Pack Tracker** on your development system with an `http://localhost` hostname, the web-version of Postman can't perform the exercises.

## Test your development system

To test your development system:.

1. Create and checkout a test branch of your fork of the Wolf Pack Tracker repo. Your `GitHub repo workspace` is the directory that contains your fork of the `wolf-pack-tracker-au24` repo.

    ```shell
    cd <your GitHub repo workspace>
    ls
    # (see the wolf-pack-tracker-au24 directory in the list)
    cd wolf-pack-tracker-au24
    git checkout -b tutorial-test
    cd api
    json-server -w wolf-pack-tracker-db.json
    ```

    If your development system is installed correctly, you should see
    the service start and display the URL of the service: `http://localhost:3000`.

2. Make a test call to the service.

    ```shell
    curl 'http://localhost:3000/wolves'
    ```

3. If the service is running correctly, you should see a list of wolves.

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

If you don't see the list of wolves, or receive an error in any step
of the procedure, investigate and correct the error before continuing.
Some common situations that cause errors include:

1. You mistyped a command.
2. You aren't in the correct directory.
3. A required software component didn't install correctly.
4. A required software component isn't up to date.

If you see the list of wolves from the service, you're ready for the
the [tutorial](tutorials/tutorials.md).

## More information

* [Wolf Pack Tracker API overview](index.md)
* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md)
* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
    * [Get a single wolf](api/wolves-get-single.md)
    * [Add a wolf](api/wolves-post.md)
    * [Update a wolf](api/wolves-put.md)
    * [Delete a wolf](api/wolves-delete.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)

