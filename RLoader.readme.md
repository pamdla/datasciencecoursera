#The way for R loading different file types of data


##xlsx

**use xlsx**

<pre><code>
library('xlsx')
data<-read.xlsx('path/to/xlxsfile',1,sheetName = “Sheet1”,header=TRUE)
</code></pre>

**or, use xlsx2**

<pre><code>
library('xlsx')
read.xlsx2("path/to/excelfile", sheetName = “Sheet1”)
</code></pre>

**or, use XLConnect**

<pre><code>
install.packages("XLConnect")
library("XLConnect")
excel.file <- file.path("path/to/excelfile")
elements <- readWorksheetFromFile(excel.file, sheet=1)
#or
elements <- readWorksheetFromFile(excel.file, sheet="Sheet1")
</code></pre>

**or use gdata**
<pre><code>
require(gdata)
myDf <- read.xls ("path/to/excelfile"), sheet = 1, header = TRUE)
</code></pre>


* Note: for some case, you may encounter failure while loading xlsx.

	If this happened, you need to install jse/jdk dependencies. 

	The latest jse/jdk installer can be found via this link: http://www.oracle.com/technetwork/java/javase/downloads

	* JSE/JDK supports all platforms. Download either jse or jdk and have it installed before you can use xlsx.

* Or for windows users, you may also use RCOM package

	Install [rcom](http://rcom.univie.ac.at/download.html)

	and documentation [How to install](http://homepage.univie.ac.at/erich.neuwirth/php/rcomwiki/doku.php?id=wiki:how_to_install)

	**How to use**

	<pre>
	<code>
	library('rcom')
	readWorksheetFromFile(excel.file, sheet=1)
	</code></pre>


##csv

<pre>
<code>data<-read.csv('path/to/csvfile')</code></pre>



##dat
for pure text format dat file,
<pre><code>
data<-read.table('path/to/datfile')
</code></pre>



##dta

<pre><code>
install.packages("foreign")
require(foreign)
unionData <- read.dta('path/to/dtafile')
</code></pre>
