# Object Deletion Tracking

## Description
For saving the GUID of a deleted object for e.g. interfacing purposes for datawarehouse export.

## Typical usage scenario
Use this module to track deletes of objects and save the GUID and type of object in a seperate entity. This can be used to inform other systems like a datawarehouse.

## Features and limitations
Features
- Uses a global before delete event handler for capturing deletes of objects - instead of having to create entity specific before delete event handlers.


## Dependencies
- v1.0.0 for MX 7.23.31 or higher
- v2.0.0 for MX 8.18.19 or higher 
- v2.0.0 for MX 9

## Installation
Download the module and add it to your project.

## Configuration

**1. After Startup**
- Add the microflow `ASU_ObjectDeletion` of the module `ObjectDeletion` to your applications after startup microflow

**2. Configuration overview**
- Add the snippet `SNIP_Configuration` to a page or link to the page `EntityToTrack_Overview` of the `ObjectDeletion` module.

**3. Configuration - To track the deletion of entities**
- Go to the configuration page
- Click `New` and select the entities that you want to track deletes for. This is a simple multi-selection grid.
- Click `Track` and the selection is saved
- Click `Delete` to remove entites from being tracked.
