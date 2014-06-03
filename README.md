playgroud
=========

my personal playground





+++++++++++++++++++++++++++++Test

mat-imageimporteditor
=====================

# Desc
This is a subset of managment-tools created for the imageimport on backend of www.michas-ausflugstipps.de/.

1. allinone html-editor to prepare import of image-dirs to mediadb (more infos on www.michas-ausflugstipps.de/portal-datenpflege.html)
2. imagedir-import-generator to prepare json-files for the imageimport-editor

# TODO for me
- [ ] documentation
- [ ] externalize config
- [ ] use and optimize it :-)

# History and milestones
- 2014 
   - prepared the tools for going public (documentation...) 
   - separated the public-tools
- 2014
   - initial version based on the original java+excel-tools

# Requires
- for building
   - maven
   - IDE (I built it with eclipse)
- for run
   - java
   - browser with html5-support

# Install
- save the project to 
```bat
d:\public_projects\ImageImportEditor
```

- import project to Eclipse

- run maven 
```bat
cd d:\public_projects\ImageImportEditor
mvn compile
mvn org.apache.maven.plugins:maven-assembly-plugin:assembly
```

# Example
- save your jpg-images at 
```bat
D:\Bilder\digifotos\test\20140304-berlin\
D:\Bilder\digifotos\test\20140305-muenchen\
D:\Bilder\digifotos\test\20140307-hamburg\
```

- run generator
```bat
echo off
cd d:\public_projects\ImageImportEditor
sbin\genImageDirImportEntries.bat D:\Bilder\digifotos\test > d:\tmp\importDigiFotos-test.json
```

- open editor
```bat
cd d:\public_projects\ImageImportEditor
firefox web\ImageImportEditor.html
```

- open jsonfile in firefox:ImageImportEditor.html
```bat
d:\tmp\importDigiFotos-test.json
```

# License
```
/**
 * @author Michael Schreiner <ich@michas-ausflugstipps.de>
 * @category publishing
 * @copyright Copyright (c) 2005-2014, Michael Schreiner
 * @license http://mozilla.org/MPL/2.0/ Mozilla Public License 2.0
 *
 * This Source Code Form is subject to the terms of the Mozilla Public
 * License, v. 2.0. If a copy of the MPL was not distributed with this
 * file, You can obtain one at http://mozilla.org/MPL/2.0/.
 */
```

+++++++++++++++++++++++++++++Test2



mat-cmdprinting plugin for firefox
=====================

# Desc
A firefox-plugin that prints Urls to PDF direct from the commandline.
It is customized for printing www.michas-ausflugstipps.de.

Bases on cmdprinting from from O. Atsushi https://sites.google.com/site/torisugari/commandlineprint2 
whose module was broken since firefox 4.X. Many Thanks to him for the idea and some of the code.

# TODO for me
- [ ] use and optimize it :-)
- [ ] if plugin is activated sometimes firefox has layoutproblems

# History and milestones
- 2014 
   - prepared the tools for going public (documentation...) 
   - separated the public-tools
- 2011
   - initial version for www.michas-ausflugstipps.de/portal-bucherstellung.html

# Requires
- for building
   - zip
- for use
   - firefox > 4.0

# Install
- save the project to 
```bat
d:\public_projects\matcmdprinting
```

- configure the project
```bat
d:\public_projects\matcmdprinting\config\config.bat
```

- import project to Eclipse

- run installer 
```bat
cd d:\public_projects\matcmdprinting
install\install.bat
```

# Example
- change  
   - tests/test.bat

- run  
```bat
cd d:\public_projects\matcmdprinting
tests\test.bat
```


# License
```
/**
 * @author Michael Schreiner <ich@michas-ausflugstipps.de>
 * @author Inspired by cmdprinting from from O. Atsushi torisugari@gmail.com whose module was broken since firefox 2.X. Many Thanks to him for the idea and some of the code.
 * @category publishing
 * @copyright Copyright (c) 2011-2014, Michael Schreiner
 * @license http://mozilla.org/MPL/2.0/ Mozilla Public License 2.0
 *
 * This Source Code Form is subject to the terms of the Mozilla Public
 * License, v. 2.0. If a copy of the MPL was not distributed with this
 * file, You can obtain one at http://mozilla.org/MPL/2.0/.
 */
```

+++++++++++++++++++++++++++++Test 3

mat-publishtools
=====================

# Desc
This is a subset of publishing-tools created for Michas-Books on www.michas-ausflugstipps.de/portal-bucherstellung.html

