#The way for R loading different file types of data


##xlsx

**use xlsx**

<pre>
library('xlsx')
data<-read.xlsx('path/to/xlxsfile',1,sheetName = “Sheet1”,header=TRUE)
</pre>

**or, use xlsx2**

<pre>
library('xlsx')
read.xlsx2("path/to/excelfile", sheetName = “Sheet1”)
</pre>

**or, use XLConnect**

<pre>
install.packages("XLConnect")
library("XLConnect")
excel.file <- file.path("path/to/excelfile")
elements <- readWorksheetFromFile(excel.file, sheet=1)
#or
elements <- readWorksheetFromFile(excel.file, sheet="Sheet1")
</pre>

**or use gdata**
<pre>
require(gdata)
myDf <- read.xls ("path/to/excelfile"), sheet = 1, header = TRUE)
</pre>


* Note: for some case, you may encounter failure while loading xlsx.

	If this happened, you need to install jse/jdk dependencies. 

	The latest jse/jdk installer can be found via this link: http://www.oracle.com/technetwork/java/javase/downloads

	* JSE/JDK supports all platforms. Download either jse or jdk and have it installed before you can use xlsx.

* Or for windows users, you may also use RCOM package

	Install [rcom](http://rcom.univie.ac.at/download.html)

	and documentation [How to install](http://homepage.univie.ac.at/erich.neuwirth/php/rcomwiki/doku.php?id=wiki:how_to_install)

	**How to use**

	<pre>
	library('rcom')
	readWorksheetFromFile(excel.file, sheet=1)
	</pre>


##csv

<pre>data<-read.csv('path/to/csvfile')</pre>



##dat
for pure text format dat file,
<pre>
data<-read.table('path/to/datfile')
</pre>



##dta

<pre>
install.packages("foreign")
require(foreign)
unionData <- read.dta('path/to/dtafile')
</pre>
