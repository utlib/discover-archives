---
layout: default
title: Policy on Digital Objects
nav_order: 5
parent: Policies
permalink: /policies/policy-on-digital-objects
---

# Policy on Digital Objects
> Created by Amanda Tome, last modified by Kelli Babcock on Jul 25, 2023

Do not upload digitized objects (i.e. photographs, audio files, video files, DIPs, etc.) directly into Discover Archives.
{: .label .label-yellow }

Digital objects (image files, audio files, video files, DIPs, etc.) can be linked to from descriptions. To do this, use the "[Link to digital object](https://www.accesstomemory.org/en/docs/latest/user-manual/import-export/upload-digital-object/#link-a-single-digital-object-to-an-archival-description)" option when you want to connect a description to a digital object. This allows administrators to link to externally hosted digital objects. This work flow was approved at the September 2017 DASC meeting.

Each repository is responsible for maintaining its links to externally hosted objects.

As of the AtoM 2.4 upgrade, please do not add finding aids as digital objects or digital object links. As of AtoM version 2.4, finding aids can be uploaded (see: [https://www.accesstomemory.org/en/docs/latest/user-manual/reports-printing/print-finding-aid/#print-finding-aids](https://www.accesstomemory.org/en/docs/latest/user-manual/reports-printing/print-finding-aid/#print-finding-aids)). 

**Note**: finding aids should not be uploaded as digital objects, _unless_ a fonds has multiple finding aid files per lower level of description (and until finding aids can be attached at lower levels of description, which will require AtoM development from Artefactual Systems).

This policy may be revised as the needs of Discover Archives group change over time.

## Notes on using "Link to digital object" feature in *Discover Archives*

* For information on adding IIIF images to *Discover Archives*, see [Adding IIIF Images to Discover Archives](https://connect.library.utoronto.ca/display/DA/Adding+IIIF+Images+to+Discover+Archives) (internal U of T documentation)
* In some cases, large digital objects may fail to generate a thumbnail in the AtoM viewer. See ticket [DA-614](https://support.library.utoronto.ca/browse/DA-614) for more information.   
  * In these special cases, contact [discoverarchives@library.utoronto.ca](mailto:discoverarchives@library.utoronto.ca) for assistance. 
  * Continue to **link out** to digital objects instead of uploading digital object files to Discover Archives.
* It's ok to add a non-digital object URL using "Link digital object" menu. In this case, DA fails to generate a thumbnail and metadata from the URL; therefore, following manual changes are necessary.
  * Go to the More > Edit digital object page
  * Change Media Type to 'Image' from 'Audio (default value)'
  * Upload both reference representation and thumbnail representation images.
  * Here's an example: [https://discoverarchives.library.utoronto.ca/index.php/personal-diary-4](https://discoverarchives.library.utoronto.ca/index.php/personal-diary-4) - the thumbnail links to the external URL and it also has a text link with 'Existence and location of copies' label.

---

[Edit page on GitHub]()