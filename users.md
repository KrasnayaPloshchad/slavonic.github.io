---
layout: default
ref: users
lang: en
---

## Church Slavonic : For Users

This page describes how to work with Church Slavonic texts in a variety of popular software platforms.

### XeTeX and LuaTeX

To work with Church Slavonic texts in TeX, you will need to use a modern Unicode-compatible TeX engine such as XeTeX or LuaTeX.
Both are part of the [TeX Live distribution](https://www.tug.org/texlive/). The following will be helpful:

* Install the hyphenation patterns for Church Slavonic. To do this, run the following command: 
  ```
  tlmgr install hyphen-churchslavonic
  ```
  Then rebuild the XeLaTeX and LuaLaTeX formats with this command: 
  ```
  fmtutil --byfmt xelatex 
  fmtutil --byfmt lualatex
  ```
* Install the `churchslavonic` package. This will install a set of Church Slavonic OpenType fonts, additional macros, 
  and handlers for polyglossia. You can install the package by running the command 
  ```
  tlmgr install churchslavonic
  ```
* If you have an older version of TeX Live or another distribution of TeX, you may need to install the hyphenation patterns 
  and additional packages manually. You can get the hyphenation patterns [here](https://github.com/slavonic/cu-tex/tree/master/hyphenation)
  and [hruch Slavonic package on CTAN](https://www.ctan.org/tex-archive/language/churchslavonic).
  Follow the instructions in the documentation.
* You can now type Church Slavonic texts using the standard commands of Polyglossia. The `churchslavonic` package 
  offers additional macros for Cyrillic numerals, drop caps and other features. See the documentation for 
  [Polyglossia](http://mirror.unl.edu/ctan/macros/latex/contrib/polyglossia/polyglossia.pdf)
  and [churchslavonic](http://ctan.altspu.ru/language/churchslavonic/churchslavonic-en.pdf) for details.
* Here is a [sample TeX file](http://www.ponomar.net/files/sample.tex)
  and its [resulting PDF output](http://www.ponomar.net/files/sample.pdf) to get you started.

### LibreOffice

Beginning with version 5.0, LibreOffice allows you to specify Church Slavonic (which it calls Church Slavic) as a 
document language. You can then take advantage of a number of features such as Cyrillic numerals (for page numbering, etc.), 
hyphenation and sorting.

* Install the Church Slavonic fonts from [this page](fonts.html) and, if needed, the 
  Church Slavonic keyboard drivers for your operating system from [this page](keyboard.html).

* If you have not already, upgrade LibreOffice to version 5.0 or later. You can download the 
  [latest version from here](http://www.libreoffice.org/download/libreoffice-fresh/). 
  On older Linux distributions, you should first remove the existing bundled version of LibreOffice 4 by running 
  ```
  sudo apt-get remove libreoffice-core
  ```
  While you can view and edit Church Slavonic text in LibreOffice 4 and earlier, you will not be able to take advantage 
  of hyphenation and other features.

* Install the Church Slavonic Hyphenation extension. To do this, download the extension from 
  [here](http://extensions.libreoffice.org/extension-center/church-slavonic-dictionary).
  To install, open LibreOffice, from the Tools menu select Extension Manager. The Extension Manager window will open. 
  Click the Add... button, and select the cu-lo.oxt file. When the License Agreement window opens, scroll to the end of 
  the license agreement text and click Accept.
  <br>
  ![install extension](http://www.ponomar.net/images/extension_install.png)

* To set the document text to Church Slavonic, select Options from the Tools menu. Under Language Settings, select Languages. 
  The Language Settings panel will appear. Under Default Languages for Documents, select Church Slavic. 
  If you need to number the pages of a document in Cyrillic numerals, you will also need to select Church Slavic under 
  Locale Setting.
  <br>
  ![locate setting](http://www.ponomar.net/images/locale_libreoffice.png)

* To turn on hyphenation, select Paragraph from the Format menu. Click on the Text Flow tab. Under Hyphenation, 
  click Automatically.
  <br>
  ![enable hyphenation](http://www.ponomar.net/images/hyphenation_writer.png)
  
* To number your pages in Cyrillic numerals, click Page Number from the Insert menu. Then double-click the resulting 
  page number. The Edit Fields dialog will open. Under Format select Native Numbering and click OK. 
  (*Note*: the default locale must be set to Church Slavic for this to work.)
  <br>
  ![cyrillic page numbers](http://www.ponomar.net/images/native_number.png)
  
* In LibreOffice Calc, you can sort data according to the Church Slavonic alphabetical order. To do this, select 
  Sort from the Data menu. Go to the Options tab. Under Language select Church Slavic.
  <br>
  ![sorting](http://www.ponomar.net/images/sort_calc.png)
  
* The Slavonic Computing Initiative also provides the 
  [Church Slavonic Converter Extension](https://extensions.libreoffice.org/extensions/church-slavonic-converter).
  It allows you to convert Church Slavonic documents into Unicode from UCS, HIP and other legacy codepages. 
  It converts a selection, or if no selection is made, the entire document. The source code is available 
  [here](https://github.com/slavonic/cuconverter-LO).
  
* There are still a number of bugs: 
  [BUG: Cannot specify _ as hyphenation character](https://bugs.documentfoundation.org/show_bug.cgi?id=85731);
  [Cannot switch the lettercase for Cyrillic Extended-B block](https://bugs.documentfoundation.org/show_bug.cgi).
  
### Apache OpenOffice

[Apache Office](http://www.openoffice.org/) is not well maintained. While you can view and edit Church Slavonic texts, 
the software will not allow declaring Church Slavonic as a language. Hence, you will not be able to use hyphenation or 
spell checking and you will not have access to Cyrillic numerals and other features. 

We suggest [using LibreOffice](https://www.libreoffice.org/download/libreoffice-fresh/) instead.

### Microsoft Office

Microsoft Corporation does not recognize Church Slavonic as a language, and so hyphenation and spell checking are 
not available, even in third-party extensions. Furthermore, there is no support for Church Slavonic in Microsoft Office. 
Church Slavonic texts **may** display correctly in Microsoft Office using the Ponomar Unicode font. 
However, your results may vary, and you may see inocrrectly positioned diacritical marks, missing characters and 
other problems. There are no workarounds for these issues. 

*We do not provide any support for Microsoft products*.

We suggest [using LibreOffice](https://www.libreoffice.org/download/libreoffice-fresh/) instead.

### Adobe InDesign

Once you have installed the Church Slavonic fonts from [this page](fonts.html), you should be able to work with Church 
Slavonic texts in Adobe InDesign. To get support for Church Slavonic hyphenation, 
download the 
[Church Slavonic Dictionary Extension for LibreOffce](http://extensions.libreoffice.org/extension-center/church-slavonic-dictionary);
then follow the instructions [here](https://helpx.adobe.com/indesign/kb/add_cs_dictionaries.html) to install it into InDesign.
Page numbering using Cyrillic numerals is not available. If you need it, [ask Adobe](https://helpx.adobe.com/contact.html?step=IDSN)
to add this feature or switch to LibreOffice.

### Where to get help?

Here are some documents that provide helpful information:

* [Church Slavonic Typography in Unicode](http://www.unicode.org/notes/tn41/) - Unicode Technical Note #41.
* [Ponomar Project Private Use Area (PUA) Allocation Policy](http://www.ponomar.net/files/pua_policy.pdf)
  (version 2.3, updated November 4, 2015; changes since v. 2.2 in yellow)

If you are having difficulties, all questions (except for those related to Microsoft products) may be addressed to 
the [SCI-Users mailing list](http://ponomar.net/mailman/listinfo/sci-users_ponomar.net).