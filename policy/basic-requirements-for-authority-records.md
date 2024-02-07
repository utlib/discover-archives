---
layout: default
title: Basic Requirements for Authority Records
nav_order: 2
parent: Policies
permalink: /policies/basic-requirements-for-authority-records
---

# Basic Requirements for Authority Records
> Created by Amanda Tome, last modified by Kelli Babcock on Nov 08, 2023

## PURPOSE
The following document outlines the minimum requirements for authority records in *Discover Archives*. The corresponding rule from ISAAR (CPF) for each element listed has been provided for reference.

Material consulted: International Standard Archival Authority Record For Corporate Bodies, Persons and Families, 2nd edition.

---

### Identity area

**Type of entity (5.1.1) - Mandatory**

Choose the type of entity (Person, Corporate Body or Family) that is being described in the authority records.

**Authorized name (5.1.2) - Mandatory**

Record the standardized form of the name for the entity in the authority record.

Do not record dates of existence in brackets in this field
{: .label .label-yellow }

### Description area

**Dates of existence (5.2.1) - Recommended**

Record the date of existence for the entity being described.

**History (5.2.2) - Recommended**

Record the administrative history or biographical history of the creator(s). This information is entered in the creator(s) authority record and automatically links to the description when the name of the creator is added.

This information will form the Administrative history / Biographical history for your description.

### Relationships Area

**Description of Relationship (5.3.3) - Recommended**

Record the nature of the relationship between the creators.

As of AtoM version 2.6, the relationship field appears in the People and Organization Advanced Search. This means Discover Archives repositories should assign consistent relationship types across authority records so that expected results appear when users make use of the relationship field. See the [AtoM Authority records documentation](https://www.accesstomemory.org/en/docs/latest/user-manual/add-edit-content/authority-records/) for more details on entering data into these fields.

[If in doubt please also refer to ISAAR 5.3](https://www.ica.org/sites/default/files/CBPS_Guidelines_ISAAR_Second-edition_EN.pdf).
{: .label .label-yellow }

| **Category of relationship** | **Relationship type**                        | **Used by**                                        | **Use when** |
|------------------------------|----------------------------------------------|----------------------------------------------------|--------------|
| hierarchical                 | controls / is controlled by                  | Victoria University Archives                       |              |
| hierarchical                 | is the owner of / is owned by                |                                                    |              |
| hierarchical                 | is the subordinate of / is the superior of   |                                                    |              |
| temporal                     | is the successor / is the predecessor        | Victoria University Archives                       |              |
| family                       | is the child of / is the parent of           | Victoria University Archives<br>East Asian Library |              |
| family                       | is the grandchild of / is the grandparent of | Victoria University Archives                       |              |
| family                       | is the sibling of                            | Victoria University Archives                       |              |
| family                       | is the spouse of                             | Victoria University Archives<br>East Asian Library |              |
| family                       | is the cousin of                             |                                                    |              |
| associative                  | is the associate of                          | Victoria University Archives                       |              |
| associative                  | is the business partner of                   |                                                    |              |
| associative                  | is the client of                             |                                                    |              |
| associative                  | is the friend of                             |                                                    |              |
| associative                  | is the provider of                           |                                                    |              |

### Control Area

**Authority record identifier (5.4.1) - Recommended**

If the authorized form of the name is taken from an authority records database, record the unique identifier of the authority record. Otherwise leave the field blank. The recommended authority to use for authority record identifiers is [VIAF](https://viaf.org/).

Please use VIAF url when available.
{: .label .label-green }
Example - [Claude Bissell](https://discoverarchives.library.utoronto.ca/index.php/bissell-claude-3)
Authority record identifier: [http://viaf.org/viaf/44326760](http://viaf.org/viaf/44326760)

**Maintaining repository (5.4.2) - Mandatory**

Select from the dropdown menu the repository that oversees the authority record

If more than one repository manages an authority record, decide by consensus which repository should be responsible for maintaining it. Record in the next field (Institution identifier) the names of the two institutions.
{: .label .label-yellow }

**Institution identifier (5.4.2) - Optional**

If two or more repositories are responsible for creating, maintaining and modifying and authority records, record the repositories name here.