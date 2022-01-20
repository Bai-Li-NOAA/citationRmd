# citationRmd
This repository shows two workflows of how to include references into documents using Zotero citation styles


- Step 1. Put all papers to a citation management software and export a list of citations as a `.bib` file. Please see the `CitationExport.bib` file in this repository.

- Step 2. Write rmarkdown file with citations.

	- Workflow 1: write references section only
	
		- In the rmarkdown header section, include the csl file and the bibliography file. 
		- Use `nocite: '@*'` to show all of the items from the bibliography (see `ReferencesOnly.Rmd` in this repository).
		- Copy paste the references to your working document. Please see `ReferencesOnly.pdf` in this repository.
		
	- Workflow 2: Write inline citations
		- In the rmarkdown header section, include the csl file and the bibliography file.
		- Use [@key], [@key1; @key2], or [-@key] to add citations. All the used citations will added to the `#References` section (see `InlineCitations.Rmd` and `InlineCitations.pdf` in this repository). 

*All csl files were downloaded from [Zotero Style Repository](https://www.zotero.org/styles).

If you would like to add citations to a Google Doc using rmarkdown file. You may need to download the Google Doc using `googledrive` package, and convert the word file to rmarkdown file using `rmarkdown::pandoc_convert()`, then add following section to the header section of the rmarkdownfile. More helpful instructions can be found here: [https://github.com/nmfs-openscapes/GoogleDrive1](https://github.com/nmfs-openscapes/GoogleDrive1).
 
```rmarkdown
---
notice: |
	@key1, @key2
---
```

