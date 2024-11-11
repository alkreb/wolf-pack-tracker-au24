---
layout: page
---

# Wolf Pack Tracker service API

This is a mock API to simulate the REST interface of an
imaginary service.

The Wolf Pack Tracer API provides information about wolves and their habitat, migration patterns and health.

You can also track information about migrations, habitat and prey. 

## Getting started

The tutorial explains how to set up your system to use the Wolf Pack Tracer API.

* [Wolf Pack Tracker API setup](getting-started.md).


## Tutorial

Learn how to locate and wolf and determine the wolf's health with in the Wolf Pack Tracker service. 

* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md).

## Reference

The Wolf Pack Tracker API provides the following endpoints for monitoring wolf packs:

* [Wolves resource](api/wolves.md)
    * [Get all wolves](api/wolves-get-all.md)
* [Packs resource](api/packs.md)
    * [Get all packs](api/packs-get-all.md)
* [Habitats resource](api/habitats.md)
* [Migration Events resource](api/migration-events.md)
* [Prey resource](api/prey.md)

**Note:** The API reference docs refer to a `{base_url}` the value depends
on the installation of the service. 
When run locally for testing, the `{base_url}` is
typically  `http://localhost:3000`.
