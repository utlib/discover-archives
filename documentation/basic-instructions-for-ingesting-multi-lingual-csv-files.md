---
layout: default
title: Basic Instructions for Ingesting Multi-lingual CSV Files
nav_order: 4
parent: Documentation
permalink: /documentation/basic-instructions-for-ingesting-multi-lingual-csv-files
---

# Basic Instructions for Ingesting Multi-lingual CSV Files

> Created by Kelli Babcock, last modified by Rebekah Bedard on Jun 19, 2023

## Background
In May 2019, UTSC Archivist Tanis Franco sponsored development with Artefactual Systems to enable csv ingest for multi-lingual descriptions.

As a result of this development work, archivists are now able to ingest csv files of multi-lingual descriptions. For example, a fonds with both French and English descriptions can be imported together in 1 csv. Details from Artefactual Systems on this feature can be found at https://projects.artefactual.com/issues/8572. 

The AtoM code branch for this feature (https://github.com/artefactual/atom/commits/dev/2.5.3-uoft) was put into production on Discover Archives in March 2020. The code will be integrated into the next AtoM release, AtoM version 2.6. 

## Ingesting Multi-lingual CSV Files

* Create your csv of descriptions

    * Translations should be in the same csv and alternate language (English 1, Other language 1, English 2, Other language 2)

    * All records MUST HAVE a legacyID and culture column in the csv

        * Current AtoM documentation on the culture column can be found at https://www.accesstomemory.org/en/docs/latest/user-manual/import-export/csv-import/#other-data-entry-notes  

    * legacyID should be the same for records that are translations of each other - ie. you will have records with the same legacyID. That is okay.

    * In the culture column, put the language of description (ISO 639-1 two-letter codes)

        * Remember, AtoM uses ISO 639-1 two-letter codes, NOT 639-2 three-letter codes

    * In summary: when you make the legacyID the same for 2 records but they have different culture values, these will become translations of each other in AtoM

    * Special note: some notes fields will not be imported in multi-lingual csv imports. This includes:

        * languageNote

        * publicationNote

        * generalNote

            * Notes are stored in a different table, and the AtoM method for updating resources via import currently only works for those fields in the primary information_object and information_object_i18n tables. 

    * Do not include any data in taxonomy columns - i.e. LevelOfDescription or Genre (this creates a duplicate Taxonomy terms in English language) - Kelli to report bug to Artefactual Systems

        * Update on this: Sunny found that you can add **levelOfDescription** and **genreAccessPoints** only to the English records (the CSV rows that have 'en' culture value). Don't add taxonomy entries to a non-English culture rows. **PublicationStatus** column is not necessary because it doesn't work with multi-lingual CSV import. All are imported as 'Draft' and you can change publication status of all descendants from its parent description by  more > update publication status > update descendants menu. (Added by TF, Jan 18 '22)

* Ingest your csv as you normally would

* Done!

### UTSC Example
* [Tamil and English csv example](/attachments/TamilTest_20220118.csv)
* Resulting description in Discover Archives: https://discoverarchives-test.library.utoronto.ca/index.php/itak-general-election-candidacy-nomination-form-for-kankesanthurai


## Other background information from Dan Gillean at Artefactual Systems

> When you export a record from AtoM, the values that appear in the legacyID column are AtoM's object ID values. That way, if you were migrating your data to a different system, you could use those unique values much as we use the ID values from other legacy systems when migrating data into AtoM. But of course, the objectID is NOT the legacyID value you might have used during a previous import! This is only stored in the keymap table, and doesn't get exported. 
> 
> The proposed enhancement was a way to add a roundtrip option to AtoM's import code that would ignore all the other more complicated matching criteria, and only look for a match on AtoM's objectID. So you would export a CSV from AtoM, make some updates (or add translation rows), and then re-import the CSV as an update. The values in the legacyID column of that CSV are AtoM's objectID values, which are unique throughout the system, so AtoM would only look for exact matches there, bypassing all the complicated checks used currently, and not requiring you to know the legacyID and sourcename values you used during any previous imports (in fact, your updates could be performed on records that weren't originally imported). 
> 
> For further details see: https://groups.google.com/d/msg/ica-atom-users/OWFFysVAdnk/SLUJ663PAAAJ