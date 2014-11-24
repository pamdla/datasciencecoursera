#The way for R loading different file types of data


##xlsx

***use xlsx***
<code>
library('xlsx')
data<-read.xlsx('path/to/xlxsfile',1,sheetName = “Sheet1”,header=TRUE)
</code>

***or use xlsx2:***
<code>
library('xlsx')
read.xlsx2(“myfile.xlsx”, sheetName = “Sheet1”)
</code>

* Note: for some case, you may encounter failure while loading xlsx.

	If this happened, you need to install jse/jdk dependencies. 

	The latest jse/jdk installer can be found via this link: http://www.oracle.com/technetwork/java/javase/downloads

	* JSE/JDK supports all platforms. Download either jse or jdk and have it installed before you can use xlsx.

* Or for windows users, you may also use RCOM package

	Install [rcom](http://rcom.univie.ac.at/download.html)

	and documentation [How to install](http://homepage.univie.ac.at/erich.neuwirth/php/rcomwiki/doku.php?id=wiki:how_to_install)

	***How to use:***

	<code>library('rcom')
	readWorksheetFromFile(excel.file, sheet=1)
	</code>


##csv
<code>data<-read.csv('path/to/csvfile')</code>



##dat
for pure text format dat file,
<code>
data<-read.table('path/to/datfile')
</code>



##dta
<code>install.packages("foreign")
require(foreign)
unionData <- read.dta('path/to/dtafile')
</code>
