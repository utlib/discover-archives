---
layout: default
title: Remove containers from archival description
nav_order: 4
parent: Physical Storage module
permalink: /documentation/physical-storage/remove-containers
---

# Remove containers from archival description  

> Created by Emily Sommers, last modified on Aug 14, 2023

There are two ways to remove containers - a) [manually](#a-manually-unlink) or b) [in bulk via CSV](#b-remove-in-bulk-via-csv)

## A. Manually unlink

Starting from the **Browse Physical Storage page** (![](img/200377644.png) Manage > Physical Storage), click on the name of the container you wish to delete, then delete

![](img/200377646.png)

![](img/200377641.png)

Or from the archival description page, click on the name of the container you wish to delete (must be logged in), then delete

![](img/200377640.png)

![](img/200377641.png)

---

## B. Remove in bulk via CSV

1. Select the descriptions you want to update, add them to the clipboard, and export them

2. Open the CSV in a spreadsheet application

3. Remove the columns you don't intend to change - just make sure you keep and DO NOT CHANGE the **legacyId** column

4. Remove the values from the **physicalObjectName**, **physicalObjectLocation**, **physicalObjectType** columns and save.
5. File a ticket with ITS - email [discoverarchives@library.utoronto.ca](mailto:discoverarchives@library.utoronto.ca)
    * Attach csv spreadsheet
    
    * Ask to have your csv file imported through the command line using the **match-and-update** option, along with the **--roundtrip** and **\--skip-unmatched** options  ([see GoogleGroup discussion thread about bulk updating descriptions](https://groups.google.com/g/ica-atom-users/c/daGpYCj9GAE/m/o3Q1qxGrCgAJ))

6.  If the update was successful, follow-up and ask ITS to run the [command-line task of deleting unlinked physical objects](https://www.accesstomemory.org/en/docs/latest/admin-manual/maintenance/cli-tools/#delete-unlinked-physical-object-locations):

    *   After un-linking containers in bulk, they will still remain in the physical storage module

        *   Rather than deleting them manually 1 by 1, they can be removed in bulk through the command-line.

---

[Edit page on GitHub]()