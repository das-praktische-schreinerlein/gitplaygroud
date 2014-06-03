playgroud
=========

my personal playground





+++++++++++++++++++++++++++++Test

mat-imageimporteditor
=====================

# Desc
This is a subset of managment-tools created for the imageimport on backend of www.michas-ausflugstipps.de/.

1. allinone html-editor to prepare import of image-dirs to mediadb (more infos on [Portalinfos zur Datenpflege](www.michas-ausflugstipps.de/portal-datenpflege.html))
2. imagedir-import-generator to prepare json-files for the imageimport-editor

# TODO for me
- [ ] documentation
- [ ] externalize config
- [ ] use and optimize it :-)

# History (future first ;-)
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


mat-publishtools
=====================

# Desc
This is a subset of publishing-tools created for [Michas-Books](www.michas-ausflugstipps.de/portal-bucherstellung.html) on www.michas-ausflugstipps.de

1. PDF-tools for converting, merge, trim and so on
2. batchfiles for support
3. batchfiles for generating a book with pagenum and TOC from different webpages

# TODO for me
- [ ] documentation
- [ ] use and optimize it :-)

# History (future first ;-)
- 2014 
   - prepared the tools for going public (documentation...) 
   - separated the public-tools
- 2011
   - initial version for michas-ausflugstipps

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
src/test/example/buch-example.bat
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
   