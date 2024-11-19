---
layout: page
---

# Wolf Pack Tracker service API

_This is a mock API that simulates the REST interface of an
imaginary wolf tracking service._

Scientists, conservationist, and naturalists can track information about wolves and wolf packs. 
The API includes a complete set of wolf tracking data including their habitat, migration patterns, health, and prey.

## Getting started

The tutorial explains how to set up your system to use the Wolf Pack Tracer API.

* [Wolf Pack Tracker API setup](getting-started.md).


## Tutorials

These tutorials give you practice with some common scenarios when using the Wolf Pack Tracker API.

[Learn how to add a wolf to the Wolf Pack Tracker service ](tutorials/tutorials.md).
[Learn how to update the information for a wolf pack]() 

## Reference

The Wolf Pack Tracker API provides the following resources for monitoring wolves and wolf packs:

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

**Note:** The documentation references `{base_url}` throughout. This value depends
on the installation of the service. 
When you are running the service locally for testing, the `{base_url}` is
typically  `http://localhost:3000`.
