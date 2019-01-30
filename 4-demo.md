---
layout: default
title: 4-Demo
nav: true
---

# Basics

**Demo data downloads:**

- [`universityData.csv`](assets/universityData.csv){:target="_blank"}, a data set about University endowments harvested from Wikipedia—so it is very *messy*! (from the [Enipedia OpenRefine Tutorial](http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial){:target="_blank"})
- [`doaj-article-sample.csv`](assets/doaj-article-sample.csv){:target="_blank"}, citations harvested from DOAJ (from [Library Carpentry OpenRefine](https://librarycarpentry.org/lc-open-refine/){:target="_blank"})
- [`potlatch-historical-collection.csv`](assets/potlatch-historical-collection.csv){:target="_blank"}, metadata from a digital collection (from [University of Idaho Library](https://www.lib.uidaho.edu/digital/){:target="_blank"}).

**Create Project:**

- "Get data from" options
- "Configure Parsing Options", *check character encoding* and options, then give your project a name (names are easier to work with if there are no spaces or dashes) and click Create project.
- Refine never over writes your original data, it creates a copy!
- Information is *not* sent over internet. The data is copied into your workspace directory in Refine's specialized format (find your workspace directory by looking for the link at the bottom of the "Open Project" page).
- **Sanity Check**, ensure you have the expected number of rows! Keep this number in mind as you work through the project.

## Column basics

Unlike most spreadsheets which focus on rows, Refine is column-centric.
Most operations are accessed via the column menus.

Explore:

- Text filter
- Facet > Text facet
- Facet > Customized facets > Facet by blank

Edit: 

- Edit individual cells (hover on value)
- Edit facets
- Transform column
    - Edit cells > Common Transformations > Trim leading and trailing whitespace
    - Edit cells > Transform > use [GREL](https://github.com/OpenRefine/OpenRefine/wiki/General-Refine-Expression-Language){:target="_blank"}
        - add text, `value + " something new"`
        - find & replace, `value.replace("old","new")`
        - GREL helpers, e.g. `value.unescape('url')`
        - get values from other cells, `cells['column_name'].value`
        - [GREL dates](https://github.com/OpenRefine/OpenRefine/wiki/GREL-Date-Functions){:target="_blank"}, `value.toDate().toString('yyyy-MM-dd')`
- Create new columns
    - Edit column > Add column based on... `value.length()`
    - Edit column > Split into several columns... 
    - *Note:* combining columns can be tricky because combining blank cells results in an error. Thus facet by blank first and combine only non-empty cells with a transform like `value + " " + cells["col 2"].value`
- Work with multi-valued cells
    - Edit cells > Split multi-valued cells... 
    - Edit cells > Cluster and edit...
- All column
    - Star, Flag
    - Edit rows > Remove all matching rows
    - Edit columns > Re-order / remove columns
- Deduplicate
    - Sort... 
    - Sort menu will appear at top of table, select "Reorder rows permanently"
    - Edit cells > Blank down, then facet on blank and remove rows

## Project basics 

Export:

- *Keep in mind:* export is always a new copy of data, never alters original! Your Refine projects will be automatically saved in your working directory and can be accessed from "Open Project" tab.
- Many export formats!
- templating

Undo / Redo & Automate:

- Undo / Redo
- Undo / Redo > Extract, copy json to txt file (use text editor, not Word)
- Undo/Redo > Apply, paste in saved extract and click Perform Operations

# Fetching and Parsing HTML

- [Sonents lesson](sonnets-demo.html) demonstrates simple fetching html, parsing HTML, using GREL arrays, and ends with an advanced use of Jython to access an API.
- [Chronam lesson](chronam-demo.html) demonstrates using Refine's build in fetch and parsing to access a simple web api.
