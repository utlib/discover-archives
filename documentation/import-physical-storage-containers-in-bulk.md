---
layout: default
title: Import Physical Storage Containers (in bulk)
nav_order: 2
parent: Physical Storage module
grand_parent: Documentation
permalink: /documentation/physical-storage/import-physical-storage-containers-in-bulk
---

# Import Physical Storage Containers (in bulk)  

> Created by Emily Sommers, last modified by Rebecca Shaw on Aug 28, 2023

These are instructions for adding storage containers to **existing archival description** in bulk through a command-line task.

**NOTE:** This method can be used to update existing containers using the ``–update`` flag (e.g. if we ever decided to add more specific location information to containers)

**Official AtoM documentation:** [https://www.accesstomemory.org/en/docs/latest/admin-manual/maintenance/cli-import-export/#import-physical-storage-containers-and-locations](https://www.accesstomemory.org/en/docs/latest/admin-manual/maintenance/cli-import-export/#import-physical-storage-containers-and-locations)

---

## 1. Download a copy of the your data

### A few collections:

1. Add them to clipboard

2. Go to clipboard and export

3. Make sure to select Format: CSV

![](attachments/200377631/200377633.png)

### All your data:

*   Email [discoverarchives@library.utoronto.ca](mailto:discoverarchives@library.utoronto.ca) and ITS can provide a bulk export from the command-line.

## 2. Fill out the physicalobjects.csv template

Using the values from your recently downloaded data, fill out the **[physicalobjects csv template](/attachments/example-physical-objects-2_6.csv)**.

The CSV template contains 6 columns, summarized below. Columns with ``*`` are new; other columns are to be copied from your existing data.

| **Column**       | **Description**                                                                                                                                                                                                                                                                       |
|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| legacyID         | Not required for new import data, but recommended as it can facilitate matching.                                                                                                                                                                                                      |
| name ``*``       | Free-text. The container name to be used                                                                                                                                                                                                                                              |
| type ``*``       | Type of container. Links to AtoM’s Physical Object Type taxonomy. <br>Use **Box**, **Folder**, or **Digital Folder** <u>only</u>.                                                                                                                                                     |
| location ``*``   | Free text. Used to add information about a container’s location.<br>Enter your repository’s acronym.                                                                                                                                                                                  |
| culture ``*``    | Language of the import data. Expects ISO 639-1 two-letter language codes.<br>If left unpopulated, it will default to ``en`` during import.                                                                                                                                            |
| descriptionSlugs | Multi-value input for the [slugs](https://www.accesstomemory.org/en/docs/latest/user-manual/glossary/glossary/#term-slug) of related archival descriptions.<br>When linking a container row to multiple archival descriptions, separate each slug value with a ``\|`` pipe separator. |

**Example:**

| **legacyId** | **name**           | **type** | **location** | **culture** | **descriptionSlugs**                                 |
|--------------|--------------------|----------|--------------|-------------|------------------------------------------------------|
| 35191        | B2015-0004/001     | Box      | UTARMS       | en          | biographical-and-early-education                     |
| 35191        | B2015-0004/002     | Box      | UTARMS       | en          | biographical-and-early-education                     |
| 35191        | B2015-0004/003     | Box      | UTARMS       | en          | biographical-and-early-education                     |
| 35191        | B2015-0004/004     | Box      | UTARMS       | en          | biographical-and-early-education                     |
| 35191        | B2015-0004/005     | Box      | UTARMS       | en          | biographical-and-early-education                     |
| 35191\|34991 | B2015-0004/006     | Box      | UTARMS       | en          | biographical-and-early-education\|correspondence-221 |
| 34991        | B2015-0004/007     | Box      | UTARMS       | en          | correspondence-221                                   |
| 34991        | B2015-0004/008     | Box      | UTARMS       | en          | correspondence-221                                   |
| 34991        | B2015-0004/009     | Box      | UTARMS       | en          | correspondence-221                                   |
| 54291        | B2015-0004/006(09) | Folder   | UTARMS       | en          | correspondence-re-dr-bondar                          |

HINT: 
{: .label .label-yellow }

To join multiple slugs together..

*   Paste slugs column into a text editor like Visual Studio Code or Notepad++
*   Use **Find & Replace**  
    *   Windows: Replace: ``\r\n``
    *   Unix: Replace: ``\n``
    *   With: ``|``
*   Make sure Regular Expression is selected

## 3. File a ticket with ITS

Email [discoverarchives@library.utoronto.ca](mailto:discoverarchives@library.utoronto.ca) with the csv file and request the physical storage data to be imported through the command-line.

Reference this documentation page: https://www.accesstomemory.org/en/docs/latest/admin-manual/maintenance/cli-import-export/#import-physical-storage-containers-and-locations