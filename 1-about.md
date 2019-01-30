---
layout: default
title: 1-About
nav: true
---

# What is OpenRefine?

OpenRefine is a [free](https://www.gnu.org/philosophy/free-sw.en.html){:target="_blank"}, [open source](https://github.com/OpenRefine/OpenRefine){:target="_blank"}, Java application, that runs offline in a web browser. 

{% include figure.html img="refine.jpg" alt="openrefine interface" width="100%" %}

The original creator, David Huynh, describes Refine as: 

> **“A power tool for working with messy data”**
>
> - more powerful than a spreadsheet
> - more interactive and visual than scripting
> - more provisional / exploratory / experimental / playful than a database
>
> [David Huynh](http://web.archive.org/web/20141021040915/http://davidhuynh.net/spaces/nicar2011/tutorial.pdf){:target="_blank"}

## Exciting Trailers from Google!

If you want a visual introduction, check out these trailers from Google created for an earlier version called GoogleRefine:

- [Introduction](https://youtu.be/B70J_H_zAWM){:target="_blank"}
- [Data Transformation](https://youtu.be/cO8NVCs_Ba0){:target="_blank"}
- [Data Augmentation](https://youtu.be/5tsyz3ibYzk){:target="_blank"}

## Tabular Data 

Refine can handle all sorts of data from all sorts of sources:

- **Import formats:** TSV, CSV, custom separator, Excel, ODF spreadsheet, XML, JSON, RDF, Google Sheets, MARC...
- **Import sources:** local file, archive (zip), URL, clipboard, database, or Google Sheets
- **Output formats:** TSV, CSV, HTML, Excel, ODF spreadsheet, SQL, Wikidata, RDF schema, or custom template

Once imported, the data is represented as tabular, using this basic terminology: 

{% include figure.html img="table.png" alt="table parts" width="100%" %}

Refine is efficient enough to provide comfortable performance up to 100,000's of rows (although, you may want to [increase memory allocated to Java](https://github.com/OpenRefine/OpenRefine/wiki/FAQ:-Allocate-More-Memory){:target="_blank"}).

## Use Cases

**Explore** - navigate and evaluate quality with visualizations and filters that help dig deeply into the data so you can get to know it better...

**Clean** - efficiently discover and fix inconsistency with faceting, clustering, cell transforms, GREL expressions...

**Transform** - easily change formats, subset, or reshape with split/join multi valued cells, split columns, transpose columns/rows...

**Extend** - enrich data by combining files, merging projects, fetching URLs, reconciliation with online databases...

**Automate** - record and preserve your processing routine for transparency, then automate reuse by exporting operation history in JSON!
