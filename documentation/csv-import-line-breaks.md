---
layout: default
title: CSV Import - How to Clean up Control Characters/Leading Line Breaks from CSV
nav_order: 3
parent: Documentation
permalink: /documentation/csv-import-line-breaks
---

# CSV Import: How to Clean up Control Characters/Leading Line Breaks from CSV  

> Created by Sunny Lee, last modified on Apr 04, 2022

AtoM's CSV import doesn't trim unnecessary leading line breaks. As a result, AtoM stores them in the database. They don't display on each object page but they cause messy or broken CSV exports.

Example of hidden paragraphs control characters in the AtoM db:

![](/img/156828748.png)

Example of hidden paragraphs control characters in CSV export:

![](/img/156828750.png)

## For Mac User, Export Data Using Numbers

If you are a Mac user, open a CSV file with Numbers. It will render all columns correctly ignoring control characters.

It removes hidden characters when you export data using using File > Export to 'Excel' or 'CSV'.

![](/img/156828749.png)

## Regular Expression: Find and Replace


In your preferred text editor, run regular expression *find & replace*. 

Replace ``,"\\n\[\\n\]+`` with ``,"``

![](/img/156828752.png)

## Edit/Review CSV Using OpenRefine

Excel or Google spreadsheet excludes leading line breaks in their cell display and you can detect them when you click the cell. Therefore, you can't notice the problem while reviewing data.

![](/img/156828753.png)

If you use OpenRefine, it displays leading line breaks more accurately so that you can easily identify extra line breaks. Other than that, OpenRefine is a powerful tool for cleaning and transforming data.

For details, refer to its website: [https://openrefine.org/](https://openrefine.org/)

![](/img/156828754.jpg)