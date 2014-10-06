tika
====
1.File  structure:
	javacode/
		src/
			TSV2XHTMLMain.java
			XHTML2JSONMain.java
			TSVParser.java
			JSONTableContentHandler.java
			XHTMLParser.java
			
		lib/
			commons-lang3-3.3.2.jar
			json-simple-1.1.1.jar
			tika-app-1.6.jar
====================================================================================================================================

2.How to run

	First, import all java filse in javacode/src
	
	Second, import all external jars in javacode/lib
	
	For 3.1 one tsv to one xhtml:
		(1)put a tsv file (original.tsv) into /some/path/original.tsv
		(2)in Eclipse, open TSV2XHTMLMain.java, set 2 arguments: /some/path/original.tsv /some/path/result.xhtml
		(3)after a few seconds, go to /some/path/ to check result.xhtml
		
	For 3.2 one xhtml to n json:
		(1)put a xhtml file (original.xhtml) into /some/path/original.xhtml
		(2)in Eclipse, open XHTML2JSONMain.java, set 2 arguments: /some/path/original.xhtml /some/path/json/
		(3)after a few seconds, go to /some/path/json/, all generated json files are here
		
	For 3.3 a  simple  crawler from n tsv files to m json files:
		(1)put all tsv filse into /some/path/tsv/
		(2)in Eclipse, open CrawlerMain.java, set 2 arguments: /some/path/tsv/ /some/path/json/
		(3)after a few seconds, go to /some/path/json/, all generated json files are here
		
	For 3.5 deduplication:
		(1)put all tsv filse into /some/path/tsv/
		(2)in Eclipse, open DeduplicateMain.java, set 1 arguments: /some/path/tsv/
		(3)we can see the results in the console
