---
layout: default
title: Policy on Users
nav_order: 11
parent: Policies
permalink: /policies/policy-on-users
---

# Policy on Users

> Created by Karen Suurtamm, last modified by Emily Sommers on March 20, 2026 (per February 23, 2026 DASC meeting)

## Definitions: User types and permissions[^1]

**Administrator:** An administrator can import, export, create, read, update, publish and delete any record in the system, can customize application to institution specific requirements, and can manage user accounts and profiles.

Administrators can also create new user roles, set granular permissions for that role, and then assign or unassign users from the new role.

**Editor:** an editor can search, browse, create, edit/update, view draft, delete and export descriptions. An editor can also change the publication status of an information object.

**Contributor:** a contributor can search, browse, create, edit/update, view draft and export descriptions. The contributor cannot change the publication status of or delete an information object.

## Policy

1\. Each archival institution will have only 1 administrator user

* If more than 1 administrator user is required by the institution, the addition of more administrators must be discussed with the DASC

* Each archival institution administrator is responsible for creating and maintaining users for their institution

* Usernames will be created using the following conventions: REPOSITORY - lastnamefirstnameinitial - i.e. ITS - babcockk

2\.  Each archival institution can have 1 or more user groups

* Each archival institution administrator is responsible for creating and managing user groups for their institution

  * For example, you may wish to have a user group for staff (who can Create, Update, Delete, View Draft, Publish) and a separate one for student contributors (Create, Update, View Draft) because you want staff to review student work before publishing.

* Each user group will be named with InstitutionLabel Function - i.e. UTARMS Editor

* Each archival institution administrator is responsible for placing their users in the correct user group.

{: .note }
> As of AtoM version 2.10: do not add both a repository "editor" user group in addition to the "administrator" user group. Doing so will result in an error when logged in (see DA-2030 ticket for additional details). Use one or the other.

3\.  Only administrators have permission to edit taxonomies

A taxonomy is a grouping of controlled-vocabulary terms used to generate value lists and access points

* Administrators have Read, Create, Update, Delete permissions

* Editors only have Read permissions

{: .note }
> Before editing a taxonomy, administrators must seek the approval of DASC – *policy forthcoming*

## Documentation

[AtoM documentation for creating and managing
users](https://www.accesstomemory.org/en/docs/latest/user-manual/administer/manage-user-accounts/)

[AtoM documentation for creating and managing user
groups](https://www.accesstomemory.org/en/docs/latest/user-manual/administer/manage-user-accounts/#add-a-new-group)

[^1]: See:
    <https://www.accesstomemory.org/en/docs/latest/user-manual/getting-started/getting-started/#user-roles>
