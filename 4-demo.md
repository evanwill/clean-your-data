---
layout: default
title: 4-Demo
nav: true
---

# Demo: University Data

In this demo we are going to play with a data set about University endowments harvested from Wikipedia—so it is very *messy*! 

Download <a href="assets/universityData.csv" target="_blank">`universityData.csv`</a>

> The university endowment demo data is from the [Enipedia OpenRefine Tutorial](http://enipedia.tudelft.nl/wiki/OpenRefine_Tutorial){:target="_blank"}. 

- Create project 
    - check character encoding, options
    - Refine never over writes your original data, it creates a copy!
    - information is *not* sent over internet

- Column basics
    - text filter
    - faceting
    - edit cells / facets
    - transform, `value.unescape('url')`, find & replace, `value.replace("old","new")`
    - add column based on, `value.length()`, numeric facet
    - undo/redo
    - clustering
	- split into multiple columns
    - combine columns (*tricky* because combining blank cells results in an error)
        - facet by blank, combine only non-empty cells
        - transform, `value + " " + cells["col 2"].value`
    - remove / reorder columns 

- Export basics
	- OpenRefine project
    - many formats!
    - templating
	- export is always a new copy of data, never alters original!
	
- Automate basics
	- Undo/Redo copy `Extract` to txt file (use text editor, not Word)
	- create new project with original file
	- Undo/Redo paste saved extract into `Apply` 

- More!
	- Star / Flag & remove rows
	- create new column with transform `length(value)`, numeric facet
	- deduplicate
		- sort by, permanent reorder
		- blank down / fill down 
    - fetch URLs
        - basic geo code lookup, `"http://maps.google.com/maps/api/geocode/json?sensor=false&address=" + escape(value, "url")
with(value.parseJson().results[0].geometry.location, pair, pair.lat +", " + pair.lng)`

# Demo: Fetching and Parsing HTML

- [Sonents lesson](sonnets-demo.html) demonstrates simple fetching html, parsing HTML, using GREL arrays, and ends with an advanced use of Jython to access an API.
- [Chronam lesson](chronam-demo.html) demonstrates using Refine's build in fetch and parsing to access a simple web api.
