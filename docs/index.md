---
layout: page
---

# Wolf Pack Tracker service API

_This is a mock API to simulate the REST interface of an
imaginary service._

Scientists, conservationist, and naturalists can track information about wolves and wolf packs, including their habitat, migration patterns, health and prey.

## Getting started

The tutorial explains how to set up your system to use the Wolf Pack Tracer API.

* [Wolf Pack Tracker API setup](getting-started.md).


## Tutorial

Learn how to add a wolf to the Wolf Pack Tracker service. 

* [Wolf Pack Tracker API tutorial](tutorials/tutorials.md).

## Reference

The Wolf Pack Tracker API provides the following resources for monitoring wolf packs:

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

**Note:** The API reference docs refer to a `{base_url}` the value depends
on the installation of the service. 
When run locally for testing, the `{base_url}` is
typically  `http://localhost:3000`.
