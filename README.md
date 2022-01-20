# citationRmd
This repository shows how to include references into documents using Citation Style Language styles from [Zotero Style Repository](https://www.zotero.org/styles).

- Step 1. Put all papers into a citation management software and export a list of citations as a `.bib` file. Please see the [`CitationExport.bib`](https://github.com/Bai-Li-NOAA/citationRmd/blob/main/CitationExport.bib) file in this repository.

- Step 2. Write rmarkdown file with citations.

	- Workflow 1: write references section only
	
		- In the rmarkdown header section, include the csl file and the bibliography file. 
		- Use `nocite: '@*'` to show all of the items from the bibliography (see [`ReferencesOnly.Rmd`](https://github.com/Bai-Li-NOAA/citationRmd/blob/main/ReferencesOnly.Rmd) in this repository).
		- Copy paste the references to your working document. Please see [`ReferencesOnly.pdf`](https://github.com/Bai-Li-NOAA/citationRmd/blob/main/ReferencesOnly.pdf) in this repository.
		
	- Workflow 2: Write inline citations
		- In the rmarkdown header section, include the csl file and the bibliography file.
		- Use [@key], [@key1; @key2], or [-@key] to add citations. All the used citations will added to the `#References` section (see [`InlineCitations.Rmd`](https://github.com/Bai-Li-NOAA/citationRmd/blob/main/InlineCitations.Rmd) and [`InlineCitations.pdf`](https://github.com/Bai-Li-NOAA/citationRmd/blob/main/InlineCitations.pdf) in this repository). 

If you would like to add citations to a Google Doc using rmarkdown. You may need to download the Google Doc using `googledrive` package, and convert the word file to rmarkdown file using `rmarkdown::pandoc_convert()`, add following section to the header section of the rmarkdownfile, and then upload the doc back to Google Drive. More helpful instructions can be found here: [https://github.com/nmfs-openscapes/GoogleDrive1](https://github.com/nmfs-openscapes/GoogleDrive1).
 
```rmarkdown
---
notice: |
	@key1, @key2
---
```

* Both fishery-bulletin.csl and fisheries-research.csl were downloaded from [Zotero Style Repository](https://www.zotero.org/styles).