1. PDF-tools for converting, merge, trim and so on
2. batchfiles for support
3. batchfiles for generating a book with pagenum and TOC from different webpages

# TODO for me
- [ ] documentation
- [ ] use and optimize it :-)

# History and milestones
- 2014 
   - prepared the tools for going public (documentation...) 
   - separated the public-tools
- 2011
   - initial version for www.michas-ausflugstipps.de

# Requires
- for building
   - maven
   - IDE (I built it with eclipse)
- to manage pdfs
   - java
- to generate pdfs
   - wkhtmltopdf-0.9.9
   - optional wkhtmltopdf-0.11
   - optional firefox + www.github.com/dat-micha/matcmdprinting
- to convert pdfs
   - optional FreePDF 4.12
   - optional ghostScript 9.07


# Install
- save the project to 
```bat
d:\public_projects\PublishTools
```

- import project to Eclipse

- run maven 
```bat
cd d:\public_projects\PublishTools
mvn compile
mvn org.apache.maven.plugins:maven-assembly-plugin:assembly
```

# Configure
- update pathes in 
   - config/config-contentloader.bat
   - config/config-converter.bat
   - config/config-pdftools.bat

# Example
- change  
   - src/test/example/buch-example.bat (define urls in section load)
   - src/test/example/buch-example.lst (list your file from example.bat section load)

- run test
```bat
cd d:\public_projects\PublishTools
src\test\example\buch-example.bat
```

# License
```
/**
 * @author Michael Schreiner <ich@michas-ausflugstipps.de>
 * @category publishing
 * @copyright Copyright (c) 2010-2014, Michael Schreiner
 * @license http://mozilla.org/MPL/2.0/ Mozilla Public License 2.0
 *
 * This Source Code Form is subject to the terms of the Mozilla Public
 * License, v. 2.0. If a copy of the MPL was not distributed with this
 * file, You can obtain one at http://mozilla.org/MPL/2.0/.
 */
```

+++++++++++++++++++++++++++++Test 4

dps-msfinancetools
=====================

# Desc
A toolset for financeplaning an management
It contains Excel-sheets and some java-progs to convert data between them.
But be aware the whole Excel-Sheets are in german language ;-)

## "Finanzplanung"
With excel/finanzplanung.xls you can configure and play finance-szenarios like: 
how will be your finance-situation if you are unemployed or you will buy your 
own house.
 
## "Haushaltsbuch"
With excel/haushaltsbuch.xls you can plan and document your whole payments.

## "Finanzübersicht"
After data-export from "Finanzplanung" with the javaprogs, you can
analyse them in excel/finanzuebersicht.xls. It gives you an overview over your
payments and visualizes trends and so on with the help of charts.

# TODO for me
- [ ] documentation
- [ ] use and optimize it :-)

# History and milestones
- 2014 
   - prepared the tools for going public (documentation...) 
   - separated the public-tools
- 2013
   - first version of finanzplanung.xls
- 2007
   - java-progs and first version of finanzuebersicht.xls
- 2006
   - extended version of the excel haushaltsbuch.xls
- 2003
   - initial version of the excel haushaltsbuch.xls

# Requires
- for building
   - maven
   - IDE (I built it with eclipse)
- to use
   - excel
- to manage and synchronize
   - java

# Install
- save the project to 
```bat
D:\public_projects\MsFinance
```

- import project to Eclipse

- run maven 
```bat
cd d:\public_projects\MsFinance
mvn compile
mvn org.apache.maven.plugins:maven-assembly-plugin:assembly
```

# Configure
- update pathes in 
   - config/config-msfinance.bat

# Example
- change
   - excel/finanzplanung.xls
   - excel/haushaltsbuch.xls
   - excel/finanzuebersicht.xls
   - excel/extractBuchungen.bat
   - excel/extractFonds.bat

- change
```bat
cd d:\public_projects\MsFinance
excel\extractBuchungen.bat
excel\extractFonds.bat
```
Then open Excel and update the sheets "Buchungen", "Fonds".

# License
```bat
/**
 * @author Michael Schreiner <ich@michas-ausflugstipps.de>
 * @category finance
 * @copyright Copyright (c) 2003-2014, Michael Schreiner
 * @license http://mozilla.org/MPL/2.0/ Mozilla Public License 2.0
 *
 * This Source Code Form is subject to the terms of the Mozilla Public
 * License, v. 2.0. If a copy of the MPL was not distributed with this
 * file, You can obtain one at http://mozilla.org/MPL/2.0/.
 */
```
        