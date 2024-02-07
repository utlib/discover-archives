---
layout: default
title: Include physical storage containers in a new CSV import
nav_order: 3
parent: Physical Storage module
permalink: /documentation/physical-storage/include-physical-storage-new-csv-import
---

# Include physical storage containers in a new CSV import  

> Created by Rebecca Shaw, last modified on Aug 28, 2023

These are instructions for adding storage containers to **new archival descriptions** using the CSV import function.

* **Official AtoM documentation:** [https://www.accesstomemory.org/en/docs/latest/user-manual/import-export/csv-import/#physical-object-related-import-columns](https://www.accesstomemory.org/en/docs/latest/user-manual/import-export/csv-import/#physical-object-related-import-columns)

---

To include physical storage containers as part of a new CSV import, your CSV file must include the following columns:

_physicalObjectName_: The Name of your physical storage container. This can be a new or existing container.

_physicalObjectLocation:_ The Location of your physical storage container. In accordance with the DASC [policy for the Physical Storage module](/discover-archives/policy/policy-on-physical-storage-module), the location field must begin with the name or acronym of your repository.

_physicalObjectType:_ Selected from the physical storage taxonomy. Options are: Box, Folder, Digital Folder.

To attach multiple physical storage containers to the same record via CSV import, use a pipe character ("|") to separate each container. All three columns must have the same number of pipe characters, e.g.:

![](img/202899603.png)

All three columns must be completed to correctly import physical storage container information.

Download official AtoM CSV templates: https://wiki.accesstomemory.org/Resources/CSV_templates

---

[Edit page on GitHub]()